# ReferralBot
Integrated An Amazon Lex Chatbot With Aws Lambda , Whatsapp Messenger , Creating A Responsive Conversational Interface

![Gif](https://github.com/Kiran090303/ReferralBot/assets/98480971/fd702e8c-b677-4aee-a256-cb06b79cef40)

 
We All Are Tackling From This Question Every Day:-

+ Applying for a new job with a referral?
+ But , Not knowing how to ask for a referral?
+ Irritated to write the same referral message again and again?

Think of a WhatsApp bot, where you only need to give the details of the Name of the person, Job ID, company name, past experience, achievements, to get a personalized referral message.

Goals to achieve the necessary Output:
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
1. Create a Lambda function.
2. Create a bot.
3. Build and test the bot.
4. Integrate with Whatsapp.

**Step1 — Create a Lambda function**
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------

- Sign in to the AWS Management Console and open the AWS Lambda console at https://console.aws.amazon.com/lambda/
- Choose to Create function.
- Select Author from scratch.
- Type the name ReferralGenerator.
- For the Runtime, choose the latest version of Node.js.
- For the Role, choose Create new role from templates.
- Enter a new role name EventRole.
- Choose Create function.
  
<img width="683" alt="one" src="https://github.com/Kiran090303/ReferralBot/assets/98480971/712a601a-38c2-4712-aa45-d36c6032d0e3">

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------
- Test the Lambda Function Using Sample Event Data.
- On the function page, in the list of test events, choose Configure test events.
- Choose Create new test event,In the Event name field, enter a name for the event Test.
- Choose to Create.
- Choose Test and Lambda runs your Lambda function.

<img width="827" alt="two" src="https://github.com/Kiran090303/ReferralBot/assets/98480971/f9cb1fdb-a792-4ae8-bdac-60b06beb2fd0">

**Step 2 — Create a bot**
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------

- Go to services console, type lex and select Amazon Lex.
- Select Get Started and then select Create.
- On the Create your Lex bot page, choose Custom bot.

<img width="947" alt="three" src="https://github.com/Kiran090303/ReferralBot/assets/98480971/56ccae20-9975-4824-8f99-dc8a8fcc8347">

- App name: ReferralBot
- Output voice: Salli
- Text Only
- Session timeout: 5 minutes.
- Keep the remaining fields as default ones and COPPA to No.
- Select Create.

Now, create the ReferralBot intent , an action that the user wants to perform, with the minimum information needed. You add slot types for the intent and then configure the intent later.

- In the Amazon Lex console choose Create new intent.
- In the Create intent dialogue box, type the name of the intent referralBotIntent, and then choose Add.
- To create slot types
- In the left menu, choose the plus sign (+) next to Slot types.
- Create according.
- Give some sample utterances. For this, you can give start so that all the slots which you entered will be asked in line.
- In Lambda initialization and validation Leave the default setting.
- In Confirmation prompt, you can Leave the default setting or provide a confirmation string.
- In Fulfillment Choose AWS Lambda function and select the earlier created ReferralProcessor lambda function.
- Choose ok to the Add permission to Lambda function dialog box.
- Leave None selected.

**Step 3 — Build and test the bot**
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

- To build the ReferralBot bot, choose Build.
- It can take some time to complete the build.
- In the Test Bot window, start communicating with your Amazon Lex bot.
- After testing if your bot works fine click the publish button.
- Select Alias BETA.

**Step 4 — Integrating with WhatsApp**
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

-> Create an account on Twilio.
-> Verify your account.
-> After all verifications, you will be asked few questions.
-> Which Twilio product are you here to use? WhatApp
-> What do you plan to build with Twilio? Contact center
-> How do you want to build with Twilio? With code
-> Click on continue

- Activate your sandbox by accepting terms and conditions.
- Now you need to send a whatsapp message to the given number with the code mentioned.
- Click on next send a one-way messaging.
- You can send a dummy message to your whatsapp by click on make request.
- Click on the Node js code and save the Account Id and auth token. If you couldn’t find it there, open settings and there you go.
- Click on next.
- Open AWS Lex, and click on publish, and go to channels. On the left side, you can find Twilio SMS.
- Give all the details, and Account SID, Auth key with the values which you saved earlier.
- Click on activate, you will get a endpoint URL. Paste that in Twilio sandbox.
- Paste that in this field: When a message comes in, and click on save.
- Now go to whatsapp and start your conversation with Bot!!

  ![13](https://github.com/Kiran090303/ReferralBot/assets/98480971/2fd7cf50-7de0-410f-ba0c-d3374504b273)

