# react-navigation-codes-for-mobile-app

## Install React-Navigation
```node
npm install @react-navigation/native
```

## Install dependencies (for expo app)
```node
expo install react-native-gesture-handler react-native-reanimated react-native-screens react-native-safe-area-context @react-native-community/masked-view
```

## Install dependencies (with npm)
```node
npm install react-native-reanimated react-native-gesture-handler react-native-screens react-native-safe-area-context @react-native-community/masked-view
```

## Install react-navigation/stack
```node
npm install @react-navigation/stack
```

## Use React-Navigation to your app

* Import 
```javascript
import 'react-native-gesture-handler';
//the above line will be on the top
//...
import { NavigationContainer } from '@react-navigation/native';
import { createStackNavigator } from '@react-navigation/stack';
```

## Create and use Stack navigator
* Import your screen components like HomeScreen, LoginScreen, SignupScreen then use them  

```javascript
const Stack = createStackNavigator();

export default function App(){
return (
    <NavigationContainer>
      <Stack.Navigator initialRouteName="Home">
        <Stack.Screen name="Home" component={HomeScreen} />
        <Stack.Screen name="Login" component={LoginScreen} />
        <Stack.Screen name="Signup" component={SignupScreen} />
      </Stack.Navigator>
    </NavigationContainer>
  );
}


```

## Move to another screen
* Press a button to go to LoginScreen from HomeScreen
```javascript
export default function HomeScreen({ navigation }) {
  return (
    <View>
      <Text>Home Screen</Text>
      <Button title="Login" onPress={() => navigation.navigate('Login')} />
    </View>
  );
}

```

## Go back to previous screen

```javascript
<Button title="Go back" onPress={() => navigation.goBack()} />
```

## Go back to the first screen
```javascript
<Button title="Go back to first screen in stack" onPress={() => navigation.popToTop()} />
```


