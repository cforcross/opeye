# Configuration of Project on Google cloud console and PlayStore

Remember we skipped step of secret_json file while setting up Fastlane. We need to provide that file to Fastlane, it’s like an address on envelope. So Fastlane would know where to deliver that build.

secret_json is a Google Developers Service Account Key which will be used for authentication of requests made to Google Play Developer API. Then Fastlane could establish a connection to this API to publish our app to Google Playstore.

Now Open Google Play Console go to 
`Settings > Developer Account > API Access` and link your cloud console project with play console.

# Create Service Account
Go to your ` Google Cloud > IAM & Admin > Service Accounts > Select Your Project > “CREATE SERVICE ACCOUNT”`

# Generate jks
`keytool -genkey -v -keystore my-release-key.keystore -alias alias_name -keyalg RSA -sigalg SHA1withRSA -keysize 2048 -validity 10000`
- Password `carnage` 
- first name and last name => chowa cross
- Organization  `self`