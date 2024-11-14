## Bio

- 👋 Hi, I’m Hưng, Innovative Software Engineer
- 👀 I am a passionate and experienced Senior Front End Developer specializing in creating responsive, high-performance web and mobile applications. With over 10 years of expertise, I excel in:

- Frontend Technologies: Proficient in ReactJS, React Native, NextJS, Material UI, Tailwind, Bootstrap, Element UI and modern front-end technologies.
- Backend Technologies: NodeJS, Express, MongoDB and modern back-end technologies.
- State Management: Redux, Redux Saga, Redux Toolkit and other state management tools.
- Unit Test: Jest and Cypress Testing.
- UI/UX Design: Skilled in transforming UI designs into functional, accessible front-end components using tools like Sketch, Zeplin, and Figma.
- Performance Optimization: Experienced in optimizing rendering and data flow to enhance application performance.
- Tools & Practices: Knowledgeable in Git for version control, Docker, CI/CD, and Agile methodologies.
- Industry Experience: Background in sectors like Education, E-commerce, Fitness, Finance, Healthcare and Logistics, providing domain-specific solutions.

I am committed to delivering high-quality, maintainable code that follows industry best practices. Let’s collaborate to bring your projects to life!

### Working on Demos: 
- [https://dev-showcase-peach.vercel.app](https://dev-showcase-peach.vercel.app)
  
  Technical Stack
  - Frontend: ReactJS Typscript with Material-UI for building a responsive and modern user interface.
  - Backend: Node.js, Express, Typscript and MongoDB for handling server-side logic and API endpoints.
  - State Management: Redux Saga, Redux Toolkit, Context API, RTK Query for managing cart state and interactions.
  - Utilities: Various utility functions for formatting and data handling.

### API Documentation: 
- [https://server-node-typescript.vercel.app/docs](https://server-node-typescript.vercel.app/docs)

 Note: Due to Vercel’s server limitations on free accounts, certain features such as clustering, websocket, SocketIO and load balancing cannot be applied…

How to Use the Demo

	1. Browse the Price Table: View detailed product information in the price table.
	2. Add Items to Cart: Select a plan and click the “Add to Cart” button. If you are not logged in, you will be prompted to authenticate. After logging in, your selected items will appear in the cart section.
	3. View and Manage Cart: Click on the cart icon to view the cart’s contents and remove items.
	4. Take the Node.js Quiz: Navigate to the quiz section to test your knowledge and learn more about Node.js.
 	5. Interact with Authentication: Use the login and signup forms to create a new account or log into an existing one. Try out the current authentication features and suggest improvements.

### Demo Description

Overview

This demo highlights an advanced e-commerce application featuring a dynamic price table, user authentication, and a fully functional shopping cart. Users can add, update, and delete cart items seamlessly. The integration of Stripe enables secure checkout for a smooth purchasing experience. This prototype serves as a robust foundation for ongoing enhancements, ensuring that each aspect of the application will improve over time, catering to user needs and evolving e-commerce standards. It serves as a foundation for a more comprehensive application with advanced features to be added in future updates.

Current Features

	1. Price Table:
	 • A comprehensive table displaying various products with detailed information including paper size, price, quantity, and business day.
	 • Styled table cells for a clean and user-friendly interface.
	2. Add to Cart:
	 • Users can add items to the cart directly from the price table and the need for authentication.
	 • Real-time updates of cart contents displayed with a badge indicating the number of items in the cart.
	 • Dynamic handling of item quantities with an interactive number input field.
	 • Ability to remove items from the cart seamlessly, with the cart updating instantly to reflect changes.
	3. Node.js Quiz:
	 • An engaging quiz section designed to test users’ knowledge of Node.js.
	 • A variety of questions to challenge users and help them learn more about Node.js fundamentals and advanced topics.

Features Done

	1. Apply Authentication:
	 • Implement user authentication to secure the cart and checkout processes.
	 • Provide personalized user experiences with account-specific cart data.

	2. Update Cart:
	 • Enable users to update item quantities directly within the cart. 
	 • Automatically calculate and display the total price based on updated quantities.

  	3. Checkout Cart (Planned Enhancements again):
	 • Integrate a secure and user-friendly checkout process with Stripe Payment.
	 • Support for various payment methods to facilitate seamless transactions.

	4. Apply State Management:
	 • Integrate Redux Saga, Redux Toolkit and RTK Query.

	6. Redis has added
	 • Enabled get prices API
  	 • Enabled get carts API (Disabled)

	7. Cypress Test for APIs
	 • Login API

Features To-Do (Planned Enhancements)

	5. More Features:
	 • Wishlist functionality to allow users to save items for later.
	 • Order history tracking for users to view past purchases.
	 • Enhanced UI/UX improvements for a more intuitive and enjoyable shopping experience.

Test Payments with Stripe Test Card

	Use the following Stripe test card details for testing payments:

	• Card number: 4242 4242 4242 4242
	• Expiry: Any valid future date
	• CVC: Any 3 digits

 	Card number			Scenario								How to test
	4242 4242 4242 4242		The card payment succeeds and doesn’t require authentication.		Fill out the credit card form using the credit card number with any expiration, CVC, and postal code.
	4000 0025 0000 3155		The card payment requires authentication.				Fill out the credit card form using the credit card number with any expiration, CVC, and postal code.
	4000 0000 0000 9995		The card is declined with a decline code like insufficient_funds.	Fill out the credit card form using the credit card number with any expiration, CVC, and postal code.
	6205 5000 0000 0000 004		The UnionPay card has a variable length of 13-19 digits.		Fill out the credit card form using the credit card number with any expiration, CVC, and postal code.

	This will simulate a successful payment when you submit the form.

Features Improvement (Planned Enhancements but cannot apply these by limitation from Vercel Server)

	2. Real-Time “Update Cart” Using WebSocket and Socket.IO: The “Update Cart” feature will be enhanced to support real-time updates of the total price using WebSocket technology, specifically with the integration of Socket.IO. This improvement will allow for a seamless and instantaneous update of the cart’s total price across all connected clients as soon as any changes occur in the cart’s contents, such as item quantity adjustments.
	


Key Enhancements:

	1. Real-Time Price Synchronization:
	 • The total price of the cart will now be updated in real-time whenever a user modifies the quantity of any item in the cart. This ensures that all users connected to the same session or cart will see the updated total price instantly without needing to refresh the page.
	2. Persistent WebSocket Connection:
	 • A persistent WebSocket connection will be established between the client and server, enabling continuous two-way communication. This connection will be maintained using Socket.IO, which provides reliable event-based communication over WebSocket.
	3. Immediate Feedback and Error Handling:
	 • Users will receive immediate feedback when they update item quantities, including any errors that might occur, such as attempting to set a quantity lower than allowed. This real-time interaction improves the user experience by ensuring that all changes are reflected instantly and accurately.
	4. Scalability and Efficiency:
	 • The WebSocket-based approach is designed to be scalable, allowing multiple users to interact with the cart simultaneously while ensuring that all views of the cart remain consistent and up-to-date. This method also reduces the need for frequent server polling, enhancing overall performance.
	5. Automatic Recalculation and Database Synchronization:
	 • Whenever an item is added, removed, or its quantity is changed, the server will automatically recalculate the cart’s total price and update the value in the MongoDB database. This ensures that the stored data always reflects the current state of the cart.

Implementation Overview:

	• Server-Side: The server will listen for cart update events (e.g., item quantity changes) via WebSocket. Upon receiving an update, the server will recalculate the total price, update the cart in the database, and broadcast the updated cart data to all connected clients.
	• Client-Side: Clients will establish a WebSocket connection upon loading the cart. Any changes made to the cart by any user will trigger a real-time update, ensuring that all users have a synchronized view of the cart, including the updated total price.

### Working on Demos: 

- [https://nextjs-showcase-lake.vercel.app](https://nextjs-showcase-lake.vercel.app)
 
  Technical Stack
  - Frontend: NextJS Typscript with Material-UI for building a responsive and modern user interface.
  - Backend: Node.js, Express, Typscript and MongoDB for handling server-side logic and API endpoints.
  - State Management: Redux Saga, Redux Toolkit, Context API, RTK Query for managing cart state and interactions.
  - Utilities: Various utility functions for formatting and data handling.


- 🌱 I’m currently learning Python, PostgreSQL
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...



- Code Sandbox: https://codesandbox.io/u/hungnm11
- Codepen : https://codepen.io/hungnm11

<!---
hungnm11/hungnm11 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
