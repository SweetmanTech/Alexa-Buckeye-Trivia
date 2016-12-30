# Alexa-Buckeye-Trivia
A trivia application for the Ohio State University students

1) Open Amazon Developer Console (found here: https://developer.amazon.com/)
2) Select Alexa in top bar then click “Get Started”
3)  “Add a New Skill”
4) You should be redirected to the Skill Information page. This page allows you to give your alexa skill a name which will be seen in app store and in Alexa app (must be unique) and an Invocation Name which is the nickname users call your app when you want it to be launched. Name both of these whatever you would like. 
5) Paste the IntentSchema.json file (found in SpeechAssets folder of Github repository) in “Intent Schema” section of page. The intent schema section is used to connect the Sample Utterances to the AWS Lambda server function in json format.
6) Next, click “Add slot type” and create a new slot with name “LIST_OF_ANSWERS” and values “1,2,3” (line-seperated). These values are referenced in the javascript code so modification of these slots may affect the skill usability. Once you have added the new slot, copy the text from SampleUtterances.txt (found in SpeechAssets folder of Github repository) to the Sample Utterances section.
7)  Now we are on the “Configuration” page and need the AWS Lambda function address from our node.js function. We will get the AWS Lambda ARN in the next step
8) Open the AWS Console (https://console.aws.amazon.com/console/home?region=us-east-1). Make sure your location is set to “N. Virginia”. Then  select “Lambda”
9) “Create a Lambda Function”
10) Select “Configure Triggers” On left menu bar. Then click the dotted box and select Alexa Skills Kit. Click “next”
11) Create a name for your function, set  “runtime” to “Node.js 4.3”, and paste index.js (found in SpeechAssets folder of Github repository) in “Lambda Function Code”
12) Below, copy information for “Lambda function handler and role” from the screenshot.
13) “Next”
14) “Create Function”
15) Copy the ARN at top of the page 
16) Paste the ARN in the correct field and click “Next”
17) Done run code using personal Alexa-enabled device or using the online simulator found here: https://echosim.io/welcome?next=%2F

Hope you enjoyed the tutorial! Please let me know if you have any questions or comments!
