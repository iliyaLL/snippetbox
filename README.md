# snippetbox
A web application, which lets people paste and share their snippets - like GitHub's [Gists][1].

till chapter 10 - Server and Security Improvements

## Setup
### TLS certificate


## Routes Documentation

1. **GET /**
- **Description**: Displays the homepage of the application.
- **Handler**: `app.home`
- **Response**:
   - **Success**: Renders the homepage as an HTML page.

---

2. **GET /snippet/view/:id**
- **Description**: View a specific snippet by its unique ID.
- **Path Parameter**:
   - `:id`: The unique identifier of the snippet to view.
- **Handler**: `app.snippetView`
- **Response**:
   - **Success**: Renders a page showing the details of the specified snippet.
   - **Failure**: Returns a `404 Not Found` if the snippet does not exist.

---
- **Description**: Display a form to create a new snippet.

3. **GET /snippet/create**
- **Handler**: `app.snippetCreate`
- **Response**:
   - **Success**: Renders an HTML page with a form for creating a new snippet.

---

4. **POST /snippet/create**
- **Description**: Process the form submission to create a new snippet.
- **Handler**: `app.snippetCreatePost`
- **Request Body**:
   - The form data submitted for creating the snippet (fields depend on your form design).
- **Response**:
   - **Success**: Creates the snippet and redirects to its details page.
   - **Failure**: Returns validation errors or error messages if the submission is invalid.


## Tech
- Go (version go1.22.0 windows/amd64)
- MySql (Ver 8.0.36 for Win64 on x86_64)
- Web: HTML, CSS
- [HttpRouter][2] (routing)
- [Alice][3] (middleware chaining)

## Copyright and disclaimer
Let’s Go: Learn to build professional web applications with Go. Copyright © 2023 Alex Edwards.

[1]: https://gist.github.com/  "Gists"
[2]: https://github.com/julienschmidt/httprouter "HttpRouter"
[3]: https://github.com/justinas/alice "Alice"