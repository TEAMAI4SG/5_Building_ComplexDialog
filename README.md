# 05. 🛠️ Building a Complex Dialog
## 💻 BUS 118i Digital Innovation

---
## 📖 Introduction

In the last few assignments, you have learned how to create a basic chatbot that can answer questions (Lab 1: Watson Assistant HelloWorld) and a chatbot that can ask questions (Lab 3: Using Watson Assistant to Interview Users). You also learned how to create a chatbot interviewer by yourself (Lab 4: Create Your Own Chatbot Interviewer)!

In this assignment, you are going to build a chatbot with a more complex dialog. This will prepare you with the basic skills to build chatbots for your team projects.

---

## 🎯 Goals

By the end of the assignment, you will be able to:

- Plan a dialog
- Define custom intents
- Add dialog nodes that can handle your intents
- Add entities to make your responses more specific
- Add a pattern entity, and use it in the dialog to find patterns in user input
- Set and reference context variables

---

## ⏱️ Estimated time
- This assignment takes about **60-90** minutes to complete.

---

## ⚠️ Keep in mind: 

While walking through the tutorial, you will make a few tests on your chatbot. You will take screenshots in this step.

- [Test 1: Test the #about_restaurant dialog node](https://cloud.ibm.com/docs/watson-assistant?topic=watson-assistant-tutorial#tutorial-test-about-intent)
- [Test 2: Test the menu option node](https://cloud.ibm.com/docs/watson-assistant?topic=watson-assistant-tutorial#tutorial-test-menu-options-intent)
- [Test 3: Test order cancellation](https://cloud.ibm.com/docs/watson-assistant?topic=watson-assistant-tutorial#tutorial-test-cancel-order)
- [Test 4: Test personalization](https://cloud.ibm.com/docs/watson-assistant?topic=watson-assistant-tutorial#tutorial-test-personalize)
- [Test 5: Test the chatbot from your web integration](https://cloud.ibm.com/docs/assistant?topic=assistant-tutorial#tutorial-integrate-assistant)

---

## 🚶‍♀️Steps

You will follow the [tutorial](https://cloud.ibm.com/docs/watson-assistant?topic=watson-assistant-tutorial) to create a restaurant reservation chatbot. Assuming that you have all the skills in the past few weeks, you do **NOT** need to go to the [prerequisite](https://cloud.ibm.com/docs/watson-assistant?topic=watson-assistant-tutorial), you can directly start with [Step 1.](https://cloud.ibm.com/docs/watson-assistant?topic=watson-assistant-tutorial#tutorial-plan)

Here are some hints for each step:

## 🔍 Step 1: 
This section just shows details about the assignment. Please read so you understand what you will be doing. 

## 🍽️ Step 2: Answer the questions about the restaurant.

1. **Please begin with the skill you previously created.** To do so: 

- Log into cloud.ibm.com

- In the top search bar, type in **Watson Assistant** and click on the assistant you previously made under **“Resource Results”**, **NOT “Catalog Results”**. For example, if your Watson Assistant was named Watson Assistant-t8 click on that one. 

![Picture 1](screenshots/Picture1.png)

- Click **Launch Watson Assistant**, create a new assistant. 

- Navigate to **Assistant Settings** and click on **Activate Dialog**.

- Click on the **Content Catalog** tab on the left, and add the **General** skill. (Click on **Add content** +). 

- Click on the **Dialog** tab and add the **#General_Greetings** node below the **Welcome** node. 

- Add another node **below** the **#General_Greetings** node. This node should be the **#about_restaurant** intent you made. **Note:** If you have not yet made the #about_restaurant intent, please follow Step 2 on the [tutorial](https://cloud.ibm.com/docs/assistant?topic=assistant-tutorial)


![Picture 2](screenshots/Picture2.png)


- After completing Step 2, continue the lab from the “Add a dialog node that is triggered by the #about_restaurant intent” section.

---

## 📋 Step 3: Answer questions about the menu

1. Add a #menu intent (Steps 1-5)
- **NO DISCREPANCIES**

2. Add a dialog node that is triggered by the #menu intent (Steps 1-12)
- **NO DISCREPANCIES**

3. Add a @menu entity (Steps 1-16)

- Step 1: Click the **Entities** tab, click **My Entities**, then click **Create Entity**

![Picture 3](screenshots/Picture3.png)

- Step 9: Click **Recommended synonyms**, then click the checkbox for **vegan.**
- Step 11: Click the empty **Type a synonym** field, then add plants-only and vegan diet.

4. Add child nodes that are triggered by the @menu entity types

- Step 4: When looking up @menu:standard, IBM Watson may just show **standard** in the drop down. Select that.
- Step 8: When looking up @menu:vegetarian, IBM Watson may just show **vegetarian** in the drop down. Select that.
- Step 12: When looking up @menu:cake, IBM Watson may just show **cake** in the drop down. Select that.

---

## 🎂 Step 4: Manage cake orders

1. Step 1: Click Entities and then “My Entities”. Then select “Create entity”

![Picture 4](screenshots/Picture4.png)

2. Step 5: Add **“order_syntax”** under **Value**.

3. Add dialog nodes that can manage requests to cancel an order

- Step 9: Add **“Ask for order number”** in the “Enter node name” field.
- Step 23: Add **“Number provided”** in the “Enter node name” field.
- Step 32: In the **“Then assistant should”** section, choose “Jump to”
- Step 33: Select **“If assistant recognizes (condition)”. Note:** the image below is simply showing which “jump to” option to select and no other aspects of this lab.
- Step 36: In the “Then assistant should” section select “Skip user input”.


![Picture 5](screenshots/Picture5.png)

## 🙋‍♀️  Step 5: Add the personal touch
1. Add the user name to the greeting

**a. 📐Step 6: Your final set up should look like this. Note: The second blank in the “If assistant recognizes” column should be left blank.**

![Picture 6](screenshots/Picture6.png)

**Reminder:** While walking through the tutorial, you will make a few tests on your chatbot. You will take screenshots in this step.

- [Test 1: Test the #about_restaurant dialog node](https://cloud.ibm.com/docs/watson-assistant?topic=watson-assistant-tutorial#tutorial-test-about-intent)

- [Test 2: Test the menu option node](https://cloud.ibm.com/docs/watson-assistant?topic=watson-assistant-tutorial#tutorial-test-menu-options-intent)

- [Test 3: Test order cancellation](https://cloud.ibm.com/docs/watson-assistant?topic=watson-assistant-tutorial#tutorial-test-cancel-order)
 
- [Test 4: Test personalization](https://cloud.ibm.com/docs/watson-assistant?topic=watson-assistant-tutorial#tutorial-test-personalize)

- [Test 5: Test the chatbot from your web integration](https://cloud.ibm.com/docs/assistant?topic=assistant-tutorial#tutorial-integrate-assistant)

When taking the screenshots, click on your account (on the top right) so that your name is shown with your testing. It is fine if your account information blocks part of your testing interface (see an example below). **Screenshots without your name will not be counted as valid.**


![Picture 7](screenshots/Picture7.png)


---

## 📝 Deliverables

A pdf document with
- your screenshots of Test 1-5 **(you need to include your name/account information in screenshots of Test 1-4);**
- the URL link of your chatbot in Test 5.

---

### 👏 Well done! You've wrapped up a key milestone in building smarter, more personalized chatbots.


