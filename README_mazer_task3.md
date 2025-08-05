1. Used the Mazer Admin Dashboard template
 *Started with the open-source Mazer Bootstrap 5 dashboard.

 *Worked directly inside the src/pages/index.html file.

2. Created and Used data.json File
  Added a data.json file in the project root.

  This file contains structured data:

  stats: Profile Views, Followers, Following, Saved Posts.

  regions: Europe, America, India, Indonesia.

  comments: User name, comment text, and profile image.

3. Loaded JSON Data Dynamically
   Used Nunjucks built-in function:
   {% set data = loadjson('data.json') %}
   This made JSON data accessible throughout the HTML file.

4. Replaced Hardcoded Text with Dynamic Bindings
   Replaced static values like:
   112.000
   with:
   {{ data.stats.profileViews }}
   Applied to:

   Profile Views

   Followers

   Following

   Saved Posts

5. Made Regional Visit Stats Dynamic
   Replaced numbers like 862, 375, etc. with:
   {{ data.regions.Europe }}
   {{ data.regions.India }}
6. Rendered Comments Using Loop
   Replaced static comment table rows with:
   {% for comment in data.comments %}
   Dynamically displayed:
   User avatar ({{ comment.image }})
   Name ({{ comment.name }})
   Comment text ({{ comment.comment }})

7. Fixed Build & Dependency Issues
   Removed husky-related issues by ignoring scripts:
   npm install --ignore-scripts --legacy-peer-deps
   npm rebuild esbuild
   Fixed broken Vite build related to esbuild.

8. Maintained Layout & Responsiveness
   Did not break Mazer’s original Bootstrap 5 structure.
   All cards, tables, and sections remain fully responsive.

9. Pushed Project to GitHub
   Initialized Git repo.
   Pushed to:
   https://github.com/shreshta21/mazer-task3
   Commits made clearly with proper messages.
   
11. Run
    npm run dev

12. Documented Work in README
Created a README.md explaining:

What was changed

How to install and run

Data binding logic

Technologies used
