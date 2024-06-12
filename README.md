# Taco-Recipe-Finder

**Description:**
Taco Town Recipe Finder is a web application that allows users to explore detailed recipes for various taco types. Users can choose from chicken, beef, or fish tacos and receive a detailed breakdown of ingredients and preparation methods.

**Implementations:**

1. **Server Setup:**
   - **Express.js:** The server is set up using Express.js, a minimal and flexible Node.js web application framework.
   - **Static Files:** `app.use(express.static("public"))` serves static files like CSS from the public folder.

2. **Body Parsing:**
   - **body-parser:** `bodyParser.urlencoded({ extended: true })` is used to parse URL-encoded data from user inputs, allowing the server to handle form submissions.

3. **Routes:**
   - **GET Route:** `app.get("/")` renders the main page (`index.ejs`), which includes buttons for selecting different taco recipes.
   - **POST Route:** `app.post("/recipe")` handles form submissions, parses the user's choice, and responds with the corresponding taco recipe.

4. **Data Handling:**
   - **JSON Data:** Taco recipes are stored in a JSON format within the server code. When a user selects a taco type, the server parses the JSON to retrieve the relevant recipe data.

5. **Dynamic Rendering:**
   - **EJS Templating:** The application uses EJS (Embedded JavaScript) templates to dynamically render HTML content based on the selected recipe. This includes displaying the name of the recipe, its ingredients, and preparation methods.

6. **User Interface:**
   - **HTML and CSS:** The user interface consists of a simple HTML form with buttons for selecting taco types. CSS is used for styling, ensuring a visually appealing and user-friendly experience.
   - **Dynamic Content Display:** When a user selects a taco, the recipe details are dynamically displayed without refreshing the page, enhancing the user experience.

**Example Flow:**
1. A user visits the main page and sees buttons for chicken, beef, and fish tacos.
2. The user clicks a button (e.g., chicken).
3. A POST request is sent to `/recipe` with the user's choice.
4. The server processes the request, retrieves the corresponding recipe from the JSON data, and renders the recipe details using EJS.
5. The recipe details are displayed on the page, showing ingredients and preparation steps.

This project demonstrates the integration of Express.js for server-side logic, body-parser for handling user inputs, JSON for data storage, and EJS for dynamic content rendering.
