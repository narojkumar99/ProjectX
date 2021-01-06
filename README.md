# ProjectX

Android App using The Movie DB API

<img src="https://github.com/muratcanbur/ProjectX/blob/master/art/app_screenshot.png" width="200" height="400">

## Description

a simple app that contain some basic functionality. It connects to the Movies DB API and fetch current popular TV shows on TMDb.


## Tech Stack
- Dagger 2 - Used to provide dependency injection
- Retrofit 2 - OkHttp3 - request/response API
- Glide - for image loading.
- RxJava 2 - reactive programming paradigm
- LiveData - use LiveData to see UI update with data changes.
- Data Binding - bind UI components in layouts to data sources

## Overview of app arch.
- follow the rules from Architecture guidelines recommended by Google.
- keep Activity only responsible for UI related code 
- ViewModel provides data required by the UI class
- Repository layer provides data to ViewModel classes. (single source of truth)

## Unit testing and Application Arch.

<img src="https://github.com/muratcanbur/ProjectX/blob/master/art/app_%20architecture.jpeg" width="500" height="300">

.
ViewModel and ViewStates classes should be tested.

* [PopularTvShowsTestSuite](https://github.com/muratcanbur/ProjectX/blob/master/app/src/test/java/co/icanteach/projectx/PopularTvShowsTestSuite.kt)

### ViewModel
need to make sure that the correct state changes occur at the right time during remote data request.

* [PopularTVShowsViewModelTest](https://github.com/muratcanbur/ProjectX/blob/master/app/src/test/java/co/icanteach/projectx/PopularTVShowsViewModelTest.kt)

### ViewState 
ViewStates are responsible for reporting changes to the UI.

* [PopularTVShowsFeedItemViewStateTest](https://github.com/muratcanbur/ProjectX/blob/master/app/src/test/java/co/icanteach/projectx/PopularTVShowsFeedItemViewStateTest.kt)
* [PopularTVShowsFeedViewStateTest](https://github.com/muratcanbur/ProjectX/blob/master/app/src/test/java/co/icanteach/projectx/PopularTVShowsFeedViewStateTest.kt)

## Blog posts about project
* [A Sample Project for your Android Interview Assignment](https://medium.com/@muratcanbur/a-sample-project-for-your-android-interview-assignment-324783e0160f)


## TODO for near future
- [ ] implement local storage example
- [ ] implement coroutines example
