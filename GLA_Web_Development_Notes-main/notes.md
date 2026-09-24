# Notes
## The Web vs. The Internet
People often use these terms interchangeably, but they are completely different layers of technology. Think of the Internet as the roads and the Web as the shops and houses built along those roads.1. The Web vs. The Internet

| Features  | The Internet | The World Wide Web   |
|-------|-----|--------|
| What is it? | A massive, global network of connected computers and servers.  | A collection of information and resources accessed via the Internet.  |
| Function | Provides the physical and routing infrastructure (cables, routers, Wi-Fi).  | Provides a way to link documents and media together using URLs and hyperlinks. |
| Protocols Used  | TCP/IP (Transmission Control Protocol / Internet Protocol).  | HTTP/HTTPS (Hypertext Transfer Protocol). |
| Examples  | Email, FTP, peer-to-peer file sharing, online gaming.  | Websites, web apps, search engines, social media feeds. |

## Websites vs. Web Applications

As the web has evolved, the line between these two has blurred, but there is still a core distinction based on interactivity.

- **Websites (Informational)**: Primarily designed for users to consume content. They are mostly static (or managed by a Content Management System like WordPress). You read an article, view a menu, or look at a company's contact page.
   
    - *Examples*: Wikipedia, a local restaurant's menu page, a news blog.

- **Web Applications (Interactive)**: Primarily designed for users to perform actions. They are dynamic, heavily rely on databases, and change based on user input. If you have to log in, create data, or manipulate things on the screen, it is likely a web app.
   
    - *Examples*: Gmail, Netflix, Google Docs, online banking portals.

## The Client-Server Model

The entire web operates on a continuous conversation called the Client-Server Model. This is a request-and-response cycle.

When you type a URL into your browser, a specific sequence occurs:

1. **The Request**: Your device (the client) asks the network, "Can I see the page at this address?"

2. **DNS Lookup**: The web uses a Domain Name System (DNS) to translate human-readable names (like google.com) into computer-readable IP addresses (like 142.250.190.46).

3. **The Processing**: The server at that IP address receives the request, gathers the necessary files or database information, and packages it up.

4. **The Response**: The server sends those files (HTML, CSS, JavaScript, images) back to the client.

## The Role of the Browser (The Client)
The browser (Chrome, Safari, Firefox) is the software running on the user's device. Its primary jobs are to:

- **Send Requests**: It formats your clicks and URL entries into proper HTTP requests.

- **Parse Code**: It receives raw code (HTML for structure, CSS for styling, JavaScript for interactivity) from the server.

- **Render the UI**: It translates that code into the visual, interactive webpage you actually see on your screen.

- **Manage State**: It stores cookies, cache, and local data to remember who you are and keep the experience fast.

## The Role of the Server (The Host)
A server is simply a powerful computer connected to the Internet 24/7, waiting for requests. Its primary jobs are to:

- **Listen & Verify**: It constantly listens for incoming HTTP requests and checks if the client is authorized to access the requested data (e.g., checking your login token).

- **Execute Logic**: For web apps, it runs backend code (Python, Node.js, Java) to calculate data, process payments, or update records.

- **Query the Database**: It fetches or saves permanent information (user profiles, post histories) to a database.

- **Serve Files**: It bundles the requested assets and sends them back over the Internet to the user's browser.

---
---
---

## The Client-Server Architecture
The web is fundamentally a massive conversation between two types of computers: Clients and Servers.

- **The Client**: The device and software requesting information. Most commonly, this is your laptop or phone running a web browser (like Chrome or Safari). The client is responsible for sending requests and rendering the received code into a visual interface.

- **The Server**: A powerful, specialized computer connected to the internet 24/7. Its job is to store files, databases, and application logic, listen for incoming client requests, and serve back the requested data.

### The Request-Response Cycle
When a client and server communicate, they follow a strict chronological sequence:

1. **Client Request**: The browser sends an HTTP request asking for a specific webpage or data.

