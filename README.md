# ami2018-notifications
Notification dataset for our AmI-2018 paper "Predicting User Responsiveness to Smartphone Notifications for Edge Computing". The dataset is free to use for any purpose, but if using for academic purposes, please cite our work as follows:

Komninos, A., Frengkou E., & Garofalakis J. (2018).  Predicting User Responsiveness to Smartphone Notifications for Edge Computing	. 2018 European Conference on Ambient Intelligence (AmI-18). Larnaca, Cyprus, Springer.

Bibtex for convenience:

@conference {120,
	title = {Predicting User Responsiveness to Smartphone Notifications for Edge Computing},
	booktitle = {2018 European Conference on Ambient Intelligence (AmI-18)},
	year = {2018},
	month = {10/2018},
	publisher = {Springer},
	organization = {Springer},
	address = {Larnaca, Cyprus},
	abstract = {Edge computing requires the addressing of several challenges in terms of privacy, complexity, bandwidth and battery life. While in the past attempts have been made to predict users' responsiveness to smartphone notifications, we show that this is possible with a minimal number of just three features synthesized from non-sensor based data. Our approach demonstrates that it is possible to classify user attentiveness to notifications with good accuracy, and predict response time to any type of notification within a margin of 1 minute, without the need for personalized modelling.},
	keywords = {Attentivity, Notifications, Responsiveness, Smartphones},
	author = {Komninos, Andreas and Frengkou, Elton and Garofalakis, John}
}

DATA DESCRIPTION
----------------

This dataset contains details of 176,195 logged notifications received on the Android devices of 14 users, in the period between 2018-05-07 and 2018-06-05. 

The fields in the dataset contain data that was obtained from the following Android API calls:

user_id
the user's id	

id
notification serial id on user's device	

nid
notification id	
https://developer.android.com/reference/android/service/notification/StatusBarNotification.html#getId()

priority
programmed notification priority	
https://developer.android.com/reference/android/app/Notification#priority

packageName
generating application package name
https://developer.android.com/reference/android/service/notification/StatusBarNotification.html#getPackageName()

timePosted
time of notification generation	
https://developer.android.com/reference/android/service/notification/StatusBarNotification.html#getPostTime()

timeRemoved
time of notification dismissal
https://developer.android.com/reference/android/service/notification/NotificationListenerService.html#onNotificationRemoved(android.service.notification.StatusBarNotification)

sound
binary variable of whether the notification was programmed to generate a custom sound	
https://developer.android.com/reference/android/app/NotificationChannel#getSound()

default_Sound	
binary variable of whether the notification was programmed to generate a sound using the device default sound	
https://developer.android.com/reference/android/app/Notification#defaults

LED	
binary variable of whether the notification was programmed to generate a custom LED pattern	
https://developer.android.com/reference/android/app/NotificationChannel#shouldShowLights()

default_LED	
binary variable of whether the notification was programmed to generate a sound using the device default LED pattern	
https://developer.android.com/reference/android/app/Notification#defaults

VibrationPattern	
on/off time pattern of whether the notification was programmed to generate a custom vibration pattern	
https://developer.android.com/reference/android/app/NotificationChannel#getVibrationPattern()

default_Vibration	
binary variable of whether the notification was programmed to generate a sound using the device default vibration pattern	
https://developer.android.com/reference/android/app/Notification#defaults

ringerMode	
current device ringer mode when the notification was issued	
https://developer.android.com/reference/android/media/AudioManager.html#getRingerMode()

idle	
binary variable of whether the device was at idle mode	
https://developer.android.com/reference/android/os/PowerManager#isDeviceIdleMode()

interactive	
binary variable of whether the device was at interactive mode	
https://developer.android.com/reference/android/os/PowerManager#isInteractive()

screen_state	
current device screen state	
https://developer.android.com/reference/android/view/Display#getState()

lock_scr_notifs	
binary variable of whether notifications were allowed on the device lock screen	
Settings.Secure.getInt(getContentResolver(),"lock_screen_show_notifications", -1);

flags	
notification programmed flags	
https://developer.android.com/reference/android/app/Notification#flags
