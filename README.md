# Haskell Agda Keyboards (Source code repository)

Here we have a keyboard layout file for setting up a keyboard on a MacOS X for writing all the difficult to type symbols that are used in Agda, and sometimes in Haskell.

To use it, first install it on your system.

If you want to edit it, or create an installation bundle, you can use [Ukelele](https://scripts.sil.org/ukelele) which is freely available software from SIL International for creating and editing keyboard layouts


## Supported Operating Systems
- Windows
- MacOS (Mojave 10.14, and some earlier versions)


## How to install a new keyboard layout on Mac OS X
1. Copy the `.keylayout` file to the `Keyboard Layouts` folder within `/Library` or `~/Library`.
   - You can navigate to the library folder for the current user from the finder by holding down
   the option key while selecting the Go menu.
2. Log out and log in again for changes to take effect.
3. Enable the new keyboard layout via _System Preferences_ › _Language & Text_ › _Input Sources_.
4. Press the `+` button on the window.
   - A window will appear allowing you to select which keyboard to add.
   - Note: it will not appear in English, but in the category `Others`.
   - It will be named `Haskell Agda`.

OS X has supported `.keylayout` files since version 10.2 (Jaguar).

## How to install a new keyboard layout on Windows
1. Download the file named Haskell_Agda_Keyboard_Layout_for_Windows_Latest.klc

- ToDo: add more instructions.

## Design decisions for initial keyboard

It is not based off any previous keyboard layout. It only keeps the numbers in their usual places. The reason is that if I made it based on a previous keyboard layout, it would be more difficult to type the characters (i.e. more work for the hands). Instead the user should map keyboard switching to a keyboard combination, and then be able to switch from their usual keyboard layout to this one.

This allows this keyboard layout to be universal in the sense that I do not have to make one for US layout, another for the UK layout, another for the other popular keyboard layouts around the world. It is possible, it is just too much work.

I did not spend much time in deciding where the symbols go. It helps if you have a keyboard viewer. I could have spent time trying to put all keys that are related next to each other, but of course keys could be related to each other in multiple ways (how they look, what they mean).

## Where did I get the choice of symbols

https://agda.readthedocs.io/en/v2.5.2/tools/emacs-mode.html

https://hackage.haskell.org/package/base-unicode-symbols

https://wiki.haskell.org/Unicode-symbols


## Collaboration / Usage

See License file.

## Wish list

- make a version for other operating systems
- add more characters that are used in Agda or Haskell.


## Background

Keyboards are physical devices, that are connected to a computer that type characters, spaces, or diacritics. A keyboard layout is a piece of software on the computer that tells the computer what character each key types. A user of a computer can change the keyboard layout. However, most keyboards do not have dynamic displays so they don't change their labels when the user changes keyboard layouts. Despite this, people who have enough typing experience usually can type without having to look at the keyboard, so this is not a big problem.

Typing in Russian, or multiple languages with different characters usually requires the user to have multiple keyboard layouts installed. People who are bilingual or multilingual and skilled with computers often learn to type in more than one language.

By contrast, people who use programming languages often all use the same keyboard layout. This is because most/all? popular programming langauges are based on the Latin characters without diacritics that English is usually written with, and the ASCII symbols. It is also the case for historical reasons that for many decades support for languages other than English was often flaky before Unicode, and for many years after (fonts, and many programs had to catch up).

But some programming languages, especially ones based more heavily on mathematical notation  use symbols from Math that are not available on any (non-specialist) keyboard layout. Among these languages are Agda, and to a lesser extent Haskell. But how are people typing these math characters? They are using special text editors, with key bindings. These key bindings allow them to convert something like \elem to the symbol ∈ . But there is no reason, that someone could not create a keyboard layout so that they could type their programming language in any program.


## Answers to questions

- Isn't it difficult to type in a keyboard layout without being able to see where the keys are?

Yes, it is at first. But you can turn on the keyboard viewer, or the virtual keyboard so that a small window with the keyboard layout appears on your window. You can use it for reference.

This is, of course, not anywhere near as ideal as actually having your keys labelled in some way with those symbols. It is technically possible to print out stickers with symbols on them, and stick them on your keyboard, but for most people it is too much work.

There are also people who create custom keyboards (that is physical keyboards), and custom keys. They could make something that would be the easiest to use.

- The keyboard layout doesn't make much, sense, I would put character X near Y, and put these groups of characters together.

I didn't spend much time refining the layout initially. I mainly layed out the keys for Agda from left to right ordered by their unicode value. Then I started laying out the keys for Haskell. Then I tried to put some arrows that are rotations of each other beside each other. Then I put the digits, the +, and = sign where they are. And I put the Unicode minus sign where the dash is on the U.S. standard. Note: It the unicode minus sign is distinct from the dash sign you have on most keyboards.

I do think the keyboard layout is unoptimal, but it is still a vast improvement over the alternative which is coping and pasting or clicking buttons. It is not any better than using a special text editor, but it could be with enough time.

- Why didn't you use any dead keys?

I didn't need to, because I didn't need to layout enough keys to run out. I did use the shift key, and the option key to layout some keys, but those are not dead keys.

If I wanted to make a keyboard layout based on the ones that people are used to like "U.S. standard", or "Canadian French", or others it would make sense to use the dead keys so that almost all the characters would be in the same place. But I am not making a keyboard layout based on a previous one.

- Why aren't you basing your keyboard layout on U.S. standard? Isn't it the most popular?

The reason is simple. Once you make a keyboard layout based on U.S. standard then it is only logical to make one based on Canadian French, and then one based on DVORAK, and so on. There are too many to do by hand.

If I had a tool that simply took my customization, and the placement of a dead key, then I could probably make 100 different keyboard layouts customized in the same way.