2. **Server Processing**: The server receives the request, verifies it, executes any necessary backend logic, and fetches data from the database.

3. **Server Response**: The server sends back an HTTP response containing a status code and the requested files (HTML, CSS, JavaScript, JSON).

4. **Client Rendering**: The browser downloads these files and renders the webpage on the user's screen.

## URLs (Uniform Resource Locators)
A URL is a web address that tells the browser exactly how to access a resource and where it is located.

Structure Breakdown (Example:

`https://www.example.com:443/products/shoes?color=red#reviews)`:

`https://` **(Protocol)**: The set of rules used to transfer the data (usually HTTP or HTTPS for secure connections).

`www.` **(Subdomain)**: A subdivision of the main domain.

`example.com` **(Domain Name)**: The human-readable name of the website.

`:443` **(Port)**: The technical "door" the server listens on (usually hidden; 80 for HTTP, 443 for HTTPS).

`/products/shoes` **(Path)**: The exact location or file being requested on the server.

`?color=red` **(Query Parameters)**: Extra data sent to the server to filter or sort results, starting with a ? and separated by &.

`#reviews` **(Fragment/Anchor)**: Directs the browser to a specific section on the loaded page.

## HTTP: The Language of the Web
**HTTP (Hypertext Transfer Protocol)** provides the vocabulary for clients and servers to communicate.

### HTTP Methods (The "Verbs")
When a client makes a request, it uses a method to indicate the desired action:

**GET**: Read or retrieve data (e.g., loading a webpage).

**POST**: Create new data (e.g., submitting a form).

**PUT/PATCH**: Update existing data (e.g., changing a profile picture).

**DELETE**: Remove data (e.g., deleting a comment).

### HTTP Status Codes
The server replies with a 3-digit code summarizing the result of the request:

**1xx (Informational)**: Request received, continuing process.

**2xx (Success)**: The request was successful (e.g., 200 OK, 201 Created).

**3xx (Redirection)**: The resource has moved; further action needed (e.g., 301 Moved Permanently).

**4xx (Client Error)**: The client made a mistake (e.g., 400 Bad Request, 403 Forbidden, 404 Not Found).

**5xx (Server Error)**: The server encountered an error (e.g., 500 Internal Server Error).

## DNS: The Internet's Phonebook
Computers route traffic using numerical IP addresses (like `142.250.190.46`), not domain names. The Domain Name System (DNS) translates human-readable URLs into machine-readable IP addresses.

### The DNS Resolution Process
When you type a URL into your browser, the following steps occur to find the IP address:

1. **Cache Check**: The browser and operating system check their local memory to see if they recently saved the IP address for this domain.

2. **Recursive Resolver**: If not found locally, the query goes to your Internet Service Provider's DNS server (the resolver), asking it to track down the IP.

3. **Root Name Server**: The resolver queries the Root server, which acts as a directory. It directs the resolver to the correct Top-Level Domain server.

4. **TLD (Top-Level Domain) Server**: The resolver asks the TLD server (e.g., the server handling all `.com` or `.org` addresses), which then points to the specific authoritative server.

5. **Authoritative Name Server**: The resolver queries the final server responsible for the specific domain (e.g., `example.com`). This server provides the exact IP address.

6. **Connection**: The resolver returns the IP address to the browser, allowing the browser to finally initiate the HTTP Request directly to the correct web server.

---
---
---

## HTML
### Purpose of HTML
**HTML (HyperText Markup Language)** is the standard markup language used to structure content on the web. It uses a system of elements and tags to tell web browsers how to display text, images, links, forms, and other multimedia assets. HTML provides the structural skeleton of a webpage, while CSS handles styling and JavaScript adds interactivity.

### Basic Document Structure
Every standard HTML5 document follows a specific structural skeleton that ensures web browsers parse and render the page correctly.

- `<!DOCTYPE html>`: Declares the document type and informs the browser that this is an HTML5 document. It prevents the browser from entering "quirks mode."

- `<html>`: The root element that wraps all the content on the entire page. Usually includes a lang attribute (e.g., lang="en").

- `<head>`: The container for metadata. It holds information about the page (like title, character encoding, and stylesheets) that isn't directly rendered on the screen.

- `<body>`: The container for all visible content, including headings, paragraphs, images, videos, and interactive components.

``` HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document Title</title>
</head>
<body>
    <h1>Welcome to My Website</h1>
    <p>This is the visible body content.</p>
</body>
</html>
```

### The `<meta>` Tag & Attributes

The `<meta>` tag provides metadata about the HTML document. It is always placed inside the `<head>` section and is self-closing. Metadata is used by browsers (how to display content), search engines (SEO ranking and snippets), and social media platforms (preview cards).

| Purpose  | Code Example | Description   |
|-------|-----|--------|
| Character Encoding | `<meta charset="UTF-8">`  | Sets text encoding to prevent garbled characters.  |
| Responsive Viewport | `<meta name="viewport" content="width=device-width, initial-scale=1.0">`  | Essential for mobile responsiveness; scales the page to the device screen width.  |
| SEO Description | `<meta name="description" content="Learn HTML basics...">`  | Provides a summary displayed on search engine results pages (SERPs).  |
| Page Author | `<meta name="author" content="John Doe">`  | Declares the author or creator of the webpage.  |
| Auto-Refresh | `<meta http-equiv="refresh" content="60">`  | Automatically reloads the webpage every 60 seconds.  |

### Core HTML Syntax & Text Structure
Understanding how HTML is written at a foundational level is essential for building web pages.

- **Elements & Tags**: An HTML element is defined by a start tag, content, and an end tag.

    - *Opening Tag*: `<tagname>` (e.g., `<p>`)

    - *Closing Tag*: `</tagname>` (e.g., `</p>`)

    - *Self-Closing Elements*: Elements like images or line breaks don't need closing tags (e.g., `<br>`).

- **Attributes**: Provide extra information about an element and are always specified in the opening tag as `name="value"` pairs (e.g., `class="highlight"`).

- **Comments**: Used to leave notes in the code for developers; browsers ignore them completely.

    - Syntax: `<!-- This is a comment -->`

- **Headings (`<h1>` to `<h6>`)**: Define the hierarchical structure of a page. `<h1>` is the most important heading (usually the main title), while `<h6>` is the least important.

- **Paragraphs** (`<p>`): Used to wrap blocks of regular text content. Browsers automatically add space (margin) before and after a paragraph.

### The Anchor Element & Hyperlinks
The anchor element (`<a>`) creates hyperlinks, allowing users to navigate between web pages, files, email addresses, or specific locations on the same page.

```HTML

<a href="https://www.example.com" target="_blank" >Visit Example</a>
```
#### Key Attributes and Concepts
- `href` **(Hypertext Reference)**: Specifies the destination URL of the link.


- **Absolute vs. Relative URLs**:

    - *Absolute URL*: Points to a location on the external web using the full web address (e.g., [`https://www.google.com/about](https://www.google.com/about)`).

    - *Relative URL*: Points to a file within the same website structure (e.g., `/contact.html` or `images/logo.png`).

- `target` **Attribute**: Determines where to open the linked document.

    - `_blank`: Opens the link in a new browser tab or window.

    - `_self` (Default): Opens the link in the exact same tab.

### Images & The alt Attribute
The `<img>` element embeds an image into a webpage. It is a self-closing tag, meaning it does not have a closing `</img>` tag.

```HTML
<img src="images/sunset.jpg" alt="A vibrant orange sunset over the ocean mountains" width="600">
```
### Essential Attributes
- `src` **(Source)**: Specifies the path/URL to the image file you want to display.

- `alt` **(Alternative Text)**: Provides a textual description of the image. This is vital because:

    - It improves accessibility for screen readers used by visually impaired individuals.

    - It acts as a fallback if the image file fails to load or the user has broken internet.

    - It helps search engines index the image content (SEO).

- `width` and `height`: Define the dimensions of the image in pixels, helping prevent layout shifts while the page is loading.

### HTML Text Formatting Tags

| Tag  | Visual Effect | Semantic Meaning   |
|-------|-----|--------|
| `<b>` | **Bold**  | No extra importance (purely stylistic)  |
| `<strong>` | **Bold**  | Strong importance or urgency |
| `<i>` | *Italic*  | Alternate voice, foreign term, or thought |
| `<em>` | *Italic*  | Stress emphasis |
| `<sub>` | Subscript  | Subscript (chemical formulas) |
| `<sup>` | Superscript  | Superscript (math exponents, dates) |
| `<del>` | Strike through  | Deleted text / revision |
| `<ins>` | Underline  | Inserted text / revision |
| `<mark>` | Highlighted  | Highlighted reference text |
| `<small>` | Smaller  | Fine print or legal disclaimers |

### HTML Lists

#### Unordered Lists (`<ul>`)
Unordered lists group items where the precise sequence does not matter. Browsers typically render these with bullet points.

- **Syntax**: Wrap items in `<ul>` and individual rows in `<li>`.

- **Styling via CSS**: You can modify the marker style using `list-style-type` (e.g., `circle`, `square`, or `none`).

- **Common Use Cases**: Website navigation bars, feature highlights, and itemized shopping lists.

#### Ordered Lists (`<ol>`)
Ordered lists sequence items where the order matters, automatically numbering them.

- **Syntax**: Use `<ol>` containers with `<li>` children.

- **Key Attributes**:

    - `reversed`: Counts backwards from the starting number.

    - `start`: Specifies a custom starting integer (e.g., `start="5"`).

    - `type`: Changes numbering styles, such as uppercase letters (`A`), lowercase letters (`a`), roman numerals (`I`, `i`), or standard numbers (`1`).

- **Common Use Cases**: Step-by-step tutorials, recipes, and leaderboard rankings.

#### Description Lists (`<dl>`) and Nested Lists
Description lists handle metadata or key-value pairs rather than standard bullet or number sequences.

- **Elements**: Created using `<dl>` (description list), paired with `<dt>` (term) and `<dd>` (description definition).

- **Nested Lists**: You can nest any list type inside an `<li>` element of another list. This is standard practice for creating multi-level dropdown menus or indented outlines.

- **Common Use Cases**: Glossaries, FAQ sections, and hierarchical site maps.

[HTML File For Lists](./HTML/lists.html)

### Semantic Tags
### What is Semantic HTML?
Semantic HTML refers to using HTML tags that explicitly describe the meaning and purpose of the content inside them, rather than just how the content should look visually.

Non-semantic elements (e.g., `<div>`, `<span>`) tell the browser nothing about their content. Semantic elements (e.g., `<article>`, `<nav>`) inform the browser, screen readers, search engine crawlers, and other developers about the role of the enclosed content.

#### Primary Bnefits of Semantic Elements

1. **Accessibility (a11y)**: Screen readers use semantic landmarks (like `<main>` or `<nav>`) to allow visually impaired users to jump directly to key areas of a webpage without reading every line.

2. **Search Engine Optimization (SEO)**: Search engine bots parse semantic tags to determine page hierarchy, main content topics, and relationships between content blocks.

3. **Code Maintainability**: Replaces nested "div soup" with structured, easily readable code for developers.

#### Core Semantic Elements & Their Usage
`<header>`

Represents introductory content or a group of introductory/navigational aids for a page or section.

- **Common Contents**: Logos, site titles, search forms, author information, or global navigation links.

- **Scope Rules**: Can be used at the page level (site header) or inside `<article>` and `<section>` elements (section header).

- **Usage Restriction**: Cannot be nested inside `<footer>`, `<address>`, or another `<header>`.

`<nav>`

Defines a block of major navigation links.

- **Usage**: Intended for primary site navigation, tables of contents, pagination links, or breadcrumbs.

- **Best Practice**: Not all groups of links belong in `<nav>`. Secondary/utility links in a footer do not need a `<nav>` tag unless they represent major site navigation.

`<main>`

Represents the dominant, unique content of the `<body>` of a document.

- **Usage**: Contains blog posts, core features, form interfaces, or primary tools unique to that specific URL.

- Rules:

    - Must be directly relevant to the unique content of the page.

    - Should not contain content repeated across multiple pages (e.g., navigation bars, footers, copyright notices, sidebar utilities).

    - There should ideally be only one visible `<main>` element per document.

`<section>`

Represents a generic standalone section of a document that groups related content together by theme.

- **Key Characteristic**: Almost always includes a heading (`<h2>`–`<h6>`) as a child element to define the topic of that section.

- **Usage**: Used for chapters, tabbed layouts, numbered sections of a document, or distinct blocks on a landing page (e.g., "Features", "Pricing", "Testimonials").

- **Rule**: If you only need a container for styling or layout scripting, use a `<div>` instead of a `<section>`.

`<article>`

Represents a complete, self-contained composition that is independently reusable or redistributable.

- Key Characteristic: The content should make logical sense on its own if removed from the page context (e.g., if syndicated via an RSS feed).

- Usage: Blog posts, news articles, forum posts, user comments, product cards, or interactive widgets.

- Nesting: Articles can be nested inside articles (e.g., user comments nested inside a blog post article).

`<aside>`

Represents content that is indirectly or tangentially related to the main content surrounding it.

- **Usage**: Sidebars, pull quotes, callout boxes, related articles links, glossary terms, or advertising blocks.

- **Behavior**: When placed inside `<main>`, it relates specifically to the main topic. When placed outside `<main>`, it relates to the website as a whole.

`<footer>`

Represents the footer for its nearest sectioning element or for the document as a whole.

- **Common Contents**: Copyright information, terms of service links, privacy policies, author contact details, back-to-top links, or related document references.

- **Scope Rules**: Can be used at the page level (site footer) or inside individual `<article>` and `<section>` elements.

[HTML File For Semantic Tags](./HTML/semantic.html)

### Tables in HTML
#### Core HTML Table Elements

HTML tables are used to display tabular data (information organized in rows and columns).

- **`<table>`**: The root wrapper element that contains all table-related structural tags and data cells.

- **`<tr>` (Table Row)**: Container element defining a horizontal row of cells.

- **`<th>` (Table Header)**: Defines a header cell. Content inside <th> is bold and centered by default, carrying semantic weight for accessibility.

- **`<td>` (Table Data)**: Defines a standard data cell holding actual content (text, numbers, images, links). Text inside `<td>` is regular-weight and left-aligned by default.

#### Table Structural Sections

Dividing a table into logical semantic sections allows browsers, screen readers, and print engine tools to process table layouts efficiently (e.g., repeating header rows when printing across multiple pages).

**`<thead>` (Table Head)**
- Encloses the header row(s) containing column titles.

- Must contain one or more <tr> elements with <th> tags.

- Positioned at the top of the table structure.

**`<tbody>` (Table Body)**
- Encloses the primary content and data rows of the table.

- Contains `<tr>` elements housing `<td>` (and occasionally row `<th>`) tags.

- A single `<table>` can contain multiple `<tbody>` elements to visually or semantically separate groups of rows.

**`<tfoot>` (Table Foot)**

- Encloses summary rows, totals, averages, or disclaimer notes at the bottom of a table.

- Remains at the bottom of the rendered table regardless of its placement in the HTML source code, though standard practice places it after `<tbody>`.

#### Cell Spanning Attributes (colspan & rowspan)

By default, every cell occupies a single grid cell (1 X 1). The `colspan` and `rowspan` attributes allow a single cell to expand horizontally across multiple columns or vertically across multiple rows.

**`colspan` (Column Span)**
- **Syntax**: `<td colspan="N">` or `<th colspan="N">` where ***N*** is an integer.

- Expands the cell horizontally to occupy the width of **N** columns.

- **Layout Rule**: Subsequent `<td>` or `<th>` elements in that same row must be omitted to match the total column count.

**`rowspan` (Row Span)**
- **Syntax**: `<td rowspan="N">` or `<th rowspan="N">` where ***N*** is an integer.
- Expands the cell vertically to occupy the height of **N** rows.
- **Layout Rule**: Corresponding cells in subsequent rows directly beneath this cell must be omitted in HTML markup to prevent layout overflow.

#### Accessibility Best Practices

- **`<caption>`**: Placed directly after opening the `<table>` tag. Provides a title or brief summary of the table for screen reader users and search engines.

- **scope Attribute**: Added to `<th>` elements to explicitly state whether a header applies to a column (`scope="col"`) or a row (`scope="row"`). This ensures screen readers correctly announce context as users navigate cells.

[HTML File for Tables](./HTML/tables.html)

### HTML Forms Overview

An HTML form (`<form>`) is an interactive container used to collect user input and send that data to a server for processing (e.g., login, user registration, search, checkout).

#### Key Form Attributes
- `action`: Specifies the URL where the form data should be submitted upon sending.

- `method`: Specifies the HTTP method used to send the data:

    - `GET`: Appends form data to the URL as query parameters (e.g., ?search=shoes). Used for non-sensitive data retrievals like searches. Data is visible in the URL bar and has length limitations.

    - `POST`: Sends form data inside the HTTP request body. Used for submitting sensitive data (passwords) or modifying server data (registration, file uploads). Data is hidden from the URL bar.

#### Form Labels (`<label>`)

The `<label>` element represents a caption for an input control. It provides essential accessibility context for screen readers and expands the clickable touch/click target area for users.

**Two Ways to Associate Labels with Inputs**
1. **Explicit Association (Recommended)**

    Uses the for attribute on the label matching the id attribute on the input element:

    ```HTML
    <label for="user-email">Email Address:</label>
    <input type="email" id="user-email" name="email">
    ```

2. **Implicit Association (Nesting)**

    Wraps the input element inside the label tag directly:
    ```HTML
    <label>
    Email Address:
    <input type="email" name="email">
    </label>
    ```

#### Basic Input Controls (`<input>`)

The `<input>` tag is a self-closing element whose behavior changes dynamically based on its `type` attribute.

**Crucial Rule**: *The `name` attribute is required for an input's data to be included in the server payload upon form submission (`name=value` pair).*

**Text Inputs**
- `type="text"`: Standard single-line text input for general strings (names, addresses).

- `type="email"`: Specialized input for email addresses. Includes built-in browser format validation (@ and domain check) and triggers email-optimized keyboards on mobile devices.

-`type="password"`: Masked text input where characters are replaced with dots or asterisks to prevent shoulder surfing.

- `type="number"`: Input for numeric values only. Triggers numeric keypads on mobile screens.

    - Key Attributes: `min`, `max`, `step` (controls increments).

**Common Attributes for Text/Number Inputs**
- `placeholder`: Hint text displayed inside the field before a user types. (*Should not replace a* `<label>`).

- `value`: Sets the default or initial value of the input.

- `required`: Boolean attribute preventing form submission if the field is empty.

- `readonly`: Prevents users from modifying the field value while still submitting the data.

- `disabled`: Disables user interaction and excludes the field's data from form submission.

- `minlength` / `maxlength`: Sets character limits for text fields.

#### Choice Controls: Radios & Checkboxes
**Radio Buttons (`type="radio"`)**

Allows the user to select exactly one option from a mutually exclusive group.

- **Group Rule**: All radio inputs in the same group must share the same `name` attribute.

- **`value` Attribute**: Defines the unique value sent to the server when that option is selected.

- **`checked`**: Sets an option as selected by default.

```HTML
<p>Select your subscription tier:</p>

<input type="radio" id="free" name="plan" value="free" checked>
<label for="free">Free Tier</label>

<input type="radio" id="pro" name="plan" value="pro">
<label for="pro">Pro Tier ($10/mo)</label>
```

**Checkboxes (`type="checkbox"`)**

Allows the user to select zero, one, or multiple independent options.

- Unlike radio buttons, checkboxes sharing the same `name` attribute operate independently.
```HTML
<p>Select your interests:</p>

<input type="checkbox" id="coding" name="interests" value="coding" checked>
<label for="coding">Coding</label>

<input type="checkbox" id="design" name="interests" value="design">
<label for="design">Design</label>
```

#### Dropdown & Multi-Line Inputs

**Dropdown Menu (`<select>` and `<option>`)**

Creates a compact collapsible dropdown menu for selecting single or multiple options.

- `<select>`: The parent element requiring the `name` attribute.

- `<option>`: Individual selectable choices requiring a `value` attribute.

- `<optgroup>`: Groups related options under a non-selectable category label.

- Attributes:

    - **`selected`**: Pre-selects a specific option.

    - **`multiple`**: Allows users to select multiple options (usually by holding Ctrl/Cmd).

```HTML
<label for="country">Country:</label>
<select id="country" name="country">
  <option value="" disabled selected>Select a country</option>
  <optgroup label="North America">
    <option value="us">United States</option>
    <option value="ca">Canada</option>
  </optgroup>
  <optgroup label="Europe">
    <option value="uk">United Kingdom</option>
    <option value="de">Germany</option>
  </optgroup>
</select>
```

**Multi-Line Text Area (`<textarea>`)**

A multi-line text input field used for longer entries (comments, feedback, bios).

- **Opening and Closing Tags**: Requires both `<textarea>` and `</textarea>`.

- **Initial Value**: Placed between the tags, not in a `value` attribute.

**Attributes**:

`rows`: Defines visible text lines (height).

`cols`: Defines average character width.

CSS Control: Best resized using CSS (`width`, `height`, `resize: vertical`;).

```HTML
<label for="feedback">Your Feedback:</label>
<textarea id="feedback" name="feedback" rows="4" cols="50" placeholder="Type your comment..."></textarea>
```

#### Form Submission & Action Buttons

Buttons trigger form actions or run JavaScript functions.

**Preferred Tag: `<button>`**

The `<button>` element is flexible because it can contain text, HTML elements, or icons inside it.

- `type="submit"` **(Default)**: Submits the parent form data to the server.

- `type="reset"`: Clears all user entries in the form back to initial default values.

```HTML
<!-- Recommended Modern Buttons -->
<button type="submit">Submit Registration</button>
<button type="reset">Clear Form</button>
```

[HTML File for Forms](./HTML/Forms.html)

---
---
---
## CSS
### Introduction to CSS
**CSS (Cascading Style Sheets)** is the styling language used to control the presentation, layout, visual design, and user interface of web pages written in HTML.

- **Separation of Concerns**: HTML defines the structure and content, while CSS handles the design and layout.

- **Why "Cascading"?** When multiple CSS rules target the same HTML element, styles "cascade" down based on specific rules of precedence (origin, specificity, and source order) to determine which final styles get applied.

### Three Ways to Include CSS
CSS can be applied to an HTML document in three different ways depending on the scope and maintainability requirements of the project.

**1. Inline CSS**

Styles are applied directly to an individual HTML element using the `style` attribute.
**2. Internal CSS**

Styles are placed within a `<style>` tag inside the `<head>` section of a single HTML document.
**1. External CSS**

Styles are written in a completely separate file with a .css extension and linked to HTML documents via the `<link>` tag inside the `<head>`.

#### Order of Precedence (Cascade Rules)
1. Inline CSS
2. External & Internal CSS (Equal weight; if specificity is equal, the rule written last in code order wins)

### CSS Syntax Anatomy
A CSS rule consists of a Selector and a Declaration Block.

```CSS
selector {
  property: value;
  property: value;
}
```

### Basic CSS Selectors
Selectors determine which HTML elements will receive the styles defined in a declaration block.


**NOTE** : ***For CSS, Refer CSS Folder in the Githut repository***
