# CartCompanion Proposal Overview

## 1. Introduction:

Grocery shopping is an activity that is done by everyone at least once a week. It is a task that plays an important role in maintaining daily life. Despite it being a common task, it still remains insufficient for most of the shoppers due to several problems. These problems are: missing price tags, forgetting important items, overspending and experiencing difficulty in searching for products. These issues can cause inconveniences and negatively affect a shopper’s experience.

As time goes by, people find ways to make life easier for them. Grocery shopping is also included. Shoppers seek efficiency, convenience, and cost-effectiveness when shopping. Using handwritten notes or relying on memory are no longer suitable for today's age. As technology has been integrated into everyday life, we can use it to create solutions to better our experiences.

This project aims to address these issues by developing a system that is designed to enhance shopping experiences of shoppers. The system will help shoppers with an integrated barcode scanner, advanced shopping list, AI-Technology, and price tracker.

Overall, this project highlights the importance of improving grocery shopping experiences of people. By creating software that uses modern technology, the goal is to make tasks more efficient, convenient, and most importantly, user-friendly.

## Problem Statement:

Grocery shopping is a common activity that is essential for daily living, yet it is still often inefficient and frustrating. A lot of supermarkets have some price checkers located at random places in the supermarket, however it is tedious to locate the price checkers to check the prices of some products. Additionally, some shelves are missing price tags which makes the shoppers confused and become hesitant about buying an item. Another challenge for most shoppers is the awareness of spending. Shoppers only discover their total expenses at the counter which makes it difficult for most to avoid overspending. These problems could potentially make shoppers frustrated and increase the chances of them making mistakes.

Together, these challenges make grocery shopping more time-consuming, disorganized, and costly than it needs to be. Addressing them presents an opportunity to improve the shopping experience by enhancing list organization, minimizing forgotten or repeated items, and enabling real-time budget tracking for smarter purchasing decisions.

## 2. Objectives/Purpose

Based on the identified problem statement, CartCompanion aims to achieve the following objectives:

### Primary Objectives:

- **Real-time Expense Tracking**: Provide instant cost calculation and budget monitoring through barcode scanning technology
- **Intelligent List Management**: Create dynamic, organized shopping lists with automatic categorization and product suggestions
- **Purchase History Analytics**: Generate insights from shopping patterns to optimize future shopping experiences
- **Personalized Recommendations**: Implement AI-driven suggestions based on user preferences, dietary restrictions, and purchase history

### Secondary Objectives:

- **User Experience Enhancement**: Develop an intuitive, user-friendly interface that reduces shopping time and stress
- **Budget Optimization**: Help users make cost-effective purchasing decisions through price tracking and deal notifications
- **Shopping Pattern Analysis**: Provide statistical insights to help users understand and improve their shopping habits

The purpose of our application is to make grocery shopping easier and more organized for everyday consumers. CartCompanion helps people:

- **Track their spending in real-time** - Users can see exactly how much money they are spending as they shop, helping them stay within their budget
- **Organize their shopping lists better** - The app automatically sorts items by category and keeps everything in one place
- **Get smart product suggestions** - Using AI technology, the app recommends products based on what users usually buy and their preferences
- **Save time while shopping** - By scanning barcodes, users can quickly add items to their list and get product information without searching manually
- **Learn from their shopping habits** - The app shows users their spending patterns and helps them make better shopping decisions
- **Never forget important items** - Smart reminders help users remember frequently bought products and essentials

## Platform Information:

We're going to make this as a mobile app because everyone has smartphones and can use the camera to scan barcodes while they're shopping. A mobile platform makes sense since people need to check prices right when they're in the store, so a website or computer program wouldn't work for this situation. We're using Dart and Flutter to build the app so it works on both iPhones and Android phones with the same code, which makes development easier and faster. For the backend, we're using Python Firebase to handle user accounts, store data in real-time databases, and run cloud functions that can scale up when lots of people use the app at once. The main AI feature comes from Google ML Kit's Barcode Scanning API, which gives us reliable barcode recognition that works even without internet connection and processes scans instantly.

