# :crystal_ball: Table of Content

| [Packages](README.md#package-packages) | [Routes](README.md#door-routes) | | [Public Routes](README.md#unlock-public-routes) | | [Private Routes](README.md#lock-private-routes) | | [Components](README.md#pushpin-components) | [Folder Structure](README.md#file_folder-folder-structure) | | [Redux-Actions](README.md#sparkler-redux-actions) | | [Redux-Reducers](README.md#sparkler-redux-reducers) | | [General](README.md#link-general) |
  


## :package: Packages 
- `axios`
- `formik`
- `history`
- `jalali-moment`
- `react`
- `react-dom`
- `react-countdown`
- `react-fade-in`
- `react-image-appear`
- `react-loading-skeleton`
- `react-modern-calendar-datepicker`
- `redux`
- `react-redux`
- `redux-thunk`
- `react-redux-loading-bar`
- `react-redux-toastr`
- `react-router-dom`
- `react-scripts`
- `react-select`
- `styled-components`
- `swiper`
- `video.js`
- `videojs-contrib-hls`
- `videojs-contrib-quality-levels`
- `videojs-hls-quality-selector`
- `videojs-landscape-fullscreen`
- `videojs-seek-buttons`
- `videojs-titleoverlay`
- `videojs-vtt-thumbnails`


## :door: Routes 
* This route forward user to __Home__ component                         => `<Route path='/' exact component={Home}/>`
* This route forward user to __Vod__ component                          => `<Route path='/vod' exact component={Vod}/>`
* This route forward user to __SingleVod__ component                    => `<Route path='/vod/:id' component={SingleVod}/>`
* This route forward user to __Pardis__ component                       => `<Route path='/pardis' component={Pardis}/>`
* This route forward user to __Learning__ component                     => `<Route path='/learning' component={Learning}/>`
* This route forward user to __Kids__ component                         => `<Route path='/children' component={Kids}/>`
* This route forward user to __PaymentReceipt__ component               => `<Route path='/invoice/:id' exact component={PaymentReceipt}/>`
* This route forward user to __Live__ component                         => `<Route path='/live' component={Live}/>`
* This route forward user to __Search__ component                       => `<Route path='/search' component={Search}/>`
* This route forward user to __Series__ component                       => `<Route path='/series' exact component={Series}/>`
* This route forward user to __SingleSerial__ component                 => `<Route path='/series/:id' component={SingleSerial}/>`
* This route forward user to __Genres__ component                       => `<Route path='/genres' exact component={Genres}/>`
* This route forward user to __SingleGenre__ component                  => `<Route path='/genres/:name' component={SingleGenre}/>`
* This route forward user to __Cast__ component                         => `<Route path='/cast/:id' component={Cast}/>`
* This route forward user to __Sport__ component                        => `<Route path='/sport' component={Sport}/>`
* This route forward user to __TermsAndConditions__ component           => `<Route path='/terms-and-conditions' component={TermsAndConditions}/>`
* This route forward user to __SingleCategory__ component               => `<Route path='/category/:type/:id/:name' component={SingleCategory}/>`
* If user enter the wrong url so user forward to __NotFound__ component => `<Route path='*' component={NotFound}/>`


## :unlock: Public Routes 
* This is Public Route, if user want to enter Private Route must be login first  => `<PublicRoute path='/login' isAuth={this.props.isAuth} component={Login}/>`


## :lock: Private Routes 
### This is Private Routes, if user login, he/she can enter to Private Routes
* This route forward user to __Packages__ component                     => `<PrivateRoute path='/accounting/packages' isAuth={this.props.isAuth} component={Packages}/>`
* This route forward user to __Invoice__ component                      => `<PrivateRoute path='/invoice/preview/:id' exact isAuth={this.props.isAuth} component={Invoice}/>`
* This route forward user to __FullScreenPlayer__ component             => `<PrivateRoute path='/arm/player/:id' isAuth={this.props.isAuth} component={FullScreenPlayer}/>`
* This route forward user to __Profile__ component                      => `<PrivateRoute path='/profile' exact isAuth={this.props.isAuth} component={Profile}/>`
* This route forward user to __EditProfile__ component                  => `<PrivateRoute path='/profile/edit' isAuth={this.props.isAuth} component={EditProfile}/>`


## :pushpin: Components 
### Intro components and what they are doing in app
#### Home => `this component included Menu, Home Main Slider, Horizontal Slider => included Category and Category Items`
#### Vod  => `this component exist on Menu and included Movies Category and Movies Item`
#### SingleVod  => `in Home or Vod component if user click on a Movie, user forward to single page that Movie`
#### Pardis  => `this component exist on Menu and included Cinema for live Movies`
#### Learning  => `this component exist on Menu and included Learning things for Adult and Kids`
#### Kids  => `this component exist on Menu and included Kids animation and cartoons`
#### Login  => `this component exist on Left Menu and user can sign or login for access to Private Route`
#### Packages  => `if user login and want to see movie and series, this component included Packages to buy subscription`
#### Invoice  => `if user click one of those Package, he/she can see Invoice for pay`
#### PaymentReceipt  => `after user pay the price for subscription, he/she can see Payment Receipt`
#### Live  => `this component exist on Menu and included Tv Shows`
#### FullScreenPlayer  => `when user click on play button for see movie or series, this component provide him/her Full Screen Player to show movie or serial`
#### Search => `this component exist on Left Menu and when user want to search Movie or Series, can use this`
#### Profile => `when user login then he/she can see his/her Profile`
#### EditProfile => `when user login then he/she can Edit his/her Profile`
#### Series => `this component exist on Menu and included Series Category and Series Item`
#### SingleSerial => `in Home or Series component if user click on a Serial, user forward to single page that Serial`
#### Genres => `this component exist on Menu and included Movies and Series Genres`
#### SingleGenre => `in Genres component if user click on a Genre, user forward to single page that Genre`
#### Cast => `this component provide user for search movie and series based on actor`
#### Sport => `this component exist on Menu and included Live Sports and Archive Sports`
#### TermsAndConditions => `this component exist on Footer and included Terms and Conditions`
#### SingleCategory => `in Home page if user click on more items in specific category, he/she forward to all items on that category`


## :file_folder: Folder Structure 
- ar-tv/
  - node_modules/  
  - public/
    - index.html
    - favicon.ico
    - logo192.png
    - logo 512.png
    - manifest.json
    - robots.txt 
  - src/
    - config/
    - helpers/
    - redux/
    - statics/
    - styles/
    - ui/
    - API.js
    - API.test.js
    - history.js
    - index.js
    - PrivateRoute.jsx
    - PublicRoute.jsx
    - serviceWorker.js
    - setup Tests.js
    - Text.js
  - .env
  - .gitignore
  - package.json
  - package-lock.json
  - README.md
  - yarn.lock
 

## :sparkler: Redux => Actions
#### cast.js => `find movie and series based on actor` 
#### category.js => `showing categories in Home page` 
#### genre.js => `showing categories subset in Home page and show single category` 
#### home.js => `main slider in Home page and Home Horizontal Slider Lists` 
#### invoice.js => `invoice for pay for subscription ` 
#### kid.js => `movies about kid` 
#### learning.js => `movies about learning` 
#### pardis.js => `show cinema movies` 
#### search.js => `search movie and series` 
#### serial.js => `all of series existance in this page` 
#### singleProgram.js => `single page for paly movie or serial` 
#### sport.js => `show live and archive sport` 
#### index.js => `general action and function` 


## :sparkler: Redux => Reducers
#### authReducer.js => `switch on auth action for authentication`
#### castReducer.js => `switch on cast action for set cast vod`
#### categoryReducer.js => `switch on category action for set single category and more items`
#### genreReducer.js => `switch on genre action for set all genres and single genre`
#### homeReducer.js => `switch on home action for set home slider and set home horizontal slider items and set home categories`
#### invoiceReducer.js => `switch on invoice action for set invoice data`
#### kidReducer.js => `switch on kid action for set kid main slider and set kid horizontal slider items and set kid categories`
#### learningReducer.js => `switch on learning action for set learning main slider and set learning horizontal slider items and set learning categories`
#### packageReducer.js => `switch on package action for set package list`
#### pardisReducer.js => `switch on pardis action for set pardis main slider and set pardis horizontal slider items`
#### paymentReducer.js => `switch on payment action for set payment detail`
#### playerReducer.js => `switch on player action for set channel list and set active channel`
#### searchReducer.js => `switch on search action for set searched text and set search result and increase search counter`
#### serialReducer.js => `switch on serial action for set serial header slider and set single serial and set serial seasons and set season episods and set episode secure link and set series horizontal sliders items`
#### singleProgramReducer.js => `switch on singleProgram action for set single program list and set single program secure link`
#### sportReducer.js => `switch on sport action for set sport live list and set sport live secure link and set sport archive list and set sport archive secure link`
#### userReducer.js => `switch on user action for set edited profile and set user birth date and set user mobile and set user payment history and set user profile and set user subscribe status`
#### vodReducer.js => `switch on user action for set horizontal sliders and set single vod and set slider items and set vod comments and set vod secure link and set movies horizontal sliders items and set vod name`

## :link: General
#### if action call an api start with get,              example : `getHomeSlider`
#### if action set data to store start with set,        example : `setHomeSlider`
#### if action clear store start with clear,            example : `clearHomeSlider`
#### if action set loading , start with is_x_loading,   example : `isHomeSliderLoading`
