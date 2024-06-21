## JDT's Google Merchant Center Feed Status Setup Guide

## Dependencies
The following libraries are required to run the Google Merchant Center Feed Status Reporter:
- [requests](https://pypi.org/project/requests/)
- [google-api-python-client](https://pypi.org/project/google-api-python-client/)
- [google_auth_oauthlib](https://pypi.org/project/google-auth-oauthlib/)
- [google-auth-httplib2](https://pypi.org/project/google-auth-httplib2/)
- [google-auth](https://pypi.org/project/google-auth/)
- [oauth2client](https://pypi.org/project/oauth2client/)
- [tabulate](https://pypi.org/project/tabulate/)

## Set Up
To set up the Google Merchant Center Feed Status Reporter, complete the following steps:
1. Clone the 'google/gmc-feed_status' sample code from [GitHub](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository).
2. Create a folder for the authentication files within the '/Google/GMC-feed_status/content', titled 'authfiles'.
    - <b>your home directory/Google/GMC-feed_status/content/authfiles/</b>
3. Setup authentication files:
    - Go to [Google Merchant Center](https://merchants.google.com/) and obtain the API Key:
    a. In Merchant Center, in the Settings menu, select Content API.
    b. Click Authentication.
    c. Click <b>'+'</b> CREATE API KEY. 
    - If prompted, read and accept the terms of service agreements. The new key downloads automatically.
    d. Rename the downloaded credentials file to service-account.json.
    - Note: This filename is defined in the _constants.py file, which is located in '/Google/GMC-feed_status/content/' folder.'
    e. Move the service-account.json file to your 'home directory/Google/GMC-feed_status/content/authfiles/' folder.
4. Setup mechant-info.json:
    a. In your 'home directory/Google/GMC-feed_status/content/authfiles/'', folder create an empty merchant-info.json file.
    b. In merchant-info.json, add the following text:
        [
            {"propName": "your_acct_name", "merchantId": "acct_merchant_id"},
        ]
        - Replace <b>your_acct_name</b> with your account name and <b>merchant_id</b> with your merchant ID.
        - 'your_acct_name' is arbitrarily named and is based on your preference for display and identification.
        - 'merchant_id' is the Merchant Center merchant ID.
        - If you have multiple merchant accounts, add additional entries in the array in the same format.
    c. Save and close the file.
5. Run the sample code: '<b>python home directory/Google/GMC-feed_status/gmc-feed_status_report.py</b>' and follow the prompts.