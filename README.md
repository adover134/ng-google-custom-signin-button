# Angular Custom Google SSO Button Implementation

This Angular project demonstrates a customized implementation of Google Sign-In using Angular components. By integrating the Google Sign-In API, this application provides a seamless authentication experience for users.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.

## How to implement the custom google button - Angular with standalone

1. Add provider in 'app.config.ts' of your project - which is given in the line 18~34 of app.module.ts file of this repository.
2. Import SocialAuthServiceConfig and GoogleLoginProvider - which is given in the line 8~12 of app.module.ts file of this repository; except SocialLoginModule.
3. Generate google-signin component on proper directory of your project, then copy-paste from google-signin component of this repository.
4. Add ngOnInit function and googleSignin function of app.component.ts file of this repository to a component which you will add login button.
5. At the same component, Import the google-signin component. Also import SocialAuthService and SocialLoginModule from @abacritt/angularx-social-login. Then add component and module to imports of the component.
6. Add an instance of the SocialAuthService as parameter of constructor of the component.
7. Finally, add the <app-google-signin> tag on the template which is binded with the component.

For example, let us assume that you will add the button on 'login.component'.
Then you need to add google-signin component and SocialLoginModule to imports of 'login.component.ts' file.
After then, you need to add ngOnInit and googleSignin function in LoginComponent class.
Finally, you need to add the <app-google-signin> tag, which is selector of the google-signin component.
