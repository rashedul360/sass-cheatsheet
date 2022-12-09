## আজকে আমরা শিখব SASS সম্পর্কে

লেখকঃ রাশেদুল ইসলাম সিহাব ~~~ সর্বশেষ আপডেটঃ ৯ ডিসেম্বর ২০২২

# প্রতিটি অধ্যায়ের নাম

- [SASS কি? - what is SASS](#whatissass)
- [SASS শিখতে কিভাবে প্রস্তুতি নিতে পারি ? what are prerequities to learn SASS](#whatAreprerequities)
- [কেন SASS শিখব ? - why SASS?](#whySASS)
- [কিভাবে SASS কাজ করে ? - how to does SASS work?](#howDOesSassWork)
- [কিভাবে SASS HTML ফাইলের সাথে যুক্ত করব ? - how to add SASS to HTML?](#howTOAddSassTohtml)
- [variables and nestings css rules](#varialesNastingClass2)
- [Nesting css rules](#nestingCssRulescls2)
- [Partials and sass settings](#partialsSassSettingsclas2)
- [VS code settings (must be)](#vsCodeSettingsclas2)
- [lets talk about module](#aboutModule)
- [@mixin and @include](#mixinInclude)
- [@include and @inheritance](#includeinheritance)
- [@if @else @else if এঁর ব্যাবহার ](#ifElseElseIf)
- [Loop - For - while](#loopForWhile)
<link name="#whatissass">

### SASS কি? - what is SASS

- SASS is a syntactically awesome style sheet.
- It's is extension of CSS
- SASS designed by hampton cattin and developed by natalie weizenbaum in 2006.

<link name="#whatAreprerequities">
### SASS শিখতে কিভাবে প্রস্তুতি নিতে পারি ? - what are prerequities to learn SASS

- HTML
- CSS
- Javascript (will help you greatly specially for @if, @for, @while etc.)

<link name="#whySASS">

### কেন SASS শিখব ? - why SASS?

1. sass has some extra special features that do not exist in CSS.
   1. variables
   2. nested rules.
   3. mixins, imports
   4. inheritance
2. extra features এঁর উদ্দেশ্য হলো to make our code simpler and more maintainable.
3. no DRY (we can @extend css rules) ---> already কোণ কোড লিখে থাকলে সেগুলো আবার নিয়ে আসতে পারবেন ।
4. ফ্রি তে ডাউনলোড করা যায় ।
5. এটা CSS এঁর সব ভার্সন সাপোর্ট করে ।

<link name="#howDOesSassWork">
### কিভাবে SASS কাজ করে ? - how to does SASS work?

1. extension হবে .scss দিয়ে ।
2. browser তো SASS বুঝতে পারবে না । তাই এই নিয়মে কাজ করবে ।

   SASS code demo.scss ---> pre-processor (transpiler) এটা স্ট্যান্ডার্ড কোডে রূপান্তর করবে । ---> standard css code (demo.css) ---> browser

<link name="#howTOAddSassTohtml">

### কিভাবে SASS HTML ফাইলের সাথে যুক্ত করব ? - how to add SASS to HTML?

- install live sass compailer in VS code
  1. create a stykle folder. ---> demo.scss --> add some code into thi#.
  2. `<link ref="stylesheet" href="styles/demo.css">`
  3. start watching SASS

* css এঁর যেভাবে কমেন্ট করতাম ঠিক সেই দুই নিয়মেই SASS এ কমেন্ট করা যাবে ।
* SASS এ সিএসএস এঁর সব স্ট্যান্ডার্ড কোড করতে পারবেন ।
* extension টা ইন্সটল করা হলে SV code এর একদম নিচে `watch sass` নামে একটা মেনু/ বাটন পাব সেখানে ক্লিক করে দিব ।

<link name="#varialesNastingClass2">

### variales and nestings css rules

###### Learning outlines

1. how to declare -[SASS variables](#sassVarcls2)
2. how to use SASS variables
3. how to do nesting css rules

#### CSS variables

```css
:root {
 --primary-color: green;
}
h1 {
 color: var(--primary-color, red);
}
```

<link name="#sassVarcls2">

#### SASS variables

sass variables is more similar than css variables that we have used already.

- like JS(let,const) we can start declaring the variables using $ sign

###### example:

```CSS
$header-bdColor: colorName;
$main-bgColor: colorName;
$para-fontSize: size;
$para-font: 15px;
```

### usaing:

```CSS
header{
   background-color:$header-bgColor;
}
```

###### using SASS variables we can store.

1. number
2. string
3. boolean
4. colors.
5. lists
6. null
<link name="#nestingCssRulescls2">

### nesting css rules

প্রথমত html এ

```html
<nav>
 <ul>
  <li>
   <a href="#">list</a>
  </li>
 </ul>
</nav>
```

বানিয়ে নিব । এখন `nav` এর `ul, li, a` কে ডিজাইন করতে চাইলে অবশ্যয় এইভাবে করতাম

```css
nav{
   ---
}
nav ul{
   ---
}
nav ul li {
   ---
}
nav ul li a{
   ---
}
```

কিন্তু sass এঁর মাধ্যমে আরও সহজ সুন্দর করে লেখা যায় ।

```sass
nav{
   color:red;
   ul{
      color:green;
      li{
         color:orange;
         a{
            color:green
         }
         a:hover{
            color:red;
         }
      }
   }
}
```

এইভাবে নেস্টেড করে সিএসএস লেখা যায় sass এ ।

<link name="#partialsSassSettingsclas2">

### partials and sass settings

- create a new folder name by `sass project`
- then create a folder named app into the `sass project` folder.
- then create a `js` folder into the `app folder` named by `SASS`

- then create a `HTML` file into the `App folder`. its a root file
- then make HTML syntex to run webpage to the browser.

<link name="#vsCodeSettingsclas2">
### VS code settings (must be configured it)

\# Press command
<kbd>CTRL</kbd > + <kbd>Shift</kbd> + P
<kbd>Command</kbd > + <kbd>Shift</kbd> + P

\# then type `open settings`
\# then findout

```settings
#liveSass setup

"liveSassCompaile.settings.formats":[
   {
      "format" : "compressed",
      "extensionName" : ".css",
      "savePath" : "/dist", --> এটা রুট ফাইল এ dsit নামে একটা ফাইল তৈরি করবে এবং এখানে css গুলো সত্যরে থাকবে ।
   }
]
```

###### ---> Settings এঁর কাজ শেষ

###### --->then go to the `scss folder` and create a file named main.scss

###### ---> than link css with HTMl

```html
<link rel="stylesheet" href="../dist/main.css" />
```

###### ---> এখন watch sass এ ক্লিক করলেই একটা `dist` নামে একটা ফাইল এবং `main.css.map` নামে ফোল্ডার থাকবে ।

### now talk about the partials

    partialso হচ্ছে আপনার কোড কে separate করবে ছোট ছোট কিছু ফাইলের মাধ্যমে । সেটাকে আপনি পরবর্তীতে যে কোণ যায়গায় ব্যাবহার করতে পারবেন ।

\# যেহেতু সিএসএস এ reset code টা একটা কমন জিনিস তাই আপনি চাইলেই একটা আলাদা ফাইল এ রেখে যেকোনো সময় অ্যাক্সেস করতে পারবেন ।

\# ধরেন অনেক ডেভেলপার একটা প্রোজেক্টে কাজ করছে । এবং তারা আলাদা আলাদা ফাইলে কাজ করছে । এতে করে কি হবে ? কোড কনফ্লিক্ট হওয়ার সম্ভবনা নেই ।

\# then create a new folder under `scss` folder named `untill`. then create a new folder named `base` inside `untill` folder. then create a new file named `-reset.scss` (file name এঁর আগে - দেওয়ার কারণ হচ্ছে partials তৈরির জন্য সামনে underscore দিতে হয়) ।

```css
* {
 margin: 0;
 padding: 0;
 outline: none;
}
```

###### untill folder এ কাজ `sass tools, hyperfile, variable, function, mixin` এইগুলো ষ্টোর করে রাখবে ।

\# এইভাবে আরও partials আপনি তৈরি করতে পারবেন ।

\# এখন partials এ থাকা সিএসএস গুলো আমরা কিভাবে ব্যাবহার করব ? ঠিক এভাবেঃ

###### main.scss এ যান ।

###### @forward "./base/reset"; ---> এখানে (-) underscore দেওয়ার প্রয়োজন নেই এবং extension ও দেওয়ার প্রয়োজন নেই

\# যখন আরো কোণ নতুন partials তৈরি করবেন । সেটা ব্যাবহার করার জন্য অবশ্যয় `root sass file` `(main.scss)` এ @frword এঁর মাধ্যমে অ্যাপ্লাই করতে হবে ।

\# যেটা বলেছিলাম নতুন partials তিরি করলে সেঁতা ব্যাবহারের জন্য `root file` এ গিয়ে @forword এঁর মাধ্যমে অ্যাপ্লাই করতে হবে । এটা একটা ঝামেলাপূর্ণ ব্যাপার । তাই এখন একটা সমাধান তৈরি করব ।
\# যার জন্য `base folder` এঁর ভেতরে `-index.scss` নামে একটা ফাইল তৈরি করব এবং এখানে যত partials আছে সও গুলোকে অ্যাপ্লাই করব `index.scss` কে root style file `(main.scss)` এ অ্যাপ্লাই করব ।

<link name="#aboutModule">
### lets talk about module

প্রথমত `until folder` এ গিয়ে `-variables.scss` নামে একটা partials তৈরি করছি । এবং সেখানে কিছু variable assign করি । অ্যাপ্লাই করার জন্য এঁর ভেতরেই `-index.scss` নামে একটা partials তৈরি করব যেটা সব ডিজাইন কে অ্যাপ্লাই করতে সাহায্য করবে ,। তারপর আগের মতি শুধু `-index.scss` কে অ্যাপ্লাই করে দিব

কিন্তু এই অ্যাপ্লাই প্রচেসস টা একটু ভিন্ন । যেহেতু আমাদের শুধু অ্যাপ্লাই করে দিলেই হবে না । সেই variables গুলো স্থানভেদে ব্যাবহার করতে হবে ।

###### প্রচেস নিম্নরূপঃ

1. go to `main.scss`
2. @use "./until/index";

এখন headers এ যদি ব্যাবহার করতে চাই । তাহলে

```css
header {
 background-color: index.$headerbg;
}
```

যদি এ `variable` নাম পরিবর্তন করতে চাই তাহলে নাম পরিবর্তন করা ছাড়াই তাহলে এই কাজটি করতে হবে

```css
@use "./until/index" as variable;
header {
 background-color: variable.$header;
}
```

<link name="#mixinInclude">

## @mixin and include

### what is mixin and include?

a group of css declarations that can be reused throughout thestylesheets.

###### example:

```sass
declarations part.

@mixin para-style{
   font-size:16px;
}

uses.

#about-me p {
    @include para-style
}
```

###### example এ আমরা কিছু সিএসএস অ্যাপ্লাই দেখলাম @mixin এবং @include এঁর মাধ্যমে । এখন আমরা dynamic ভাবে @mixin and @include এঁর ব্যাবহার করা শিখব ।

###### declarations:

```sass
@mixin para-style($font,$margin){
   font-size: $font;
   margin: $margin;
}
```

###### uses:

```sass
#about > p{
   @include para-style(18px,left)
}
#education > p{
   @include para-style(50px,center)
}
```

<link name="#includeinheritance">

### @include and inheritance

@extend এঁর মাধ্যমে আমরা একটি selector এঁর কিছু property অন্য একটি selector এঁর মধ্যে inharit করতে পারি

```html
<button class="btn" />

<button class="btn2" />
```

```css
/* <!-- css file এ  --> */
.btn {
 background: red;
 color: black;
}
.btn2 {
 @extend .btn;
}
 btn2 class এও btn এঁর সব ডিজাইন অ্যাপ্লাই হয়ে যাবে । extend করার পাশাপাশি আপনি চাইলে আরও css add করতে পারবেন ।
```

<link name="#ifElseElseIf">

### @if, @else, @else if

###### declarations:

```sass
@mixin font-size ($value){
   @if $value ===small{
      font-size : 10px;
   }@else if $value ===large{
      font-size : 20px;
   }@else{
      font-size :none;
   }
}
```

###### uses:

```sass
 a{
      @include font-size(small)
}
```

<link name="#loopForWhile">

### Loop - For , while

```sass
@for $i from 1 through 12{
   do something
}
```

##### Real example

```sass
@for $i from 1 through{
   .col-#{$i}{
      width : 100% / 12 * i
   }
}
```

### @while

###### example:

```sass
$i : 1;
@while $i < 10{
   .col-#{$i}{
      width : 100% / 10 * i
   }
   $i = $i + 1;
}
```

###### each:

```css
.red-text {
 color: red;
}
.green-text {
 color: green;
}
.blue-text {
 color: blue;
}

@each $color in red, green, blue {
 #{$color}-text {
  color: $color;
 }
}
```

##### different ways to do it.

```sass
<!-- firstly declare a variable -->
$colors : {color1:red, color2:green, color3:blue};

@each  $key $color in $colors{
   #{$color}-text{
      color: $color;
   }
}

```

## References

- [https://sass-lang.com](https://sass-lang.com)
- [https://w3school.com/sass](https://w3school.com/sass)
- [https://www.codeacademy.com/learn/learn-sass](https://www.codeacademy.com/learn/learn-sass)
