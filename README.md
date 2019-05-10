# Actions on Google: Java Client Library Boilerplate with AppEngine Framework

Boilerplate to help you get started quickly with the Java client library for Actions on Google.
The original source from https://github.com/actions-on-google/dialogflow-webhook-boilerplate-java was amended with AppEngine Framework

### Setup Instructions

#### Action Configuration
1. From the [Actions on Google Console](https://console.actions.google.com/), add a new project (this will become your *Project ID*) > **Create Project**.
1. Scroll down to the **More Options** section, and click on the **Conversational** card.
1. From the left navigation menu under **Build** > **Actions** > **Add Your First Action** > **BUILD** (this will bring you to the Dialogflow console) > Select language and time zone > **CREATE**.
1. In Dialogflow, go to **Settings** ⚙ > **Export and Import** > **Restore from zip**.
    + Follow the directions to restore from the `agent.zip` file in this repo.

#### Requirments
1. Working Java (>=8) Development Environment
1. [Maven](https://maven.apache.org/download.cgi)
1. Download & install the [Google Cloud SDK](https://cloud.google.com/sdk/docs/)

#### Compiling and starting the development server
Run the following commands

    mvn clean package
    
    mvn appengine:devserver

#### Tunneling Fulfillment to your local development server
1. Start forwarding the HTTP traffic with a service like [Serveo](https://serveo.net) to your local development server

       ssh -R 80:localhost:8080 serveo.net

1. In the [Dialogflow console](https://console.dialogflow.com), from the left navigation menu > **Fulfillment** > **Webhook** set URL according to your tunnel endpoint
https://myservice.serveo.net

#### Testing this Sample
+ In the [Dialogflow console](https://console.dialogflow.com), from the left navigation menu > **Integrations** > **Integration Settings** under Google Assistant > Enable **Auto-preview changes** >  **Test** to open the Actions on Google simulator. **OR**
+ Type `Talk to my test app` in the simulator, or say `OK Google, talk to my test app` to Google Assistant on a mobile device associated with your Action's account.

### References
+ Questions? Go to [StackOverflow](https://stackoverflow.com/questions/tagged/actions-on-google), [Assistant Developer Community on Reddit](https://www.reddit.com/r/GoogleAssistantDev/) or [Support](https://developers.google.com/actions/support/).
+ Actions on Google [Documentation](https://developers.google.com/actions/extending-the-assistant)
+ [Examples from Google] (https://developers.google.com/actions/samples/github) using Node.js or Java backend
+ More info about deploying [Java apps with App Engine](https://cloud.google.com/appengine/docs/standard/java/quickstart).
+ More info about creating clean [AppEngine maven projects] (https://cloud.google.com/appengine/docs/standard/java/tools/maven)
+ Information about [Dialogflow SDK](https://dialogflow.com/docs/sdks)

### License
See [LICENSE](LICENSE).
 
### Terms
Your use of this sample is subject to, and by using or downloading the sample files you agree to comply with, the [Google APIs Terms of Service](https://developers.google.com/terms/).
