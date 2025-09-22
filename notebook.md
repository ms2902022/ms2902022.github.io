# My Coding Notebook

## Day 1
## Table of Contents
- [Flutter Notes](#flutter-notes)
  - [What is Flutter?](#what-is-flutter)
  - [Key Terms and Definitions](#key-terms-and-definitions)
  - [Definitions with Structures](#flutter-definitions-with-structures)
  - [Layout and Design Widgets](layout-and-design-widgets)
- [Code Definitions](#code-definitions)
- [Notebook Style Guide](#markdown-style-guide-for-coding-notebooks)

## Flutter Notes

### What is Flutter?
- Definition: A framework made by google for building apps that work on web, Android, and IOS-- with one codebase.
- Why is it useful? Saves time and money by having multiple different ways to utilize the app.

---

### Key Terms and Definitions

| Term             | Definition                                      | Example / Notes                          |
|------------------|--------------------------------------------------|-------------------------------------------|
| Widget           | Basic nuilding block of a flutter App. Everything is a widget|Text, Image Container, Column  |
| MaterialApp      | The root of the app. Sets up routes and themes.  | Found in main.dart                        |
| Scaffold         | provides basic visual layout -- like a header, body, floating button | Each screen uses it   |
| StatelessWidget  | A widget that doesn't change                     |Most of the screen files                   |
| StatefulWidget   |A widget that changes over time                   | Used in MyHomePage()                      |
| Navigator        | manages screen transitions                       | Navigator.pushNamed(context, '/page2' )    |
| AppBar           | Top navigation bar                               | Navigator.pushNamed(context, '/page1') |
| Column           |        vertical layout                           |                                           |
| Row              |    horizontal layout                             |                                           |
| Container        |   wraps content with padding, margin, or color   |                                           |
| Text             |       displays text                              |                                           |
| Image.network    |     displays images from a IRL                   |                                           |
| Padding          |     adds space around a widget                   |                                           |
| Center           |     centers its child                            |                                           |

---

### Layout and Design Widgets
- How do you center a widget?
- How do you align something to the left or right?
- What widget adds space around content?


## Flutter Definitions with structures

| Term | Definition and Description | Base Structure | Real Life Example | App Example |
|------|----------------------------|----------------|-------------------|-------------|
|main()| A function that runs when your app starts. It tells Flutter what app to show. | `void main() => runApp(MyApp());` |Turning on a phone|main.dart, void main() => runApp(MyPortfolioApp());|
|MaterialApp| The widget that sets up your whole app’s look and navigation. | `MaterialApp(...)` |Setting up a social media page|main.dart, return MaterialApp(debugShowCheckedModeBanner: false,title: 'TSA Portfolio',theme: ThemeData(, and more|
|Scaffold| A widget that gives you the basic layout: background, navigation bar, floating button, etc. | `Scaffold(...)` |Templetes (these notes)|showcase.dart, return Scaffold(body: Column(mainAxisAlignment: MainAxisAlignment.start,children: [|
|Column| A widget that holds and displays your content in a straight line from top to bottom. | `Column(...)` |Keep related content in order (these notes)|showcase.dart,  child: Column(children: [|
|Row| A widget that shows things side-by-side. | `Row(...)` |Keep related content in order (these notes)|infocard.dart,  child: Row(children: [|
|Container| A box that holds other widgets. You can add color, padding, borders, or size. | `Container(...)` |Designing a template on canva|infocard.dart, return Container margin: const EdgeInsets.symmetric(vertical: 8, horizontal: 16),padding: const EdgeInsets.all(12),decoration: BoxDecoration(|
|Text| A widget to display text on the screen. | `Text('Hello')` |Reaing articles from news outlets online|infocard.dart,  child: Text(description,style: const TextStyle(color: Colors.white),|
|Image.network| A widget to show an image using a link from the internet. | `Image.network('https://...')` |Google images|infocard.dart, child: Image.network(imageUrl, width: 100, height: 100, fit: BoxFit.cover),),|
|ElevatedButton| A clickable button that floats above content. You choose what happens when it's clicked. | `ElevatedButton(onPressed: ..., child: ...)` |A key on a keyboard y7ou programmed outputs your character|showcase.dart,  ElevatedButton(onPressed: () => Navigator.pushNamed(context, '/alt'),child: const Text('Alternate Design'),|
|onPressed| The code that gets run when a button is tapped or something happens. | `onPressed: () => doSomething()` |A key on a keyboard outputs a character|showcase.dart, onPressed: () => Navigator.pushNamed(context, '/alt'),child: const Text('Alternate Design'),|
|StatelessWidget| A class that creates widgets that never change. Good for static screens. | `class HomeScreen extends StatelessWidget` |A profile picture|infocard.dart, StatelessWidget {final String imageUrl;final String description;|
|StatefulWidget| A class for widgets that can change while the app is running. | `class MyWidget extends StatefulWidget` |Game graphics on a screen|Not Applicable|
|Navigator| Lets you move from one screen to another using route names. | `Navigator.pushNamed(context, '/about')` |Navigation through a website| onPressed: () => Navigator.pushNamed(context, '/alt'),child: const Text('Alternate Design'),|
|Padding| Makes space around a widget inside its container. | `Padding(padding: EdgeInsets.all(8.0), child: ...)` |Packing Peanuts| Padding(padding: const EdgeInsets.only(left: 100.0),child: Column(children: [|
|Center| Aligns content in the center of the screen or container. | `Center(child: ...)` |App title (thats in the center)| body: Center(child: Column(|
|Wrap| Automatically puts widgets onto a new line when there's no space. | `Wrap(children: [...])` |Writing in a doc wraps to the next line| Wrap(alignment: WrapAlignment.center, children: puppyUrls.map((url) => puppyImage(url)).toList()),ElevatedButton(onPressed: () => Navigator.pushNamed(context, '/alt'),child: const Text('Alternate Design'),|
|@override| This marks a method as one that’s replacing a method in a parent class. | `@override` |Updating a website|@overrideWidget build(BuildContext context) {final List<Map<String, String>> dogInfo = [{|
|build()| The special function in every widget that describes what gets drawn on the screen. | `Widget build(BuildContext context) {...}` |Having a blueprint for a project|Widget build(BuildContext context) {return Scaffold(body: Center(|
|build| Required in every widget class to describe what to show. | `build` |Printing out a design|Widget build(BuildContext context) {return Scaffold(body: Center(|
|BuildContext| A variable that helps the widget know where it is and lets it communicate with the app. | `BuildContext context` |Typing and hitting undo|Widget build(BuildContext context) {return Scaffold(body: Center(|
|super.key| A keyword used to pass a value to the parent widget. | `super.key` |Sending an email|super.key,required this.imageUrl,required this.description,});|
|Const| A keyword that means the value won't change and is set once. | `const` |Title of a homescreen, won't change|const InfoCard({super.key,required this.imageUrl,required this.description,});|









| Term | Definition | Base Structure / Syntax | Real Life Example | App Example |
|------|------------|--------------------------|-------------------|-------------|
|Variable| A named container used to store a value that may change. | `var x = 5;` |Amount of water in a watterbottle|main.dart, string title: TSA Portfolio|
|Constant| A fixed value that cannot change once set. | `const PI = 3.14;` |Apps title, font, etc.|main.dart, const MyPortfolioApp({super.key});|
|Data Type| The kind of value a variable holds, like numbers or text. | `int`, `String`, `bool` |Processing text from a book|main.dart, bool,debugShowCheckedModeBanner:false,|
|String| A sequence of characters used to represent words or text. | `"Hello World"` |Sentences|main.dart,  title: 'TSA Portfolio',|
|Integer| Whole number values. | `int age = 16;` |Clock||
|Double| Number values with decimals. | `double age = 16.2;` |Calculator|main.dart, isplayLarge: TextStyle(fontSize: 36, color: Colors.white, fontWeight: FontWeight.bold),bodyLarge: TextStyle(color: Colors.white),|
|Boolean| A value that can be true or false. | `bool isLoggedIn = false;` |Human movement||
|List| A collection of values in a specific order. | `List<String> names = [];` |Individuals Info.||
|Null| A special value that means “nothing.” | `String? name = null;` |Not knowing a username||
|Function| A reusable block of code that performs an action. | `void sayHi() { print("Hi"); }` |Jumping in a game||
|Parameter| The information passed into a function to change how it works. | `greet(String name)` |Bank information (account #)||
|Return| The result a function gives back. | `return total;` |Making a deposite, recipt in return ||
|Scope| Where a variable or function can be used. | (No set syntax — concept-based) |Kite (wind/outside)|  |
|Class| Blueprint for creating objects with specific structure and behavior. | `class Dog {}` |Waterbottles, computers, dogs, (everything!)|  |
|Object| A specific version of a class. | `Dog myDog = Dog();` |Computers,cars,pens,  created in the same model and make,|  |
|Property| A variable that belongs to a class/object. | `String name;` |Everyone has a name, but they are specific to each person|  |
|Method| A function that belongs to a class. | `void bark() {}` |Waterbottle = Drinking water, Teacher = teaches|  |
|Constructor| A special function used to set up a class when it’s created. | `Dog(this.name);` |Baby is born =  defealt gender, doc = defealt settings|  |
|Abstraction| Hiding the inner workings of code so users only interact with what they need. | (Concept — not specific code) |Hiding complex translation (keyboard, binary, etc.)|  |
|Override| Changing how a built-in or inherited function behaves. | `@override` |Changing print statements to make it more useable (waterbottleABC123 = waterbottle, blue, # volume)|  |
|Void| A function that does not return a value. | `void printMessage() {}` |Teacher speaking - no return|  |





































## Markdown Style Guide for Coding Notebooks

Follow this guide to keep your coding notebook **clear, consistent, and professional**.  
This ensures your notes are easy for you (and others) to read later.

---

## 🔹 Headings
**When to use:** Organize your notebook into sections (like days, topics, or projects).  
- `#` for the notebook title (use once at the top).  
- `##` for each day or major topic.  
- `###` for subsections (like "Notes", "Practice", "Reflections").  

✅ Example:


# My Coding Notebook
## Day 1
### Notes
### Practice
🔡 Text Formatting
When to use: Highlight important ideas or add emphasis.

Use bold for key terms or definitions.

Use italic for emphasis or side comments.

Use inline code for keywords, functions, or commands.

✅ Example:

**Class** = a blueprint for objects  
*Remember:* always test your code  
Use `System.out.println()` to print

💻 Code Blocks
When to use: Anytime you write multiple lines of code.

Inline code for short snippets.

Fenced code blocks with language for full examples.

✅ Example:

```java
public class Hello {
    public static void main(String[] args) {
        System.out.println("Hello World!");
    }
}
```
🧾 Lists
When to use: Organize steps, notes, or key points.

Numbered lists for sequences or steps.

Bulleted lists for unordered ideas.

✅ Example:

1. Define the class
2. Write the main method
3. Test your program

- Variables
- Loops
- Conditionals
✅ Checklists
When to use: Track progress on assignments or tasks.

✅ Example:

- [x] Complete coding warm-up
- [ ] Finish project draft
- [ ] Reflect on learning

      
➡️ Blockquotes
When to use: Call out notes, reminders, or teacher comments.

✅ Example:

> 💡 Remember: Loops repeat code until a condition is false.
📊 Tables
When to use: Compare values, track progress, or organize data neatly.

✅ Example:

| Task        | Status   | Notes          |
|-------------|----------|----------------|
| Homework 1  | Done ✅  | Submitted      |
| Homework 2  | Pending  | Needs review   |
🔗 Links & Images
When to use: Add references, resources, or visuals.

✅ Example:

[Java Docs](https://docs.oracle.com/javase/8/docs/api/)  
![Markdown Logo](https://upload.wikimedia.org/wikipedia/commons/4/48/Markdown-mark.svg)
📂 Collapsible Sections
When to use: Hide solutions, extended notes, or extra details.

✅ Example:

<details>
  <summary>Click to reveal solution</summary>
  
System.out.println("Answer: 42");

</details>
📝 Footnotes
When to use: Add references or side notes without cluttering the page.

✅ Example:

This concept is related to object-oriented programming.[^1]

[^1]: See "Objects and Classes" in your textbook.
🎯 Style Rules
Consistency matters more than creativity

Always use headings to structure your notes.

Always use code blocks for multi-line code.

Clarity first

Bold key terms.

Use lists instead of long sentences when outlining steps.

Professional tone

Don’t mix casual notes with formal work in the same section.

Use blockquotes for reflections or teacher feedback.

Track your learning

Use checklists to mark what’s done.

Use collapsible sections if you want to hide answers until review time.

✅ Bottom Line:

Headings = Structure

Bold/Italic = Emphasis

Code blocks = Code

Lists = Steps/Ideas

Tables = Organization

Checklists = Progress

Blockquotes = Notes/Tips

Collapsible = Hide/Show detail

Keep it simple, consistent, and clear.
## Day 2 
Notes for day 2
