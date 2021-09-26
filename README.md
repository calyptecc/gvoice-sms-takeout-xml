# gvoice-sms-takeout-xml
Convert Google Voice SMS data from Takeout to .xml suitable for use with SMS Backup and Restore.
Input data is a folder of SMS .html files from Google Takeout.

Working as of 2020-04-22.

## How to use:
1. Go to https://contacts.google.com
2. Export all Google Contacts
3. Delete all Google Contacts (this is required so that numbers show up for each thread, otherwise Takeout will sometimes only have names. If you want to skip this step, you can, but some messages won't be linked to the right thread if you do. Note that this may remove Contact Photos on iOS if you don't pause syncing on your iOS device)
4. Get Google Voice Takeout and Download
5. Restore contacts to your account
6. Download this script to your computer
7. Extract Google Voice Takeout and move the folder into the same folder as this script
8. Open terminal
9. Install pip (sudo easy_install pip)
10. sudo pip install virtualenv
11. virtualenv sms
12. pip install phonenumbers BeautifulSoup4 python-dateutil
13. python sms.py
14. Copy the file "gvoice-all.xml" to your phone, then restore from it using SMS Backup and Restore



