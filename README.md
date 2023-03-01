# Analysis of baby activity data

This repository includes an analysis of our baby's sleep activity data in his first 6 months. You can find an article describing this analysis in [Medium](https://medium.com/@sandrewge/tales-from-the-c%CC%B5r%CC%B5y%CC%B5p%CC%B5t%CC%B5-crib-7adf5537fd44).

## Data Collection

For privacy reasons I am not sharing the dataset but if you are interested you may repeat this analysis with your own baby's data since most apps are tracking similar data.

The app I chose to track our baby’s activity is [Baby Tracker](https://apps.apple.com/bz/app/baby-tracker/id1439575933) which allows you to manually enter the data. We used the app to track our baby’s daily sleep, feedings and diaper changes as well as their monthly weight and height. It is also possible to track other activities like going for a stroll or the baby’s mood. 

The main feature of the app is storing activity data in the form of *activity type*, *start time*, *end time* but doesn't provide any insights besides a visualization of activities during the day.

### Extracting data from Baby Tracker

The app data is in [Realm format](https://realm.io/). To get the data you can upload a backup of your data from a given date to your iCloud drive and then use [Realm Studio](https://www.mongodb.com/docs/realm-legacy/products/realm-studio.html) to open the file and export it in JSON format.

The features I have used for my analysis are `type` (e.g. "sleep"), `leftStart` and `leftEnd`, which correspond to the start and end times of the sleep session.

### App data privacy

You can read the app's privacy policy [here](https://neiman.tilda.ws/mybaby-privacy-policy) which states data is collected for debugging purposes and shared with third parties with the purpose of building the app (like Google’s Firebase). Their privacy policy also mentions Google’s AdMob but I have never seen any ads on this app so I am not sure it is being used. There is no identifiable information on the baby nor the parents.


