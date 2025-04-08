# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
Make the webpage responsive using media queries.
Ensure proper alignment and spacing.

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.

Happy Coding! 💻✨

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Pauline's Responsive Design Example</title>
  <style>
    /* General Reset */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    /* Basic Layout */
    body {
      font-family: Arial, sans-serif;
      line-height: 1.6;
    }

    header {
      background-color: #333;
      color: white;
      padding: 1rem;
    }

    nav ul {
      display: flex;
      justify-content: space-around;
      list-style: none;
    }

    nav ul li {
      margin: 0 10px;
    }

    nav ul li a {
      color: white;
      text-decoration: none;
      font-size: 1.1rem;
    }

    footer {
      background-color: #333;
      color: white;
      text-align: center;
      padding: 1rem;
      position: fixed;
      bottom: 0;
      width: 100%;
    }

    /* Flexbox Layout for Main Content */
    .main-content {
      display: flex;
      justify-content: space-between;
      padding: 2rem;
    }

    .left, .center, .right {
      padding: 1rem;
    }

    .left, .right {
      flex: 1;
      background-color: #f4f4f4;
    }

    .center {
      flex: 2;
      background-color: #e2e2e2;
    }

    h2 {
      font-size: 1.5rem;
      margin-bottom: 1rem;
    }

    /* Media Queries for Responsiveness */
    @media (max-width: 768px) {
      .main-content {
        flex-direction: column;
        align-items: center;
      }

      .left, .right {
        flex: none;
        width: 100%;
        background-color: #f4f4f4;
      }

      .center {
        width: 100%;
        background-color: #e2e2e2;
      }

      nav ul {
        flex-direction: column;
      }

      nav ul li {
        margin-bottom: 10px;
      }
    }

    @media (max-width: 480px) {
      header {
        text-align: center;
      }

      nav ul {
        padding: 0;
      }

      footer {
        position: relative;
      }
    }
  </style>
</head>
<body>
  <header>
    <nav>
      <ul class="nav-links">
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Services</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>
  </header>

  <main class="main-content">
    <section class="left">
      <h2>Left Sidebar</h2>
      <p>Content for the left sidebar.</p>
    </section>
    <section class="center">
      <h2>Main Content</h2>
      <p>This is the main content area.</p>
    </section>
    <section class="right">
      <h2>Right Sidebar</h2>
      <p>Content for the right sidebar.</p>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 Pauline's Website</p>
  </footer>
</body>
</html>

