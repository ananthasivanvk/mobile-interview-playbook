## **iOS, App lifecycle**

In iOS, the **app lifecycle** refers to the sequence of states an app goes through from launch to termination, and the methods provided by the system to respond to these transitions. These lifecycle methods are primarily handled in the **AppDelegate** (or **SceneDelegate** for multi-scene apps introduced in iOS 13).

Here’s a breakdown of the key lifecycle states and their corresponding methods:

***

### **1. App Launch**

*   **`application(_:didFinishLaunchingWithOptions:)`**
    *   Called when the app has finished launching.
    *   Use this to set up initial configurations, load resources, and prepare the UI.

***

### **2. Active State**

*   **`applicationDidBecomeActive(_:)`**
    *   Called when the app moves to the foreground and becomes active.
    *   Ideal for restarting tasks paused when the app was inactive.

***

### **3. Inactive State**

*   **`applicationWillResignActive(_:)`**
    *   Called when the app is about to move from active to inactive (e.g., incoming call or home button press).
    *   Pause ongoing tasks or disable timers.

***

### **4. Background State**

*   **`applicationDidEnterBackground(_:)`**
    *   Called when the app enters the background.
    *   Save user data, release shared resources, and store enough state to restore the app later.

***

### **5. Foreground Transition**

*   **`applicationWillEnterForeground(_:)`**
    *   Called when the app is transitioning from background to foreground.
    *   Undo changes made when entering the background.

***

### **6. Termination**

*   **`applicationWillTerminate(_:)`**
    *   Called when the app is about to terminate.
    *   Save data if needed.

***

### **SceneDelegate Methods (iOS 13+)**

For apps using multiple scenes:

*   **`sceneDidBecomeActive(_:)`**
*   **`sceneWillResignActive(_:)`**
*   **`sceneDidEnterBackground(_:)`**
*   **`sceneWillEnterForeground(_:)`**

***


### **General iOS & Swift Basics**

1.  **Difference between `struct` and `class`?**  
    Struct = value type, Class = reference type; classes support inheritance.

2.  **Value vs reference types?**  
    Value types copy data; reference types share the same instance.

3.  **What is optional?**  
    A variable that can hold `nil`. Use `?` and unwrap with `if let` or `guard`.

4.  **`let` vs `var`?**  
    `let` = constant, `var` = mutable variable.

5.  **What is a protocol?**  
    A blueprint of methods/properties; similar to interface.

***
