<!--
author:   André Dietrich & Sebastian Zug

email:    LiaScript@web.de

version:  0.0.1

language: en

narrator: US English Male

comment:  Try to write a short comment about
          your course, multiline is also okay.

import:   https://raw.githubusercontent.com/liaTemplates/AVR8js/main/README.md

-->

# Create & Share Interactive online-courses with LiaScript

                             --{{1}}--
These are Sebastian and André your hosts of the today's session about creating
and sharing online-courses with LiaScript. If you want to, you can try out
different presentation styles by switching them within the settings. Or, if you
want this course to be served within another language, try out the experimental
google-translation.

                              {{1-2}}
<div style="display: flex; flex-wrap: wrap; gap: 12px;">

<!-- style="flex: 1 0 48%; min-width:320px; margin: 0 6px 6px 0;"-->
> ![Pic: Sebastian Zug](https://tu-freiberg.de/sites/default/files/media/institut-fuer-informatik-9034/professur-st/zug_sebastian_192x125.jpg)
> __Sebastain Zug__ is Professor of Software Engineering and Robotics at
> TU Bergakademie Freiberg. His technical research focuses on outdoor robotics
> and the modeling of sensor errors in these scenarios. In addition, he works on
> concepts and tools for the digitalization of teaching. The main focus is on
> the collaborative development of OER teaching materials and cooperatively used
> remote laboratories. In this area, Sebastian Zug coordinates several national
> research projects.
>
> **Contact: [Sebastian.Zug@informatik.tu-freiberg.de](mailto:Sebastian.Zug@informatik.tu-freiberg.de)**

<!-- style="flex: 1 0 48%; min-width:320px; margin: 0 6px 6px 0;"-->
> ![Pic: André Dietrich](https://oeb.global/sites/default/files/images/speakers/imported/2021-08-1311%25253A32%25253A48477724-me.jpg)
> __André Dietrich__ is originally a robotics and embedded software developer,
> now working as a researcher at the TU Bergakademie Freiberg. Due to struggles
> with common Learning-Management-Systems and authoring-systems, he started the
> development on LiaScript, a language-based approach for creating interactive
> and open online-courses. His current research interests are language design,
> new web technologies and online education with focus on open educational
> resources.
>
> **Contact: [Andre.Dietrich@informatik.tu-freiberg.de](mailto:Andre.Dietrich@informatik.tu-freiberg.de)**

</div>

---

                             --{{2}}--
Before we start, here are a couple of additional resources that allow you to
take a deeper dive into LiaScript. You can also contact us via email or start a conversation at [gitter](https://gitter.im/LiaScript/community?source=orgpage).


                               {{2}}
* __Project-Website:__ https://LiaScript.github.io
* __OpenSource:__ https://github.com/liascript
* __YouTube:__ https://www.youtube.com/channel/UCyiTe2GkW_u05HSdvUblGYg
* __Additional resources:__

  - Documentation: https://github.com/LiaScript/docs
  - Free books: https://github.com/LiaBooks
  - Templates: https://github.com/LiaTemplates
  - Talks & ...: https://github.com/LiaPlayground
  - Blog: https://aizac.herokuapp.com

## About LiaScript

                             --{{0}}--
The development on LiaScript started as a side-project within the
["Industrial eLab"](http://www.elab.ovgu.de/Das+Projekt.html) project in
Magdeburg. You can check out the follwoing video resource, which shows an
earlier version of the system as well as an historical outline.

!?[Open Course Development with Liascript](https://www.youtube.com/watch?v=w_CRABsJNKA)


                             --{{1}}--
We needed a way of providing educational content for programming courses and
thought that a language-based approach instead of a tooling- or plattform-based
might provide a higher degree of freedom, exchangeability, and sustainability,
next to some other benefits.


                               {{1}}
* No backend required
* Works offline (PWA)
* Open-Source development and Versioning
* Faster development cycles
* ... and more


                             --{{2}}--
And finally, we wanted to have a system that can be used for different purposes,
we wanted to use it for presentations, but in the same way also for developing
interactive books, or to have something like YouTube-screencast with automated
text-to-speech output.

                               {{2}}
********************************************************************************

**Display-Formats:**

1. Textbook
2. Presentation
3. Slides

********************************************************************************

## Syntax

                             --{{0}}--
In order to flatten the learning curve and to not reinvent the wheel, we decided
to rely on Markdown. But, we also wanted to have an extendable language with
support for interactivity and beyond the possibilities of todays Learning
Management Systems.

<div style="width:100%;height:0;padding-bottom:100%;position:relative;"><iframe src="https://giphy.com/embed/HEURGne9Vj856oivkD" width="100%" height="100%" style="position:absolute" frameBorder="0" class="giphy-embed" allowFullScreen></iframe></div><p><a href="https://giphy.com/gifs/shecodesio-swipe-up-computer-congratulations-HEURGne9Vj856oivkD">via GIPHY</a></p>

                             --{{1}}--
Within the follwoing section, we will shortly introduce the basic Markdown
syntax and then some our extensions or reinterpretations.


### 1. Markdown basics

                             --{{1}}--
Markdown is a pretty simple Markup-language to learn. Everything starts with a `#`
or heading. The number of hashtags defines the heading number. In LiaScript
these headings are also used as separators between different "slides".


                              {{1-2}}
``` markdown
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6
```

                             --{{2}}--
A paragraph is simply a block of text/sentences that are separated by an empty
line. Thus, empty lines do not only provide a visual separator for the author,
but posses also a semantic value as separators between blocks. By the way, it
makes no difference if you use only one or multiple empty lines.

                              {{2-3}}
********************************************************************************

``` markdown
A text block that consists of multiple lines,
is a simple paragraph.

An empty line is a simple divider between
different paragraphs or other Markdown blocks.
```

---

A text block that consists of multiple lines,
is a simple paragraph.

An empty line is a simple divider between
different paragraphs or other Markdown blocks.

********************************************************************************

                             --{{3}}--
How would you create an ordered or unordered list only by using a typewriter?
Probably in a similar way. You can mix different lists with different Markdown
blocks. The only thing that is important in this case is to use a propper
indentation.

                              {{3-4}}
********************************************************************************

``` markdown
* unordered list
* with an additional

  1. ordered list
  2. as a sub element

- isn't that easy?
```

---

* unordered list
* with an additional

  1. ordered list
  2. as a sub element

- isn't that easy?

********************************************************************************


                             --{{4}}--
Highlighting elements within the text as *italic*, **bold**, or ***both*** with
underlines and other features is also possible, just by surrounding the element
with asterisks, tildes or underscores or other characters.

                              {{4-5}}
********************************************************************************
``` markdown
- *italic* ... _also italic_
- **bold** ... __also bold__
- ***bold and italic*** ... ___also ...___
- ~crossed out~
- ~~underlined~~
- ~~~crossed out and underlined~~~
- ** ~_and_ mix~tures ** _are **allowed**_ ^~~as~~ *well*^
```

---

- *italic* ... _also italic_
- **bold** ... __also bold__
- ***bold and italic*** ... ___also ...___
- ~crossed out~
- ~~underlined~~
- ~~~crossed out and underlined~~~
- ** ~_and_ mix~tures ** _are **allowed**_ ^~~as~~ *well*^

********************************************************************************


                             --{{5}}--
Tables are also self-explanatory. The only thing that is relevant in this case
is the use of colons within the separators between the head and the body. The
position of colons is used as an indicator of whether the column should be
aligned to the left, right, or centered. The LiaScript interpreter adds the
possibility to sort the table by clicking onto the sort-button on the right
corner of every column header.

                              {{5-6}}
********************************************************************************

``` markdown
| Tables               |      Are      |  Cool |
| -------------------- |:-------------:| -----:|
| *** columns 3 is *** | right-aligned | $1600 |
| ** column 2 is **    |   centered    |   $12 |
| * zebra stripes *    |   are neat    |    $1 |
```

---

| Tables               |      Are      |  Cool |
| -------------------- |:-------------:| -----:|
| *** columns 3 is *** | right-aligned | $1600 |
| ** column 2 is **    |   centered    |   $12 |
| * zebra stripes *    |   are neat    |    $1 |

********************************************************************************

                             --{{6}}--
Quoting important phrases was inspired by emails.

                              {{6-7}}
********************************************************************************

``` markdown
> A block-quote with something important that was said long
> time ago ...
>
> -- by somebody
```

---

> A block-quote with something important that was said long
> time ago ...
>
> -- by somebody

********************************************************************************


                             --{{7}}--
Last but not least, a peace of code, where syntax-highlighting should be
applied, has only be surrounded by at least three backtics with an language
indicator at the top.

                              {{7-8}}
********************************************************************************

````
``` cpp
// Your First C++ Program

#include <iostream>

int main() {
    std::cout << "Hello World!";
    return 0;
}
```
````

---

``` cpp
// Your First C++ Program

#include <iostream>

int main() {
    std::cout << "Hello World!";
    return 0;
}
```

********************************************************************************


### 2. References

                             --{{0}}--
There are actually four types of references in Markdown, you can either directly
place a link everywhere within your documents. Most parsers are pretty smart and
will recognize this, but this can become quite ugly for long urls. Hence, you
can add named links via combination of brackets and parenthesis. The same can be
used to reference parts within the document and if you want to include an image,
this link has to be marked with a starting exclamation mark.


1. **A direct link:**

   `https://LiaScript.github.io`

   https://LiaScript.github.io

2. **A named link:**

   `[LiaScript](https://LiaScript.github.io)`

   [LiaScript](https://LiaScript.github.io)

3. **An internal link:**

   `[about liascript](#about-liascript)`

   [about liascript](#about-liascript)

4. **An image:**

   `![alt text](https://...url...image.jpg)`

   ![Netherlandish Proverbs](https://upload.wikimedia.org/wikipedia/commons/thumb/7/7e/Pieter_Brueghel_the_Elder_-_The_Dutch_Proverbs_-_Google_Art_Project.jpg/2560px-Pieter_Brueghel_the_Elder_-_The_Dutch_Proverbs_-_Google_Art_Project.jpg "Pieter Brueghel the Elder - The Dutch Proverbs")

                             --{{2}}--
LiaScript is smart enough to scale your the image propperly, furthermore it is
possible to click onto the image in order to enlarge it and inspect the details.

### 3. Extensions

                             --{{0}}--
By now you should have a basic understanding of Markdown. Within the next part
we will go briefly through some of our extensions and reinterpretations that can
be used to create interactive learning experiences.

<div style="width:100%;height:0;padding-bottom:74%;position:relative;"><iframe src="https://giphy.com/embed/uBQNLeszLtiNO" width="100%" height="100%" style="position:absolute" frameBorder="0" class="giphy-embed" allowFullScreen></iframe></div><p><a href="https://giphy.com/gifs/disney-cinderella-fairy-godmother-bibbidi-bobbidi-boo-uBQNLeszLtiNO">via GIPHY</a></p>

#### A. Animations & TTS

                             --{{0}}--
Everything that is related to animations, is associated to braces. Double braces
at the beginning of a block indicate the point in time when something should
appear or disappear. Braces surrounded by dashes can be interpreted as the
explanaition for a specific point. Thats it, if you change the representation of
the course, these elements will be treated differently.

``` markdown
       --{{1}}--
See this important table.

             {{1-2}}
| I   | appear    | at  | first |
| --- | --------- | --- | ----- |
| and | disappear | at  | two   |


              {{2}}
* I will remain till the end
* and do have some {3}{__inline animations__}
* inline effects can also {3-4}{dissapear} ...

        --{{2}}--
The bullet point list is also quite important, it contains some sub effects

        --{{3 Russian Female}}--
Первоначально создан в 2004 году Джоном Грубером (англ. John Gruber) и Аароном
Шварцем. Многие идеи языка были позаимствованы из существующих соглашений по
разметке текста в электронных письмах...
```

       --{{1}}--
See this important table.

             {{1-2}}
| I   | appear    | at  | first |
| --- | --------- | --- | ----- |
| and | disappear | at  | two   |


              {{2}}
* I will remain till the end
* and do have some {3}{__inline animations__}
* inline effects can also {3-4}{dissapear} ...

        --{{2}}--
The bullet point list is also quite important, it contains some sub effects

        --{{3 Russian Female}}--
Первоначально создан в 2004 году Джоном Грубером (англ. John Gruber) и Аароном
Шварцем. Многие идеи языка были позаимствованы из существующих соглашений по
разметке текста в электронных письмах...

                             --{{4}}--
If you try out the experimental google translation, you will find out that
everything gets translated and also the voice will change, except for the
russian text, this will remain.


#### B. Movies and XXX

                             --{{0}}--
We simply extended reference in three ways. If an exclamation mark is used to
identify an image, then maybe a question mark can be used for audio files.

                              {{0-2}}
``` markdown
?[soundcloud](https://soundcloud.com/glennmorrison/beethoven-moonlight-sonata)
```

                              {{1-2}}
?[soundcloud](https://soundcloud.com/glennmorrison/beethoven-moonlight-sonata)


                             --{{2}}--
And if you combine an image with audio, then this can be used as an marker for
videos.

                              {{2-4}}
``` markdown
!?[Create an LMS Educational Website](https://www.youtube.com/watch?v=df5hfVID5mo)
```

                             --{{3}}--
The follwoing example shows, how you can create an educational website in three
hours, content creation not included.

                              {{3-4}}
!?[Create an LMS Educational Website](https://www.youtube.com/watch?v=df5hfVID5mo)


                             --{{4}}--
And finally, if you have no idea, then use two question marks. In this case
LiaScript will try to oEmbed the content of the link or at least try to add this
as an iframe.

                               {{4}}
********************************************************************************

``` markdown
??[anotomy of the eye](https://sketchfab.com/3d-models/the-human-eye-extrinsic-muscle-contraction-20-dc9c88630b6c42a8b242fd6024d0697f)
```

??[anotomy of the eye](https://sketchfab.com/3d-models/the-human-eye-extrinsic-muscle-contraction-20-dc9c88630b6c42a8b242fd6024d0697f)

********************************************************************************

#### C. Coding

                             --{{0}}--
The script-tag is an native element in LiaScript. It can be either used
stand-alone or in combination with other elements. If you attach a script-tag to
an Markdown code-block, then this tells the LiaScript inpterpeter that this is
an editable and executable piece of code. The script-tag in this case is used to
tell LiaScript how to deal with the code. If it is JavaScript, then directly
interpret the input code.


```` markdown
``` javascript
console.log("Hello World")

console.warn("Global climate change is a serious threat!!!")

42
```
<script>@input</script>
````

                             --{{1}}--
You can execute and modify this peace of code directly. Every change creates a
new version and you as a user can go back and forth.


                               {{1}}
``` javascript
console.log("Hello World")

console.warn("Global climate change is a serious threat!!!")

42
```
<script>@input</script>


                             --{{2}}--
But such script-tags can contain also more elaborate code, which you don't want
want to copy an paste again and again. LiaScript therefore offers the
opportunity to create macros, which can be parameterized and imported from other
courses, Just like an ordinary library as it done in other programming
languages.


                               {{2}}
```` markdown
<div id="example">
<wokwi-led color="red"   pin="13" label="13"></wokwi-led>
<wokwi-led color="green" pin="12" label="12"></wokwi-led>
<wokwi-led color="blue"  pin="11" label="11"></wokwi-led>
<wokwi-led color="blue"  pin="10" label="10"></wokwi-led>
<span id="simulation-time"></span>
</div>

``` cpp
byte leds[] = {13, 12, 11, 10};
void setup() {
  Serial.begin(115200);
  for (byte i = 0; i < sizeof(leds); i++) {
    pinMode(leds[i], OUTPUT);
  }
}

int i = 0;
void loop() {
  Serial.print("LED: ");
  Serial.println(i);
  digitalWrite(leds[i], HIGH);
  delay(250);
  digitalWrite(leds[i], LOW);
  i = (i + 1) % sizeof(leds);
}
```
@AVR8js.sketch(example)
````

                             --{{3}}--
The `@`-whatsoever gets replaced by a more complex script and by importing the
template course, your course also adds all relevant JavaScript, CSS, and a bunch
of additional elements that might be required.

                               {{3}}
********************************************************************************

<div id="example">
<wokwi-led color="red"   pin="13" label="13"></wokwi-led>
<wokwi-led color="green" pin="12" label="12"></wokwi-led>
<wokwi-led color="blue"  pin="11" label="11"></wokwi-led>
<wokwi-led color="blue"  pin="10" label="10"></wokwi-led>
<span id="simulation-time"></span>
</div>

``` cpp
byte leds[] = {13, 12, 11, 10};
void setup() {
  Serial.begin(115200);
  for (byte i = 0; i < sizeof(leds); i++) {
    pinMode(leds[i], OUTPUT);
  }
}

int i = 0;
void loop() {
  Serial.print("LED: ");
  Serial.println(i);
  digitalWrite(leds[i], HIGH);
  delay(250);
  digitalWrite(leds[i], LOW);
  i = (i + 1) % sizeof(leds);
}
```
@AVR8js.sketch(example)

********************************************************************************

#### D. Data & Tables

                             --{{0}}--
Only a quick side-note. Tables in most cases also contain some form of
structured data that begs for being visualized.

                             --{{1}}--
Thus, if you see the follwoing table, how would you visualize it?


                              {{1-3}}
``` markdown
<!--
data-title="Government expenditure on education"
data-xlabel="year"
data-ylabel="% of GDP"
-->
| Year | Finland |     USA | Germany |   China |
| ---- | -------:| -------:| -------:| -------:|
| 1995 | 6.80942 |         | 4.42079 | 1.84192 |
| 1996 | 6.86052 |         | 4.48319 | 1.85338 |
| 1997 |         |         |         |         |
| 1998 |         |         | 4.45345 | 1.84432 |
| 1999 | 5.86960 |         |         | 1.88803 |
| 2000 | 5.71687 |         |         |         |
| 2001 | 5.84797 |         |         |         |
| 2002 | 6.02477 |         |         |         |
| 2003 | 6.17476 |         |         |         |
| 2004 | 6.16849 |         |         |         |
| 2005 | 6.03605 |         |         |         |
| 2006 | 5.93809 |         | 4.27930 |         |
| 2007 | 5.68608 |         | 4.34302 |         |
| 2008 | 5.84676 |         | 4.40954 |         |
| 2009 | 6.48517 |         | 4.88047 |         |
| 2010 | 6.54070 | 5.42001 | 4.91368 |         |
| 2011 | 6.48200 | 5.22389 | 4.80779 |         |
| 2012 | 7.19254 | 5.19485 | 4.93331 |         |
| 2013 | 7.15848 | 4.94378 | 4.93496 |         |
| 2014 | 7.15155 | 4.98948 | 4.93112 |         |
```

                             --{{2}}--
Probably also as a line-chart and this is what LiaScript does as well. It tries
to find patterns for the most appropriate visualization.

                              {{2-3}}
<!--
data-title="Government expenditure on education"
data-xlabel="year"
data-ylabel="% of GDP"
-->
| Year | Finland |     USA | Germany |   China |
| ---- | -------:| -------:| -------:| -------:|
| 1995 | 6.80942 |         | 4.42079 | 1.84192 |
| 1996 | 6.86052 |         | 4.48319 | 1.85338 |
| 1997 |         |         |         |         |
| 1998 |         |         | 4.45345 | 1.84432 |
| 1999 | 5.86960 |         |         | 1.88803 |
| 2000 | 5.71687 |         |         |         |
| 2001 | 5.84797 |         |         |         |
| 2002 | 6.02477 |         |         |         |
| 2003 | 6.17476 |         |         |         |
| 2004 | 6.16849 |         |         |         |
| 2005 | 6.03605 |         |         |         |
| 2006 | 5.93809 |         | 4.27930 |         |
| 2007 | 5.68608 |         | 4.34302 |         |
| 2008 | 5.84676 |         | 4.40954 |         |
| 2009 | 6.48517 |         | 4.88047 |         |
| 2010 | 6.54070 | 5.42001 | 4.91368 |         |
| 2011 | 6.48200 | 5.22389 | 4.80779 |         |
| 2012 | 7.19254 | 5.19485 | 4.93331 |         |
| 2013 | 7.15848 | 4.94378 | 4.93496 |         |
| 2014 | 7.15155 | 4.98948 | 4.93112 |         |


                             --{{3}}--
The follwoing table might look like an bar-chart, since the first column does
not contain any numbers. But instead this could be identified as categories.


                              {{3-5}}
``` md
| Animal          | weight in kg | Lifespan years | Mitogen |
| --------------- | ------------:| --------------:| -------:|
| Mouse           |        0.028 |              2 |      95 |
| Flying squirrel |        0.085 |             15 |      50 |
| Brown bat       |        0.020 |             30 |      10 |
| Sheep           |           90 |             12 |      95 |
| Human           |           68 |             70 |      10 |
```

                             --{{4}}--
You can try to sort the table and check the resulting visualization and also
filter it.


                              {{4-5}}
| Animal          | weight in kg | Lifespan years | Mitogen |
| --------------- | ------------:| --------------:| -------:|
| Mouse           |        0.028 |              2 |      95 |
| Flying squirrel |        0.085 |             15 |      50 |
| Brown bat       |        0.020 |             30 |      10 |
| Sheep           |           90 |             12 |      95 |
| Human           |           68 |             70 |      10 |


                             --{{5}}--
A table with only one line might be interpreted as an pie-chart. But, it is also
possible to combine this with animations, as we had seen it earlier.

                               {{5}}
``` markdown
| Music-Style {0-1}{1994} {1}{2014} |           Classic |           Country | Reggae |             Hip-Hop |           Hard-Rock |               Samba |
|:--------------------------------- | -----------------:| -----------------:| ------:| -------------------:| -------------------:| -------------------:|
| Student rating                    | {0-1}{50} {1}{20} | {0-1}{50} {1}{30} |    100 | {0-1}{200} {1}{220} | {0-1}{350} {1}{400} | {0-1}{250} {1}{230} |

```

                             --{{6}}--
Thus, if you change to the visualization, the changes might become more obvious.

                               {{6}}
| Music-Style {6-7}{1994} {7}{2014} |           Classic |           Country | Reggae |             Hip-Hop |           Hard-Rock |               Samba |
|:--------------------------------- | -----------------:| -----------------:| ------:| -------------------:| -------------------:| -------------------:|
| Student rating                    | {6-7}{50} {7}{20} | {6-7}{50} {7}{30} |    100 | {6-7}{200} {7}{220} | {6-7}{350} {7}{400} | {6-7}{250} {7}{230} |

#### E. Quizzes?

##### A Textquiz

What did the **fish** say when he hit a **concrete wall**?

    [[dam]]

##### Multiple Choice

Just add as many points as you wish:

    [[X]] Only the **X** marks the correct point.
    [[ ]] Empty ones are wrong.
    [[X]] ...

##### Single Choice

Just add as many points as you wish:

    [( )] ...
    [(X)] <-- Only the **X** is allowed.
    [( )] ...


## A typical workflow


## Publishing via ...

### GitHub

### DropBox

### IPFS

### Beaker

### ...
