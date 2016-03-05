# ghostwriter-themes

[Ghostwriter](https://github.com/wereturtle/ghostwriter) is a multiplataform distraction-free [Markdown](https://daringfireball.net/projects/markdown) editor. while I consider it a pretty good piece of software, it is still lacking a good variety of themes so users can avoid monotony when they feel like. Here I will collect my experimental themes, and you are invited to contribute yours.

## Theme Documentation

[Wereturtle](https://github.com/wereturtle), the developer of Ghostwriter, has not, so far, documented the Theme spec. This is a tentative approach to understanding what the theme file must include.

### Local

Theme files must be kept in a folder of their own inside the `~/.config/ghostwriter/themes` if you are on Linux, like me. If you're not, please edit this file to add where themes reside in other OSes.

### Naming

A theme is named by Ghostwriter as the directory its configuration is in. So, if your create a directory called "Foo" and put a valid `theme.cfg` file inside it, Ghostwriter will add a "Foo" theme to its theme menu.

### Theme contents

Each theme comprises the following sections:

#### [Background]

Sets the basic window area. Valid settings are `color` (for the background colour), `imageAspect` (for the method of handling the image) and `imageUrl` for the image filename (if any). Specifying `imageAspect` without a corresponding `imageUrl` may result in an invalid theme. The `imageUrl` can point anywhere, afaik, since it asks for a "URL" (Universal Resource Locator), but I hava only tried it with files residing in the same directory as the `theme.cfg`.

Example:
~~~~~~~~~~
  [Background]  
  color=#cccccc  
  imageAspect=1  
  imageUrl=file.jpg  
~~~~~~~~~

#### [Editor]

Sets the text editing area. No idea what `aspect` and `corners` are supposed to mean, but the rest is pretty self-explanatory.

~~~~~~~~~~~
  aspect=0
  backgroundColor=#ccc2af
  backgroundOpacity=0
  corners=0
  spellingErrorColor=#ff1000
~~~~~~~~~~~
  
#### [HUD]

Sets the appearance for the floating subwindows (Outline & Cheat-Sheet only, as the preview renders in a separate window). Ghostwriter cannot change the display font for these windows so far (though it'd be really cool).

~~~~~~~~~
  backgroundColor=#ccc2af
  foregroundColor=#311c1c
~~~~~~~~~~  

#### [Markdown]

Sets the appearance of the text itself, within the editor area. The three obvious values are the main text colour, the link colour and the markup colour (which is used to indicate spans recognised by Ghostwriter as markdown codes).

~~~~~~~~~~
defaultTextColor=#4b2d19
linkColor=#221093
markupColor=#cd142b
~~~~~~~~~

## Contributing

If you have created some themes and don't want to create a repository of your own, feel free to add them here.
