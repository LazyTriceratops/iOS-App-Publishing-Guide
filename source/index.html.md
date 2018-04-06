---
title: Publishing an iOS Application to the App Store

language_tabs: # must be one of https://git.io/vQNgJ

toc_footers:
  - <a href='developer.apple.com'>Sign up for a Developer License</a>
  - <a href='itunesconnect.com'>iTunes Connect</a>

search: true
---

<p style="font-size:32px;font-weight:bold;text-align:center;padding-top:25px;">Publishing an iOS Application to the App Store</p>

# Introduction

Publishing an App to Apple’s App Store can be a complicated process. Over the years their publishing platform, iTunes Connect, has become easier to work with. But the first attempt at publishing an iOS App can still be intimidating. This set of instructions will help assist you in connecting your app to iTunes Connect, complete the process of preparing it for review, publishing it to the App Store, and interpreting the generalized data tracked through iTunes Connect.

# Materials

> ◽ Already built iOS Application. <br>
> ◽ An Apple Developer Account (see link on left of screen)

In order to publish an application to the App Store, only two things are needed. 1) An application. This set of instructions is based off the assumption that you have completed the process of developing an application in Xcode. And 2) an Apple Developer account. A Developer Account should have previously been created through developer.apple.com.

## Preparations:

In addition to the required materials, you will also need to prepare your application's icon set and at least one (with a maximum of ten) screen shots.

<aside class="notice">
Icons can be easily prepared by downloading the Mac App Prepo on the Mac App Store. A 1024px x 1024px version will be needed for iTunes Artwork.
</aside>
<aside class="notice">
Screenshots can be prepared in the simulator by pressing `CMD + S` on the screen you would like to capture in the simulator.
</aside>

# Creating your App in iTunes Connect

## Step 1 — Initialization

iTunes Connect's home screen contains several icons to help you manage various parts of of the application deployment process. The first step in publishing an app is creating an application in iTunes Connect. To do this, select the "My Apps" icon at the top left of the available icons. From here, select the plus button (which is also located towards the top left of the screen).

This will bring up the New App card as seen below:

> 1. Choose the type of app you are publishing.
2. Pick a name for your application. This must be unique, and with the size of the App Store, this can be difficult. One method of avoiding conflicts is to add a hyphenated title (i.e. "<name of app> - The best <single word describing app> west of the Mississippi").
3. Select the language you expect most of your user base to use.
4. The Bundle ID is what links your app in iTunes Connect to the app you've built in Xcode. If your app's Bundle ID isn't listed, you will need to go back to <a href='developer.apple.com'>developer.apple.com</a> and set it up.
5. The SKU will need to be a unique identifier. After this point it won't be needed for the purposes of this tutorial.

![](/images/NewAppInit.png "New App Initialization")

## Step 2 — App Information

After creating your app in iTunes Connect, you will be greeted with the App Information page. This page contains general information about your app that will inform your users about the various aspects of your app before purchasing.

> 1. This is the name you created in the previous step.
2. Subtitles will appear under your App Name and should help describe your app as briefly as possible.
3. The Privacy Policy is optional, unless your app gathers data or is a "Made for Kids" app. In which case you will be required to enter a URL to your Privacy Policy.
4. If you ever change your Bundle Identifier in Xcode, you will also need to change it here.
5. Here you can add a secondary language if applicable.

![](/images/AppInformation.png "App Information")

## Step 3 — Pricing and Availability

The next tab down on the left side of the screen is the Pricing and Availability setup. From here you will need to set the price for your app (even if it is going to be sold as Free). Prices can also be set differently for different currencies.

<aside class="notice">
The selected price is the customer facing price. Apple takes care of the tax then splits the revenue 70%/30% with the developer.
</aside>

You are also able to setup preordering, customize availability by territory, offer discounts for volume purchases, and disable bitcode auto-recompilation.

## Step 4 — Prepare for Submission

To finish the preparation process, select <b>1.0 Prepare for Submission</b>. This is the largest step (second to creating your app) and most complicated. This is simplified by handling each section individually.

>1. Every app submission requires at least one (and as many as 10) previews and screenshots for each of your app's supported devices. This is best accomplished by running your app in the simulator and pressing ⌘ + S to save a screenshot. A preview can be filmed by using either a device or the simulator and the Quicktime application to record the screen.
2. Promotional text is the first thing a user will see when they tap on your app in the App Store. It is intended to be used as a way to highlight current features. Under this is the App Description, which is intended to detail the content of your application.
3. Keywords — used to help users find your app when searched.<br>Support URL — a link to an external website used to answer potential user's questions.<br>Marketing URL — an optional link to help further inform a potential user on why they should download your app.
4. A build of your app will appear here after it is sent to Apple through Xcode and finishes processing.
5. General App Information — Starting with the upper left, the App Store Icon will be filled in when an uploaded build of your app is selected. Below this is the version number. it is populated with `1.0`, and should be increased with every version submitted to the App Store. Apple will not approve an app submitted with a less than `1.0` version number. A general age rating will be generated for your app by tapping `edit`, and filling out the corresponding survey. If you own a Copyright the date and Copyright holder should be entered in the field provided. A street address is required for an App Store submission, it will not be viewable on the App Store (unless `Trade Representative Contact Information` is selected, in which case the information provided will be viewable in the Korean store).
6. If your application requires users to sign in you will need to provide a generic user for Apple to use with their review. You will also need to provide contact information for the reviewer and can provide any notes to help the reviewer understand aspects of your app.

![](/images/PreparingForSubmission.png "App Information")

<aside class="warning">
 Be sure to hit `Save` in the upper righthand side of the window before continuing.
</aside>

## Step 5 — Archiving and Sending a Build to Apple

Jumping out of iTunes Connect, open your application's project file. In order to get the app from Xcode to iTunes Connect an archived build needs to be sent to Apple.

>1. Before Archiving your project, make sure your project set to run on `Generic iOS Device` (or a physical device you have connected and paired to your developer account).
2. In the menu bar, select `Product` and Archive.

Archive Step 1:
![](/images/Xcode-01.png "Archive Step 1")

>3. After the archive is built, select `Send To App Store`

Archive Step 2:
![](/images/Xcode-02.png "Archive Step 2")

>4. Leave the settings at their default state and select `Next`.

Archive Step 3:
![](/images/Xcode-03.png "Archive Step 3")

>5. Select `Next`.

Archive Step 4:
![](/images/Xcode-04.png "Archive Step 4")

>6. Select Upload. This process should take up to about 5 minutes depending on the size of your app.

Archive Step 5:
![](/images/Xcode-05.png "Archive Step 5")

After uploading the build it will take some time to process on Apple's servers before being available to add to your iTunes Connect (this has recently been improved to take 5-20 minutes). Once it has finished processing Apple will send an email (or push notification if you have the iTunes Connect iOS App downloaded).

Switching back to iTunes Connect, select the build you just uploaded in the <b>1.0 Prepare for Submission</b> section (see Step — 4 item 4). Once the build has been selected, save your progress again and select `Submit for Review`. The review process can take anywhere from a few hours to a few days to complete, but once it does your app will be available in the App Store for download (unless Apple rejects it, in which case, follow their directions on what needs to be changed and follow the above steps to resubmit).

Best of luck!
