# Code Smells

## 1. God Object, src/todo.js
**Where:** src/todo.js, lines 2-121 (class TodoManager)

**Smell:** God Object. TodoManager is doing too many jobs. It stores tasks, saves them to localStorage, validates new tasks, changes task data, and also renders the page.

**Cost:** This makes the class harder to change because many unrelated parts of the app depend on the same class. A change to storage or rendering could accidentally affect task logic.

**Not yet fixing:** noted for Week 3.


## 2. Long Method, src/todo.js
**Where:** src/todo.js, lines 80-120 (render method)

**Smell:** Long Method. The render method does many different things, including building HTML, finding the oldest task, adding button events, showing the flash effect, and changing the page title.

**Cost:** The method is harder to read and debug. Changing one part of the page could accidentally affect another part of the rendering.

**Not yet fixing:** noted for Week 3.


## 3. Long Parameter List, src/todo.js
**Where:** src/todo.js, lines 124-140 (buildTaskRow function)

**Smell:** Long Parameter List. The buildTaskRow function takes six parameters: id, desc, completed, priority, createdAt, and showActions.

**Cost:** It is easy to pass the arguments in the wrong order, and adding more task information later would make the function even harder to use.

**Not yet fixing:** noted for Week 3.