---

### Biography of a React Native App
<span style="color:gray">The Story of GroupThreads Dash</span>

Note:
influenctial time

---

#### This is a Story

React Native and Leading Tech Decisions

Developing Core Principles

---

#### Context

Coffeeshop Meeting with Keagan, Co-Founder GroupThreads

GroupThreads' Distruptive Model

High-Growth -> Need for Better Technology

Note:
Keagan was CMO

---

#### Mobile App

Desktop Angular 1.0 Web App

Providing a Mobile Experience

Investors

Note:
- There is nothing wrong with a working app, as long as it's usable
- 

---

### Whiteboard Night

CEO Shares Vision

Mockups with Balsamiq & Google Drive

---

![home](assets/home.png)

---

![home_actual](assets/home_actual.png)

---

![calculator](assets/calculator.png)

---

![calculator_actual](assets/calculator_actual.png)

---

![product_page](assets/product_page.png)

---

![product_page_actual](assets/product_page_actual.png)

---

#### The React Native Decision

Experience with Golang on Mobile

Surveying Future Users

---

#### Lesson 0

*Don’t decide on using a cross-platform mobile technology until you know who is going to be using the app*

---

#### What Distinguishes React Native

Know FE Web? React? Great.

Open Source, Big Community

The Real Deal: A Native Experience

Code Push

Better Than Golang on Mobile

---

#### Achieving a Native Experience

Your Phone is Running React with JavaScript Core

JavaScript is Doing the Business Logic

React Problem: Need to Sync Virtual DOM to UIKit, Asynchronously

The Solution: A Message Queue

---

#### The Bridge: JavaScript Communicating with Native

Events Registered in Native Code (touches, network calls, etc.)

Asynchronous API (to Native), Batched Messages, Exchange Serializable Messages

Native -(JSON)-> JavaScript -(JSON)-> Native -> Execute Commands & Update UI

JS Wrappers: Take Method and Module Name, Arguments, and Add it To Message Queue

---



---


```javascript
    render() {
        return React.createElement(
          View,
          { style: Styles.modalContainer },
          React.createElement(
            View,
            { style: { borderColor: '#303030' } },
            React.createElement(Sae, {
              label: 'Search for a Product',
              height: 38,
              onChangeText: text => this.setState({ searchText: text }),
              iconClass: FontAwesomeIcon,
              iconName: 'search',
              iconColor: 'white',
```

```jsx
   render() {
    return (
      <View style={Styles.modalContainer}>
        <View style={{borderColor: '#303030'}}>
          <Sae
            label={'Search for a Product'}
            height={38}
            onChangeText={(text) => this.setState({searchText: text})}
            iconClass={FontAwesomeIcon}
            iconName={'search'}
            iconColor={'white'}
```

---

#### Starting with a Boiler Plate

Choosing a Boiler Plate

Minimal Templates

---

#### Ignite

Reusable Components

Redux: Sagas, Reducers, Actions

---

#### 

Note:
Ask how much they know about this pattern

---

#### Saga

```jsx
// Generator in the LoginSaga
// Waits for the Login button press
export function * watchLoginAttempt () {
    // daemonize
    while (true) {
      // wait for LOGIN_ATTEMPT actions to arrive
      const { username, password } = yield take(Types.LOGIN_ATTEMPT)
      // call attemptLogin to perform the actual work
      yield call(attemptLogin, username, password)
    }
  }
```

---

#### Links

* [GroupThreads Dash on the App Store](https://itunes.apple.com/us/app/groupthreads-dash/id1162856658?mt=8)



---