# Recruitment Challenge

First of all, thank you for your interest in Shoki !

In order to build the best team and to build a professionnal trust, each tech recruitment goes through a challenge phase, which is a simple full exercice (not some small little task). Your mission, if you accept it, is to build an application, in React-Native, from scratch, and with some constraint.

This is a 'take-home' test, which means that there is no real time limit for completion. It is better to complete it well, then rushing it, although one should strive to complete it within 5 days.

---
## State of play
For you, we have [initialized the default project](https://facebook.github.io/react-native/docs/getting-started.html), called app, without Expo. You will use `babel preset 5`, `react 16.4.1` and `react-native 0.56`. A basic `.gitignore` is provided. The same for the `.eslintrc` file which corresponds to the internal standard (norme).

## How to play
- Fork the git repository and pull it onto your development machine.
- Initialise the projects by running `yarn` or `npm install` (depending on what package manager you prefer).
- Run the packager by running `yarn start` in one terminal
- Start working on your simulator/[device](https://facebook.github.io/react-native/docs/running-on-device) by runing `react-native run-android` or `react-native run-ios`

## Goals to reach
We would like you to build a simple React-Native application whose main feature would be the creation of movie collections.
Here is what you have to do:
1. A navbar on the bottom in order to switch between 3 screens: [`Search`, `Homepage`, `Settings`].

2. The `Homepage` which is a `ScrollView` with all your collections (`Flatlist` of `TouchableOpacity`), sorted by date of creation, with a `TextInput` on the top in order to be able to create a new collection with a custom name. When you will press on of the collection, you will be redirected to a `MovieDetail` screen (either with a new screen or a `modal`).

3. The `Search` screen, with a `TextInput` on the top, in order to search a movie through [The Movie Database](https://www.themoviedb.org/?language=en). You will have to use `fetch` to call the [TMDB api](https://www.themoviedb.org/documentation/api?language=en) once the input length is more than 2 characters, in order to get the list of the movies containing this characters. You will display the 5 first results (name of the movie) as a `Flatlist` of `TouchableOpacity` elements. When the user is pressing one of this element, you have to display the informations of this movies in a `SearchDetail` screen (either with a new screen or a `modal`).

4. The `SearchDetail` screen should contain the image of the movie on top (fullWidth, 30% of the device height), the name with the release year and the director bellow, and then the description of the movie. A `Button` should be visible in order to add the collection in which the user wants to add the movie (and so let the user select in which collection he wants to add it).

5. The `MovieDetail` screen should contain the image of the movie on top (fullWidth, 30% of the device height), the name with the release year and the director bellow, and then the description of the movie. A `Button` should be visible in order to remove the movie from the current collection. A star/heart should be visible with two differentes states (full or empty) depending if the current movie is marked as `Liked` or not (kind of favorite list). By pressing it, the state should toggle.

6. The setting page should display a `Switch` and a `Button`. The `Switch` must allow to go from a Light to a dark theme, and the button must clear the [`AsynStorage`](https://facebook.github.io/react-native/docs/asyncstorage).

7. All the collections (list and movies) should be saved in the local storage (`AsyncStorage`). The same for the liked movies and the theme status -> When I am restarting the applications, I should be able to see my collections etc. without having to do anything.


## Constraint and Informations

- Obviously, we should never be stuck in one screen without be able to go back/cancel
- You can use [FastImage](https://github.com/DylanVann/react-native-fast-image) in order to replace the default `Image` component.
- You can use [VectorIcons](https://github.com/oblador/react-native-vector-icons) in order to display the star/heart icon, instead of an image.
- You can build the app as you want. The highlight words/components are suggestions, but maybe you could use `Picker` instead of a `Flatlist` of `TouchableOpacity`.
- You should use the fewest possible external components. If you are using some, you should explain why it's necessary.
- No redux or boilerplate.
- The application should only work on portrait and both on IOS and Android.
- You have to respect the norme.
