# <center><i>TailWind</i></center>

## Setting up the tailwind css
- Just use <b>tailwind</b> link
    -  ```<script src="https://cdn.tailwindcss.com"></script> ```
- While you use this link, got an error 'In console window'
    - ```cdn.tailwindcss.com should not be used in production. To use Tailwind CSS in production, install it as a PostCSS plugin or use the Tailwind CLI: https://tailwindcss.com/docs/installation```
- <b>Solution</b>
    1. Open folder where you want to code tailwind
    2. install node js
    3. write code in terminal or That location : <b>npm init -y</b>
    4. <b>npm install -D tailwindcss postcss autoprefixer vite</b> 
    5. <b>npx tailwindcss init -p</b>
        - Create a css file "input.css", add it to your html and edit it with this content:
            - @tailwind base; => Some css code present here
            - @tailwind components; => Here also present some CSS code
            - @tailwind utilities; => Utilities classes
    6. package.json -> script.text -> change key = start AND value = vite
    7. tailwind.config.js -> content: ["*"]
    7. ```https://tailwindcss.com/docs/installation/using-postcss```

## What is tailwind
- Tailwind CSS is a utility-first CSS framework, providing low-level utility classes for direct application in HTML elements, allowing the creation of designs through the composition of small, composable classes. 
- Users can customize Tailwind to generate only the necessary styles, ensuring a compact final CSS file size. 
- Ultimately, the choice between Tailwind and other frameworks depends on personal preferences and project requirements.
- tailwind CSS v3.0 replaced with just in time (JIT)
- Codes are readable

## Why Use Tailwind CSS
- No reinventing of class names required
- You CSS doesn't grow with your html and designs
- When you make a change, no risk of breaking existing templates!
- Will this make sites slow? Will it increase bundle size? -> <b>NO</b>
- What about responsiveness? -> <b>Yes</b>
- Inline : Tailwind? Tailwind {Minimize the thinking just provide good looking page it has some specific numbers to use} 

## Small Replacement
- Direction X-axis = x, Y-axis = y, top = t, bottom = b, left = l, right = r
- Number = Predefined color present like 2, 4, 8, 12, 1, 500, 900 
- x stands for the extra
- s stands fot the small
- l stands for the large
- Undefined value passes : m-[valuewithUnit]

## Replacement : CSS to Tailwind
- Font Color -> text-colorName-Number(Predefined)
- justify content -> space-between -> space-x-4 -> justify-around -> justify-between
- margin -> mx-4 
- padding -> px-4
- cursor-pointer
- background-color -> bg-colorName-Number 
- align-item -> items-alignment
- float:right -> justify-end 
- font-size: 1.25rem -> text-xl -> 20px
- When you type font You get - font family , font weight 
- when you type text you get - font size, 
- letter spacing : tracking-tighter
- line-height : leading-4
- list-image-[none, url()], list-none   
- Styling just typing : italic 

## Responsive
- Use unprefixed utilities to target mobile, and override them at larger breakpoints
- First design mobile view then design for the desktop view IN CASE OF 'min'
- @media query and (min-width: px) {}
    1. sm -> 640px - 767px
    2. md -> 768px - 1023px
    3. lg -> 1024px - 1279px
    4. xl -> 1280px - 1535px
    5. 2xl -> 1236px - unlimited
- @media query and (max-width: px) {}
    1. max-sm -> 640px - 767px
    2. max-md -> 768px - 1023px
    3. max-lg -> 1024px - 1279px
    4. max-xl -> 1280px - 1535px
    5. max-2xl -> 1236px - unlimited
- Hide -> hidden; screen:visible; display:block;

## External CSS -> <b>@apply</b>
- Apply your CSS between : components & utilities for better expierence
- id and class 
- Syntax :- @apply ...yourCSS... 
- Allow multiple @apply for css
- You can also seperate @apply with different screen size and effects

## Layer Directive
- You can define CSS anywhere in the CSS file, and by providing directives, you can set its position.
- Positions
    1. base
    2. components
    3. utilities
- CSS Code
    - <pre>@layer components {
        .btn {
            @appy bg-blue-500;
        } 
      } </pre>
- The above code implies adding the CSS where the components' CSS is defined and placing it at the end of the components.

## Customizing tailwind CSS
- File : tailwind.cofig.js
- Location : module.exports.theme.extend
- Inside {} : Add your Values here, In form of objects
- Extra support : 
    - <pre>npx tailwind init fileName --full</pre>
    - Above code add a file of JS, where your css code present
- Now you can add value manually 

## Theme object in tailwind.config.css
- Oberride in theme
- Screen breakpoint must be written here to add breakpoint

## For Deployment :- Github
1. File : package.json
2. In script object : Add Key - 'build', Value - 'vite build'
3. Terminal : npm run build
4. After this you get you production folder 
5. Must be accurate file location used
