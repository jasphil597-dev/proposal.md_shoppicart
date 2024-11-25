## Project-Proposal_shoppicart

---

#### Objective

To build a simple online grocery shopping platform where users can browse, add, update, and remove items from their shopping cart. Users will be able to sign up, log in, and manage their cart via a web interface, with backend functionality provided by Express.js and MongoDB.

---

#### User Stories

##### 1. User Registration & Authentication

- As a user,

  - I want to be able to create an account by providing my email and password so that I can securely access and manage my shopping cart.

  - The user can sign up by entering an email, password, and confirming the password.
  - A hashed password is stored in the database.

- As a user,
  - I want to be able to log in using my credentials so that I can access my personalized shopping cart.
  - The user can log in with their email and password.
  - Invalid credentials return an error message.

2. Cart Management

- As a user,

  - I want to be able to view my shopping cart so that I can see all the items I’ve added to it before proceeding to checkout.
  - The user can view their cart with details like item name, quantity, price, and total cost.
  - The cart is associated with the user and persists between sessions using MongoDB.

- As a user,
  - I want to be able to add items to my cart so that I can start shopping for groceries.
  - The user can add an item to their cart with fields like name, quantity, and price.
  - The item is stored in the database with the user’s ID as a reference.
- As a user,
  - I want to be able to update the quantity or details of items in my cart to adjust my shopping list.
  - The user can modify the quantity or remove individual items from their cart or delete the entire item on the cart.

3. Authentication and Authorization

- As a user,

  - I want to be sure that only I can access my cart and manage my items, ensuring my data is private.

  - Access to the cart is restricted to authenticated users.

4. Backend & Data Modeling

- As a developer,

  - I want to define a user model and cart model to structure the data in MongoDB so that we can persist user information and their cart items efficiently.

---

#### API Endpoints

1. User Authentication:
   - POST /auth/signup: Register a new user.
   - POST /auth/login: Log in a user.
2. Cart Management:
   - GET /cart: Get the current user's cart.
   - POST /cart: Add an item to the user's cart.
   - PUT /cart/:itemId: Update an item in the cart.
   - DELETE /cart/:itemId: Remove an item from the cart.

---

![image](./Screenshot%202024-11-22%20at%204.55.21 PM.png)
![image](./Screenshot%202024-11-23%20at%209.59.26 PM.png)
![image](./Screenshot%202024-11-23%20at%209.59.13 PM.png)
![image](./Screenshot%202024-11-23%20at%209.58.50 PM.png)

---

#### Routing Table Example…

| HTTP Method (Verb) | Path/Endpoint/URI | CRUD Operation                 | Route Name | Has Data Payload? | Purpose | Render/Redirect Action |
| ------------------ | ----------------- | ------------------------------ | ---------- | ----------------- | ------- | ---------------------- |
| POST/GET           | /auth/signup      | Register a new user.           | create     | Yes               |
| POST/GET           | /auth/login       | Log in a user                  | show       | Yes               |         |                        |
| GET                | /cart             | Get the current user's cart    | show       |                   |         |                        |
| POST               | /cart             | Add an item to the user's cart | edit       | Yes               |         |                        |
| PUT                | /cart/:itemId     | Update an item in the cart     | show       | Yes               |         |                        |
| DELETE             | /cart/:itemId     | Remove an item from the cart   | Delete     | No                |         |                        |

---

#### Timeline - Daily Accountability

| Day                |     | Task                                   |     | Blockers                                     |     | Notes Thoughts |
| ------------------ | --- | -------------------------------------- | --- | -------------------------------------------- | --- | -------------- |
| Monday             |     | Create and present proposal Deployment |     | Finalize the proposal and submit thru github |
| Tuesday & Thursday |     | Create scaffolding                     |     |                                              |     |                |
| Friday             |     | Add functionality                      |     |                                              |     |                |
| Saturday - Sunday  |     | Create html, js, css files             |     |                                              |     |                |
| Monday             |     | MVP / Finalize fuctionality            |     |                                              |     |                |
| Tuesday            |     | Presentation Day                       |     |                                              |     |                |
