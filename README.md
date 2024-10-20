## PR Review Process

### Code Quality Checking :
### 1. **Variable/Function/Class/Interface Names**
- **Good Practice:** Use descriptive names to enhance readability.
  - **JavaScript:** `let userFirstName = "John";`
  - **.NET:** `public class UserProfile { public string FirstName { get; set; } }`
  
- **Bad Practice:** Use ambiguous or abbreviated names.
  - **JavaScript:** `let fn = "John";`
  - **.NET:** `public class U { public string f; }`

### 2. **Error Handling**
- **Good Practice:** Use structured error handling.
  - **JavaScript:** 
    ```javascript
    try {
        // code that may throw an error
    } catch (error) {
        console.error(error);
    }
    ```
  - **.NET:**
    ```csharp
    try {
        // code that may throw an exception
    } catch (Exception ex) {
        LogError(ex);
    }
    ```
  
- **Bad Practice:** Use unhandled exceptions or console logs.
  - **JavaScript:** `// no try/catch`
  - **.NET:** `catch { /* ignore */ }`

### 3. **Function Name**
- **Good Practice:** Use verbs and be descriptive.
  - **JavaScript:** `function fetchUserData() {}`
  - **.NET:** `public void SaveUser() { }`
  
- **Bad Practice:** Use vague names.
  - **JavaScript:** `function doStuff() {}`
  - **.NET:** `public void Process() { }`

### 4. **Function Size**
- **Good Practice:** Keep functions short and focused.
  - **JavaScript:** 
    ```javascript
    function calculateArea(radius) {
        return Math.PI * radius * radius;
    }
    ```
  - **.NET:** 
    ```csharp
    public double CalculateArea(double radius) {
        return Math.PI * radius * radius;
    }
    ```
  
- **Bad Practice:** Functions that do too much.
  - **JavaScript:**
    ```javascript
    function handleUserData(user) {
        // fetch data, validate, save, log
    }
    ```
  - **.NET:**
    ```csharp
    public void ProcessUser(User user) {
        // multiple operations mixed
    }
    ```

### 6. **Coding Consistency**
Maintain consistency throughout the codebase in terms of style and conventions.

### 7. **Code Duplication**
- **Good Practice:** Avoid duplicate code by creating reusable functions or components.
  - **JavaScript:** 
    ```javascript
    function calculateTax(amount) { return amount * 0.2; }
    ```
  
- **Bad Practice:** Copying and pasting code in multiple places.
  - **JavaScript:**
    ```javascript
    let tax1 = amount1 * 0.2;
    let tax2 = amount2 * 0.2; // Duplication
    ```

### 8. **Proper Log Handling**

**Good Practice:** Use logging libraries and define log levels.

**.NET Example:**
```csharp
 logger.Information("User with ID {UserId} fetched successfully", userId);
```

**Bad Practice:** Use `Console.WriteLine` for everything.

**.NET Example:**
```csharp

 Console.WriteLine("Debug info: User fetched with ID " + userId);

```

### 9. **Type Definition**
- **Good Practice:** Use type definitions for clarity (TypeScript or strong typing in .NET).
  - **JavaScript:** 
    ```typescript
    interface User { name: string; age: number; }
    ```
  - **.NET:** 
    ```csharp
    public class User { public string Name { get; set; } public int Age { get; set; } }
    ```
  
- **Bad Practice:** Avoid typing; use any or dynamic types.
  - **JavaScript:** `let user: any;`
  - **.NET:** `dynamic user;`

### 10. **Security**
Address security vulnerabilities, including SQL injection, password management, and API key protection.

### 11. **Proper Interface**
- **Good Practice:** Use interfaces to define contracts.
  - **JavaScript:** 
    ```typescript
    interface IUserService { getUser(id: number): User; }
    ```
  - **.NET:**
    ```csharp
    public interface IUserService { User GetUser(int id); }
    ```
  
- **Bad Practice:** Directly using classes without interfaces.
  - **JavaScript:** `class UserService { /* implementation */ }`
  - **.NET:** `public class UserService { /* implementation */ }`

### 12. **Proper Module Maintain**
Organize code into well-defined modules for easier maintenance.


### 13. **Browser and Device Compatibility**
- **Good Practice:** Test across multiple browsers and devices.
  - **JavaScript:** Use tools like BrowserStack.
  
- **Bad Practice:** Assume all users use the same browser.
  - **JavaScript:** `if (window.navigator.userAgent === "Chrome") { /* code */ }`


### 14. **Using Appropriate Fonts**
Follow guidance of figma 

### 15. **Image Form CDN**
- **Good Practice:** Use CDNs for optimized image loading.
  - **JavaScript:** `<img src="https://cdn