**User Description:**
CartCompanion is designed for a diverse group of grocery shoppers who seek convenience, organization, and efficiency in their shopping routines. The target users include everyday consumers, busy professionals, students, and parents who want to save time, manage budgets effectively, and avoid forgetting essential items. Since the app is mobile-based, it is suitable for users across all age groups who own smartphones. The interface will be intuitive and user-friendly, ensuring that even those with limited technical skills can navigate it with ease.

**User Capabilities:**

- Create and manage digital shopping lists directly on their smartphones
- Scan product barcodes to retrieve price and product information instantly
- Track expenses in real-time while shopping to avoid overspending
- Receive personalized product recommendations based on history and preferences
- Review purchase history and gain insights from shopping analytics
- Navigate the app easily due to its simple, modern, and intuitive design

## Specific Requirements:

1. **Barcode Scanning and Product Recognition System**
   CartCompanion’s barcode scanning feature serves as the main method for quickly identifying products during shopping. By leveraging the device camera with Google ML Kit’s Barcode Scanning API, users can instantly capture barcodes and retrieve product information. The system will support common formats such as UPC-A, EAN-13, and QR codes, ensuring wide compatibility. Upon a successful scan, product details such as name, brand, and estimated price will be displayed to the user. For items not found in the database, users can enter details manually. To improve speed, successful lookups will be cached locally, allowing faster recognition in future scans.

2. **Dynamic Shopping List Management System**
   The shopping list management module allows users to create, categorize, and manage their shopping lists efficiently. Items can be added either by scanning a barcode or through manual entry, and the system automatically organizes them into categories such as Produce, Dairy, Meat, and Pantry. Each item is displayed with its name, quantity, and estimated cost, giving shoppers a structured and clear view of their needs. Users can also update quantities, mark items as completed, remove entries, and reorder items using simple interactions. Lists remain persistent across sessions to ensure continuity and organization.

3. **Real-time Budget Tracking System**
   Budget awareness is a core feature of CartCompanion. Before starting a shopping trip, users can set spending limits, and the app will continuously track expenses as items are added to the list. Real-time calculations update totals instantly, while visual indicators (green, yellow, and red zones) provide clear insights into how close the user is to their budget limit. Alerts will be triggered when spending nears or exceeds the set budget. Additionally, the system estimates taxes and displays the remaining balance to help users make informed financial decisions during shopping.

4. **Purchase History and Analytics System**
   CartCompanion records completed trips and stores them as purchase histories, allowing users to review and analyze past shopping behaviors. Each record includes the date, total amount spent, and the list of purchased items. From this data, the system generates basic analytics such as weekly and monthly spending summaries, average cost per trip, and frequently purchased items. Visual charts and simple statistics help users recognize trends, optimize their shopping habits, and make smarter purchasing decisions. Data is stored locally for privacy, though cloud integration may be considered in future versions.

5. **AI-Powered Recommendation Engine**
   The recommendation system enhances shopping efficiency by suggesting products tailored to user preferences and history. Using Firebase Genkit, the engine will analyze purchase patterns, item combinations, and seasonal trends to generate personalized suggestions. Recommendations will be delivered in multiple contexts, such as suggesting frequently bought items when creating a list, highlighting complementary products while shopping, or offering “You might also need” prompts based on current selections. Over time, the system adapts based on user feedback, becoming more accurate and relevant to individual preferences while maintaining privacy and responsiveness.

6. **User Profile and Settings Management**
   To create a personalized shopping experience, CartCompanion includes a user profile and settings system. Shoppers can define dietary restrictions, budget defaults, and preferred notification styles, which the app will apply automatically in future sessions. Profiles also allow the system to filter recommendations in line with health preferences and shopping behaviors. Users can customize interface options, store frequently visited supermarkets, and adjust units of measurement. These personalized settings ensure that the app feels intuitive and aligned with the unique needs of each user.

**Technical Specifications**
The app will be developed using Flutter with Dart to support both iOS and Android platforms with a single codebase. The backend will be powered by Python Firebase for authentication, data storage, and cloud scalability. Barcode scanning will rely on Google ML Kit, while SQLite will provide local storage for histories and preferences. The AI recommendations will be handled through Firebase Genkit, ensuring secure, scalable, and adaptive machine learning integration. All operations will be optimized to respond within two seconds, with core features designed to function even without internet connectivity. Personal data will be processed locally where possible to prioritize user privacy.
