// Install Next.js by running the following command first:
// npx create-next-app textile-sample-book

// Replace the default code in the Next.js project with the following:

// 1. pages/index.js (Landing Page)
export default function Home() {
  return (
    <div>
      <header>
        <h1>Welcome to Textile Sample Book</h1>
        <p>Your trusted partner for premium textile samples.</p>
        <a href="/products">Explore Products</a>
      </header>
    </div>
  );
}

// 2. pages/about.js (About Page)
export default function About() {
  return (
    <div>
      <header>
        <h1>About Us</h1>
        <p>We specialize in creating high-quality textile sample books to showcase your products in the best light.</p>
        <p>Our mission is to help businesses in the textile industry stand out with elegant and professional sample solutions.</p>
      </header>
    </div>
  );
}

// 3. pages/products.js (Products Page)
export default function Products() {
  const products = [
    { id: 1, name: "Cotton Samples", description: "Premium cotton textile samples." },
    { id: 2, name: "Silk Samples", description: "Elegant silk textile samples." },
    { id: 3, name: "Wool Samples", description: "Warm and soft wool textile samples." },
  ];

  return (
    <div>
      <header>
        <h1>Our Products</h1>
        <ul>
          {products.map((product) => (
            <li key={product.id}>
              <h2>{product.name}</h2>
              <p>{product.description}</p>
            </li>
          ))}
        </ul>
      </header>
    </div>
  );
}

// 4. pages/contact.js (Contact Us Page)
export default function Contact() {
  return (
    <div>
      <header>
        <h1>Contact Us</h1>
        <form>
          <label htmlFor="name">Name:</label>
          <input type="text" id="name" name="name" required />

          <label htmlFor="email">Email:</label>
          <input type="email" id="email" name="email" required />

          <label htmlFor="message">Message:</label>
          <textarea id="message" name="message" required></textarea>

          <button type="submit">Submit</button>
        </form>
        <p>Email: info@textilesamplebook.com</p>
        <p>Phone: +123-456-7890</p>
      </header>
    </div>
  );
}

// 5. styles/global.css (Add global styles for basic styling)
/* styles/global.css */
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

div {
  padding: 20px;
  text-align: center;
}

header h1 {
  color: #333;
}

header a {
  text-decoration: none;
  color: white;
  background-color: #0070f3;
  padding: 10px 20px;
  border-radius: 5px;
}

header a:hover {
  background-color: #005bb5;
}

ul {
  list-style: none;
  padding: 0;
}

ul li {
  margin: 10px 0;
  border: 1px solid #ddd;
  padding: 10px;
  border-radius: 5px;
}

form {
  display: flex;
  flex-direction: column;
  align-items: center;
}

form label {
  margin: 10px 0 5px;
}

form input, form textarea {
  margin-bottom: 10px;
  padding: 10px;
  width: 100%;
  max-width: 400px;
}

form button {
  background-color: #0070f3;
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
}

form button:hover {
  background-color: #005bb5;
}
