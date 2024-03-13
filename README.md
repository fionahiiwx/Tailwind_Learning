# Tailwind_Learning

by NetNitja

# Lesson 1 - Intro and Setup

## Installing TailwindCSS

npm init -y

npm install tailwindcss

package.json would have tailwindcss in the dependencies and a node_modules file (diff packages the tailwind depends on and its function)

## How Tailwind Works

src file (styles.css) > Tailwind > public file (styles.css) > index.html

src file = tailwind would be at

public file = final output css after tailwind has been processed, contain HTML and maybe any frontend Javascript; eventually deployed

## package.json file

no commenting in .json files

-o = output flag

build-css is from the "scripts" in the file

running it is by: npm run build-css

change things in the src/styles.css must be reprocessed to update the public/styles.css ones.

# Lesson 2 - HTML Template

**"doc" + tab** can automatically generate html content template.

npm install -g http-server

**http-server ./public** in terminal to see it in the web

ctrl+c to stop it

# Lesson 3 - Fonts & Colors

Tailwind gives us huge amount of low-level utility classes to style our elements amd by low-level

Classes only do 1 or 2 things: change colour, font size, position, padding, etc.

class = "text-gray-700" (text gray with 700 intensity)

text-6xl (text for 6xl size)

font-bold

# Lesson 4 - Padding, Margin & Borders

px-16 (padding on x-axis)

mt-12 (margin top)

border-t-8 (border top width 8px)

# Lesson 5 - Tailwind Config

## npx tailwindcss init --full

creates config gile with all default values that tailwind uses under the hood included in it

can see **tailwind.config.js** created (MUST BE THIS NAME!!!)

this file serves as the indicators of what each those things mean (like fontSize of xs means 0.75rem with lineHeight 1rem). So basically we can change the default.

## npx tailwindcss init

this only includes the bare minimum, no default values at all

remember to **npm run build-css** when changing the config or src/styles.css

extension **Tailwind CSS IntelliSense** must have the **tailwind.config.js** defined

# Lesson 6 - Custom Font

font-serif

can find fonts in google fonts

copy the embed url, then put it in src/styles.css

@import url('....')

then update it in ur config too

fontFamily: {
    any_name: [
        'the_font_family_name', 
        'can_add_more'
        ]
}

# Lesson 8 - Responsive Classes

module.exports = {
    theme: {
        screens: {
            'sm': '640px',
             @media (min-width: 640px) { ... }

             'md': '768px',
             @media (min-width: 768px) { ... }

             'lg': '1024px',
             @media (min-width: 1024px) { ... }

             'xl': '1280px',
             @media (min-width: 1280px) { ... }
        }
    }
}

# Lesson 9 - Cards

class = "rounded-sm"

# Lesson 10 - Badges

overflow-hidden

shadow-md
shadow-hidden

absolute

# Lesson 11 - @apply Directive

can use **@apply** in the src/styles.css so that u don't need to repeat in the html, much like the classes/IDs similar to CSS.

# Lesson 12 - Grids

lg:grid-cols-3 (when large screen, apply 3 column grid) so when it in in small screen, the card stack on top of each other
gap-10 (gap between the column)

when u have like grid-cols-3
and u want one of the div to cover up 2 of the columns, so put col-span-2
can put "md:" infront of it so that only medium screen would apply that 1:2 ratio. So in small screen, on top of each other

# Lesson 13 - Buttons

cursor-pointer
tracking-wider (space between letters)

# Lesson 14 - Icons

<svg>

# Lesson 15 - Hover effect

hover:text-gray-700

# Lesson 17 - Responsive Nav

transition ease-out duration-500