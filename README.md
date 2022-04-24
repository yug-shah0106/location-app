
# Our App in React Native

This is my first React Native project done with expo.
[Demo Video](https://youtu.be/RHxPceOgMB0)

Desktop version in React can be found [here](https://github.com/wecode-bootcamp-korea/Codebnb-frontend).

### Goal

- Componentize reusable features
- Learn to utilize popular libraries
- Add messaging feature using socket.io

### Librares used

- react navigation
- socket.io
- redux
- formik
- yup
- [react-native-calendars](https://github.com/wix/react-native-calendars)
- [lodash](https://lodash.com/)
- [moment](https://momentjs.com/)
- react-native-maps

### Features Implemented

**Signup and Login**

- Error handling

**Home**

- Search filter
- Calendar
- Counter

**List & Details**

- Fetching data
- Google maps
- Image slider

**Host**

- Adding images using native ImagePicker
- Getting current location

**Message**

- Creating socket connection
- Sending and receiving messages

### Features componentized

### colors


**Example**

```jsx
import colors from "../config/colors.js";

// inline style
<View style={{color: colors.red}} />

// styled components
const Container = styled.View`
	color: ${colors.red}
`
```


### Typography

**Font family**

```jsx
--App.js--

const Common = styled.SafeAreaView`
  ${Platform.select({
    ios: {
      fontFamily: "Avenir",
    },
    android: {
      fontFamily: "Roboto",
      paddingTop: StatusBar.currentHeight,
    },
  })}
`;
```

**Example**

```jsx
import * as Typography from "../config/typography.js";

<Typography.H1 color={colors.red}>Welcome to our App</Typography.H1>
```


### Buttons

**Button Types**

 1. Contained Button

 2. Outlined Button

 3. Icon Button

 4. Floating Action Button

 5. Text Button

 6. Underlined Text Button

**Anatomy**

**Example**

```jsx
import * as Button from "../components/Button.js";

<Button.BtnContain
  icon="search"
  label="Next"
	labelcolor={colors.white}
  color={colors.red}
  size="small"
  disabled={false}
  onPress={() => onNavigate()}
/>
```


### Lists

**List Types**


 1. Default list item with contained icon 

 2. Default list item with icon to the right

 3. User list item

**List Anatomy**


**Example**

```jsx
import * as List from "../components/List.js";

<ListItem.Default
  title="Title"
	secondary="Secondary Text"
  containedicon="location"
  onPress={() => onNavigate(item.title)}
/>

<List.UserList
  title="User Name"
  secondary="Secondary Text"
  image={userimage}
  meta={item.dates}
  onPress={() => handleNavigation(item)}
  RightActions={() => (
    <DeleteItem onPress={() => handleDelete(item)} />
  )}
/>
```


### Cards

**Card Types**


 1. Default

 2. Review

**Card Anatomy**

**Example**

```jsx
import * as Cards from "../components/Cards.js";

<Cards.Image
  image={image}
  sub="Subheader"
  title="Title"
  secondary="Secondary text"
  action="View More"
  onPress={() => console.log(item)}
/>
```


### Issues to resolve in the future

- keyboardshouldpersist
- Typescript
