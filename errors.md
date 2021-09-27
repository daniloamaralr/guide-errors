# Errors and Solutions Angular

- ./src/app/app.module.ts:6:0-74 - Error: Module not found: Error: Can't resolve './services/side-nav/side-nav.component' in 'C:\Users\d.amaral.ribeiro\Documents\projects\new-menu-now\src\app'
  - check app.modules.ts to see if the declarations compeonents is correct
 
--- 
- Property 'showSideNav' has no initializer and is not definitely assigned in the constructor.
  - Just go to tsconfig.json and set
  ```
    "strictPropertyInitialization": false
  ```
---

- Error: src/app/components/side-nav/side-nav.component.html:12:50 - error TS2345: Argument of type 'boolean | null' is not assignable to parameter of type 'boolean'. 
  Type 'null' is not assignable to type 'boolean'.
   -
   
---

- error: 'src/app/components/' does not have a commit checked out
- error: src refspec main does not match any
  -If you have a subdirectory with a .git directory and try to git add . you will see this message. This can happen if you have a git repo and then create/clone another repo in a subdirectory under that repo.
  - You don't need to delete the entire file from the directory as the first answer suggests, I just had to delete the .git directory, and then your git add . will work This happens for the reason @Mario Zigliotto suggested, there is another repo in a subdirectory under that repo. 
  - to fix: steps to add and commit files
