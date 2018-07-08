## Maintenance tools for [language-noted] _and co_

**STOP!** This is **NOT** an `Atom` package itself.
There is nothing to install here: **No** package, **no** theme, _nothing_. There is hardly even any source code here.

If you came here looking for [language-noted] or any of its extensions such as [language-noted-todo], then you are at the **wrong** place. Just follow the just-mentioned links for that.

---------------------

This repository is used internally to track personal notes and also common resources and tools used for developing and maintaining several `Atom` packages in the [language-noted] family.

For the moment, this includes notably:

  - `resources/grammar-noted.xlsm`  (_Excel worksheet_ , see below for a decription)

##### `grammar-noted.xlsm`:

This is a _MS Excel worksheet_ that contains a bunch of macros and formulas for generating *regexen* and also *chunks* of the `grammar/noted.cson` file of [language-noted], as well as word and regex lists for [language-noted-todo] and [language-noted-doc].

Note that this is **NOT** really an automated process. The actual source files involved (e.g `grammar/noted.cson`) are still maintained manually; copying chunks from `Excel` and pasting them into the source file as needed.

The reason I have taken such a questionable path was to quickly get a **POC** (_Proof-Of-Concept_) up and running; and like many things made for a POC, it got stuck in the chain along the way... :-)

As [language-noted] stablizes, this should be replaced with a proper automation process, i.e. either through a classical *template-based* source generation, or else using `coffeScript` to generate a `CSON / JSON` within the [language-noted] package itself.

> I need to further investigate the feasability and suitability of the latter option.
> Although the first option (template-based generation) is quite straightforward, it would add a `build` in the process, which I would like to avoid. Granted, at worst, the `build` can happen before each release and the resulting tree would be the one that gets distributed, ... Still, better avoid it if we can.

Naturally, it's also possible to directly maintain the source files by hand; but, if possible, I would like to avoid that one too, since the `regexen` we employ tend have quite a few superflous capture groups in them (which simplifies some other aspects of `grammar/*.cson` files).

-----------------------
[language-noted]: <https://github.com/tabulon-addon/atom-language-noted>
[language-noted-todo]: <https://github.com/tabulon-addon/atom-language-noted-todo>
[language-noted-doc]: <https://github.com/tabulon-addon/atom-language-noted-doc>
