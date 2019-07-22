# **Test plan for Monefy app (iOS)**

**Object of testing**: Monefy application for money management (standard version, not updated to the pro version).

**Version**: 1.2.10

**OS**: iOS 9.0 or higher

**Devices**: iPhone, iPad, iPod Touch

Monefy is a money management tool which allows users to track their expenses and income. Therefore, operations of adding this data to the app and calculating total balance/expenses for a chosen period of time is the main function of Monefy. Considering the app has a pro version, the business goal is to sell it to the customer. This goal can be achieved if the main functions of this app are working and a customer has a positive user experience. Also, we need to check that customer doesn’t have access to special features until he updates to the pro version. 
So, first of all, we need to check:
 - the application can be installed and updated without losing user data
 - work of main functions: adding money to total balance, adding expenses, checking calculations of total expenses and income for a chosen period of time
 - user doesn't have access to pro features
 - design of the app is responsive and looks the same on devices with a different form factor

## 1 Install and update application
### 1.1 Install application
|#| Step | Expected result |
| ------ | ------ | ------ |
|1| Install Monefy app from App Store | Application is installed successfully |
|2| Open application| Application is opened. System message about given the app permission to send messages is displayed |
|3| Grant permission to send messages | System message is closed. The main display of app is shown with tips on how to use this app |

### 1.2 Update application
|#| Step | Expected result |
| ------ | ------ | ------ |
|1| Update Monefy app from App Store | Application is updated successfully |
|2| Open the application| Application is opened. User data displayed as it was before the update |

**Additional step for PRO version**

|#| Step | Expected result |
| ------ | ------ | ------ |
|1|  Check PRO version features availability| PRO version features are available after update |

## 2 Functionality testing
### 2.1 Adding new income
|#| Step | Expected result |
| ------ | ------ | ------ |
|1| Open Monefy App| Application is opened. The main screen is displayed |
|2|Tap "+"" button | Form for adding new income is opened |
|3| Enter sum, add a note and choose a category| App shows the main screen. Balance field and income in the circle are updated. System message appeared with info about the operation with "Undo" option |
|4|Tap on balance button |  List of balance operations is displayed divided by category names|
|5|Tap on operation category that we chose on step 3| List of completed operations in this category is displayed, operation from step 3 also in this list |

### 2.2 Adding new expenses
|#| Step | Expected result |
| ------ | ------ | ------ |
|1| Open Monefy App| Application is opened. The main screen is displayed |
|2|Tap "-"" button | Form for adding new expense is opened |
|3| Enter sum, add a note and choose a category| App shows the main screen. Balance field and expenses in the circle are updated. System message appeared with info about the operation with "Undo" option |
|4|Tap on balance button |  List of balance operations is displayed divided by category names|
|5|Tap on operation category that we chose on step 3| List of completed operations in this category is displayed, operation from step 3 also in this list |

### 2.3 Other features
Also, we can test other features:
1. Adding expenses by tapping on the expenses category icon
2. Customize main screen info by choosing a time period (day/week/month/year/all/chosen date) or/and account
3. Transfer money between user accounts
4. Adding a new account (default currency)
5. App customization settings
6. Balance settings
7. Data backup

### 2.4 PRO version features
We should check that pro features aren't available until user updates to the pro version
List of these features:
1. Adding new categories
2. Create accounts in different currencies
3. Scheduled income/expenses records
4. Synchronization with Dropbox and Google Drive
5. Passcode protection
6. Dark theme

## 3 Testing on different devices
We need to check that the app is responsive and looks the same on devices with a different form factor. Monefy can be installed on iOS 9.0 and higher. So there is a list of devices suitable for this app:
- iPhone 4S and newer
- iPad 2 and newer
- iPod Touch 5th gen and newer
We won't test on all of the devices because it's unnecessary and time-consuming. But we need to take into consideration display size and resolution of devices as well as there popularity (amount of users) and based on that make a decision about devices on which to test our application.

## 4 Localization testing
Monefy support several languages: English, Bulgarian, Croatian, German, Italian, Malay, Polish, Portuguese, Russian, Simplified Chinese, Spanish, Turkish, Ukrainian.
So we need to check that everything is translated correctly in chosen languages when we choose a language in the app settings.

## 5 Device specific tests
We need to check how Monefy app behave:
- if there is an incoming call/message
- if a device goes to/from sleeping mode, or when a screen is locked
- if a device is charging, or battery is low
- etc.

## 6 Network testing
We need to check how Monefy app behave:
 - when it connected to the Internet through Wi-Fi
 - when it connected to the Internet through 4G
 - when it connected to the Internet through 3G
 - when it out of network reach
 - etc.

## 7 Security testing  (for PRO version)
According to Monefy feature list, in its PRO version passcode protection is available with three options:
 - 4-digit password
- TouchID
- FaceID

**Disclaimer**: I don't have PRO version, so further is my speculation on how it probably should work.
Devices for the test: iPhone 7 and iPhone Xs

|#| Step | Expected result |
| ------ | ------ | ------ |
|1| Open Monefy on iPhone 7| Monefy app is opened. User should enter a passcode or use TouchID to use the app |
|2| Enter passcode| Passcode is accepted. Now user can use the app|
|3| Repeat login with TouchID| TouchID is accepted. Now user can use the app|
|4| Repeat login with FaceID using iPhone Xs| FaceId is accepted. Now user can use the app|

## 8 Integration testing (for PRO version)
According to Monefy feature list, in its PRO version Synchronization with Google Drive and Dropbox is available, which allows users to use the same account on several devices. 
**Disclaimer**: I don't have PRO version, so further is my speculation on how it probably should work.

|#| Step | Expected result |
| ------ | ------ | ------ |
|1| Open Monefy on the device A| Monefy app is opened|
|2| Enable synchronization with Google Drive| Synchronization is enabled|
|3|Open Monefy on the device B and use the same account as at device A| Monefy app is opened under the same account|
|4|Add some expenses| Expenses are added, changes are displayed on the main screen |
|5|Check how expenses are displayed in the app on device A| Expenses are synchronized and displayed the same way as on device B|



