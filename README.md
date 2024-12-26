# **Chat Application**

## **Project Overview**

This is a **real-time chat application** built using **Firebase** to handle user authentication, data storage, and media uploads. The app supports features like user registration, login, storing user profiles, chats, messages, and chat images. It integrates Firebase Storage to upload user avatars and media within chat messages.

---

## **Features**

- **Firebase Authentication**: Secure login and registration using email/password.
- **Firestore Database**: Stores user details, chat histories, and messages.
- **Firebase Storage**: Upload and store avatars and images for chat messages.
- **Real-time Chat**: Send and receive messages in real-time.
- **User Profiles**: Upload, view, and change avatars.
- **Blocking Mechanism**: Block/unblock users from chatting.

---

## **Tech Stack**

- **Frontend**: (React, Angular, etc.)
- **Backend**: Firebase (Firestore, Authentication, Storage)
- **Database**: Firebase Firestore
- **Storage**: Firebase Storage

---

## **Entity Relationship Diagram (ERD)**

### **Entities**

1. **users**  
   Stores user details:
   - **id** (string, PK): Unique identifier for the user.
   - **username** (string): Display name.
   - **email** (string): User’s email.
   - **avatar** (string): URL of the user's avatar stored in Firebase Storage.
   - **blocked** (array of strings): List of blocked users.

2. **chats**  
   Stores chat information:
   - **id** (string, PK): Unique identifier for the chat.
   - **createdAt** (date): Timestamp when the chat was created.
   - **messages** (array of objects): List of messages in the chat.

3. **userChats**  
   Stores user-chat relationships:
   - **id** (string, PK): Unique ID for the user-chat relationship.
   - **chats** (array of objects): Contains details about chats a user is part of.
     - **chatId** (string): Chat's ID.
     - **senderId** (string): Sender's user ID.
     - **receiverId** (string): Receiver's user ID.
     - **text** (string): Text content of the message.
     - **image** (string): Image URL (optional).
     - **createdAt** (date): Timestamp of the message.
     - **lastMessage** (string): Most recent message in the chat.
     - **updatedAt** (date): Timestamp when the message was last updated.
     - **isSeen** (boolean): Whether the message has been read.

---

## **Installation**

### **Step 1: Clone the Repository**

```bash
git clone https://github.com/your-username/chat-app.git
cd chat-app
