# SurveyBoxSdk-ios
SurveyBoxSdk-ios
Mobile SDK - iOS

The Survaybox Mobile SDK allows you to collect feedback from your mobile app users. Installed in your app, the SDK will enable you to trigger targeted surveys to better understand your users and collect their opinions about your products.

The SDK is maintained and supported by Survicate - The Customer Experience & Survey Software.

Installation The SDK can be installed in the iOS mobile app using one of the three methods described below.

Swift Package Manager To install Survicate using Swift Package Manager:

Open Xcode and select New Project in the File > New > Project… menu to create a new project for your application.

Choose the App template for your project.

When prompted, choose your app name (for example, Survabox) and use the default options, next select the location to save the project and finally click on the Create button to finish project creation.

Once the project is created, open your application in Xcode and select your project’s Package Dependencies tab

Copy the Survicate SDK Swift package repository URL https://github.com/surveybox-io/SurveyBoxSdk-ios into the search field

Under Dependency Rule, select version according to your preferences

# Requirements

The SDK supports iOS 13+. Survicate Mobile SDK is distributed in a binary version and developed using Swift 5.3. The minimum required version of Xcode is 13.0, however we recommend using the SDK with Xcode 13.1 and above.

Using Survaybox Mobile SDK requires an account at [Survaybox](https://surveybox.io/). Sign up for free and find your workspace key in the Access Keys tab.

# Installation
1. [Download the latest Surveybox SDK for iOS](https://github.com/surveybox-io/SurveyBoxSdk-ios) and extract the zip. This is a ~1.3MB file and might take some time to download.
2. Open your existing iOS application Xcode project.
3. Import the `SurvayBox.embeddedframework` into your project.
4. Confirm the SDK files have been added to your project, as follows:
    + Navigate to your project build settings by selecting your project's Project File in the Project Navigator.
    + Select the main build target for your app.
    + Select the **Build Phases** tab.
    + Confirm **_Thunderhead.xcframework_** is located in the **Link Binary With Libraries** section.
    + Confirm **_ThunderheadBundle.bundle_** is located in the **Copy Bundle Resources** section.

![Screenshot 2023-06-07 at 3 01 43 PM](https://github.com/surveybox-io/SurveyBoxSdk-ios/assets/79449782/fd184f5b-25ae-4beb-a32b-9a58e1695f55)

## Configuring Framework API Key

To use the framework's features, you need to configure the API key. Follow these steps:

1. Open the `AppDelegate.swift` file.
2. Locate the `didFinishLaunchingWithOptions` method.
3. Find the line that configures the API key.
4. Replace the placeholder `YOUR_API_KEY` with your actual API key.
5. Save the changes to the `AppDelegate.swift` file.
6. Build and run the application.

Example code in `AppDelegate.swift`:

```swift
func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey: Any]?) -> Bool {
    // Other code...

    // Configure your API key
   Surveybox.configure(apiKey: "YOUR_API_KEY", customer_email: "Email")

    // Other code...

    return true
}




