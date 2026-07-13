---
UID: NS:winddi._IFIMETRICS
title: IFIMETRICS (winddi.h)
description: The IFIMETRICS structure defines information for a given typeface that GDI can use.
helpviewer_keywords: ["*PIFIMETRICS","IFIMETRICS","IFIMETRICS structure [Display Devices]","PIFIMETRICS","PIFIMETRICS structure pointer [Display Devices]","display.ifimetrics","grstrcts_85d0a649-0d14-4b17-ab47-c35d61ce507e.xml","winddi/IFIMETRICS","winddi/PIFIMETRICS"]
old-location: display\ifimetrics.htm
tech.root: display
ms.assetid: fd2606ed-ec61-430a-aaad-38a4c3a207b6
ms.date: 12/05/2018
ms.keywords: '*PIFIMETRICS, IFIMETRICS, IFIMETRICS structure [Display Devices], PIFIMETRICS, PIFIMETRICS structure pointer [Display Devices], display.ifimetrics, grstrcts_85d0a649-0d14-4b17-ab47-c35d61ce507e.xml, winddi/IFIMETRICS, winddi/PIFIMETRICS'
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IFIMETRICS, *PIFIMETRICS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IFIMETRICS
 - winddi/_IFIMETRICS
 - PIFIMETRICS
 - winddi/PIFIMETRICS
 - IFIMETRICS
 - winddi/IFIMETRICS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - IFIMETRICS
---

# IFIMETRICS structure


## -description

The IFIMETRICS structure defines information for a given typeface that GDI can use.

## -struct-fields

### -field cjThis

Specifies the size in bytes of this structure. The specified size includes any Unicode strings appended to the end of this structure, plus the size in bytes of the optional <a href="/windows/desktop/api/winddi/ns-winddi-ifiextra">IFIEXTRA</a> structure.

### -field cjIfiExtra

Specifies the size in bytes of the IFIEXTRA structure that follows this IFIMETRICS structure. A value of zero indicates that no IFIEXTRA structure is present.

### -field dpwszFamilyName

Specifies the offset in bytes to a null-terminated Unicode string containing the family name of the font (for example, "Times Roman"). Generally, this string immediately follows the IFIMETRICS structure. This string should be the same as the name recorded in the <b>lfFaceName</b> member of the Win32 LOGFONT structure.

### -field dpwszStyleName

Specifies the offset in bytes to a null-terminated Unicode string describing the style of the font (for example, "Bold").

### -field dpwszFaceName

Specifies the offset in bytes to a null-terminated Unicode string representing the unique and complete name of the font. The name contains the family and subfamily names of the font (for example, "Times New Roman Bold").

### -field dpwszUniqueName

Specifies the offset in bytes to a null-terminated Unicode string representing the unique identifier of the font (for example, "Monotype:Times New Roman:1990").

### -field dpFontSim

Specifies the offset in bytes from the beginning of this IFIMETRICS structure to a <a href="/windows/desktop/api/winddi/ns-winddi-fontsim">FONTSIM</a> structure that describes the simulations that the font supports. The driver should set this member to a nonzero value only if the font supports bold, italic, or bold italic simulations; otherwise, the driver should set this to zero.

Note that if a font is italic by design, the driver should not indicate font support for italic simulation although it can indicate font support for bold italic simulation. Similarly, the driver should not indicate font support for bold simulation if the font is bold by design, but can indicate font support for bold italic simulation. If the font is both bold and italic by design, it should not support any simulations.

The offsets in the <a href="/windows/desktop/api/winddi/ns-winddi-fontsim">FONTSIM</a> structure are relative to the base of the FONTSIM structure.

### -field lEmbedId

Specifies the Embedding ID of the font. This value is TrueType-specific and should be set to zero by all other font providers.

### -field lItalicAngle

Specifies the italic angle of the font. This value is TrueType-specific and should be set to zero by all other font providers.

### -field lCharBias

Specifies the character bias. This value is TrueType-specific and should be set to zero by all other font providers.

### -field dpCharSets

Specifies the offset from the beginning of this IFIMETRICS structure to an array containing a list of all Windows character sets supported by this font. The array is 16 bytes in size and is always terminated with **DEFAULT_CHARSET**. The first value of the array should identify the Windows character set that has the best and most complete coverage in the font; this value should also be stored in <b>jWinCharSet</b>. For instance, if this is a Japanese font that also supports US ANSI and Cyrillic character sets, then <b>jWinCharSet</b> should be set to **SHIFTJIS_CHARSET** and the array identified by <b>dpCharSets</b> would contain **SHIFTJIS_CHARSET**, **ANSI_CHARSET**, **RUSSIAN_CHARSET**, **DEFAULT_CHARSET**.

If this font does not support more than one Windows character set, <b>dpCharSets</b> should be set to zero.

### -field jWinCharSet

Identifies the character set best supported by this font. If the font supports only a single Windows character set, the driver should store the corresponding value in <b>jWinCharSet</b>. The driver should not store **DEFAULT_CHARSET** in this field.

For a list of possible values, see *lfCharSet* field of the <a href="/windows/desktop/api/wingdi/ns-wingdi-logfontw">LOGFONT structure</a>.

### -field jWinPitchAndFamily

Specifies the pitch of the font. The two low-order bits specify the pitch of the font and can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
FIXED_PITCH

</td>
<td>
For fixed pitch fonts

</td>
</tr>
<tr>
<td>
VARIABLE_PITCH

</td>
<td>
For variable pitch fonts

</td>
</tr>
</table>
 

Bits 4 through 7 of this member specify the font family and can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
FF_DECORATIVE

</td>
<td>
Novelty fonts, such as Old English.

</td>
</tr>
<tr>
<td>
FF_DONTCARE

</td>
<td>
Don't care or unknown.

</td>
</tr>
<tr>
<td>
FF_MODERN

</td>
<td>
Fonts with constant stroke width (fixed-pitch), with or without serifs. Fixed-pitch fonts are usually modern, such as Pica, Elite, and Courier.

</td>
</tr>
<tr>
<td>
FF_ROMAN

</td>
<td>
Fonts with variable stroke width (proportionally spaced) and with serifs, such as Times Roman, Palatino, and Century Schoolbook.

</td>
</tr>
<tr>
<td>
FF_SCRIPT

</td>
<td>
Fonts designed to look like handwriting, such as Script and Cursive.

</td>
</tr>
<tr>
<td>
FF_SWISS

</td>
<td>
Fonts with variable stroke width (proportionally spaced) and without serifs, such as Helvetica and Swiss.

</td>
</tr>
</table>

### -field usWinWeight

Specifies the weight of the font in the range 0 to 1000 (for example, 400 is normal and 700 is bold). This value is provided to the application in the <b>lfWeight</b> member of the Win32 LOGFONT structure.

### -field flInfo

Specifies additional information about the font. This field can be a combination of the following flag values:





#### FM_INFO_1BPP

Indicates that a glyph bitmap has a color depth of one bit per pixel. For Windows NT 3.1, the first version of Windows NT, this flag must be set.





#### FM_INFO_4BPP

Indicates that a glyph bitmap has a color depth of four bits per pixel. The driver should set this if the font supports antialiased glyph bitmaps with 16 levels of gray.





#### FM_INFO_8BPP

Indicates that a glyph bitmap has a color depth of eight bits per pixel. The current version of GDI will ignore this setting as it does not support color fonts.





#### FM_INFO_16BPP

Indicates that a glyph bitmap has a color depth of 16 bits per pixel. The current version of GDI will ignore this setting as it does not support color fonts.





#### FM_INFO_24BPP

Indicates that a glyph bitmap has a color depth of 24 bits per pixel. The current version of GDI will ignore this setting as it does not support color fonts.





#### FM_INFO_32BPP

Indicates that a glyph bitmap has a color depth of 32 bits per pixel. The current version of GDI will ignore this setting as it does not support color fonts.





#### FM_INFO_90DEGREE_ROTATIONS

Indicates that the font can be realized in 90 degree rotations of the original notional shape. GDI requests the rotation of a font by including the rotation in the notional to device transformation passed to the driver when creating the font. This member has meaning only when the FM_INFO_ARB_XFORMS flag has not been set.





#### FM_INFO_ANISOTROPIC_SCALING_ONLY

Indicates that the font supports only arbitrary anisotropic scaling. That is, transforms are equivalent to a diagonal matrix multiplied by a positive real number. If this flag is set, then the FM_INFO_ARB_XFORMS and the FM_INFO_ISOTROPIC_SCALING_ONLY flags cannot be set. If the FM_INFO_90DEGREE_ROTATIONS flag is also set, the font supports transformations that are a combination of a simple anisotropic scaling followed by a rotation by a multiple of 90 degrees.





#### FM_INFO_ARB_XFORMS

Indicates that a font can be realized under a continuous range of two dimensional linear transformations.





#### FM_INFO_CONSTANT_WIDTH

Indicates that all glyphs of the font under all realizations have the same value of character increment. If this flag is set, the FM_INFO_OPTICALLY_FIXED_PITCH flag must also be set.





#### FM_INFO_DBCS_FIXED_PITCH

Indicates that double-byte characters for this font are fixed pitch. Nothing is implied about single byte characters. This flag is meaningful only for fonts that support a double-byte character set (DBCS), such as shift JIS. Fonts that do not support a DBCS should not set this flag.





#### FM_INFO_DO_NOT_ENUMERATE

Indicates that this font will not be enumerated by the Win32 <b>EnumFontFamiliesEx</b>, <b>EnumFontFamilies</b> or <b>EnumFonts</b> routines. Moreover, the string returned to a Win32 application call to <b>GetTextFace</b> will be retrieved from the string <b>dpwszUniqueName</b>. This flag allows the font provider to associate more than one IFIMETRICS structure with one of its fonts.





#### FM_INFO_DSIG

Indicates that a font is compliant with the Unicode standard.





#### FM_INFO_FAMILY_EQUIV

Indicates that the <b>dpwszFamilyName</b> offset in IFIMETRICS is actually the offset to a list of equivalent family names or aliases. The first name is the base or real name; the subsequent names are equivalents or aliases. Each name in the list is null-terminated; the list is terminated by two zeros.


<dl>
<dt>&lt;base name&gt; &lt;0&gt; &lt;alias 1&gt; &lt;0&gt;...&lt;alias n&gt;</dt>
<dt>&lt;0&gt; &lt;0&gt;</dt>
</dl>


The based names are used only for mapping; they are not enumerated.





#### FM_INFO_IGNORE_TC_RA_ABLE

Indicates that, for this font, the TC_RA_ABLE flag is ignored.





#### FM_INFO_INTEGER_WIDTH

Indicates that all glyphs have nonfractional advance widths. Bitmap fonts usually set this flag.





#### FM_INFO_INTEGRAL_SCALING

Indicates that the font can be scaled by an integral amount in both the x and y directions. If this flag is set, then the driver must be able to render glyphs in the case where the notional to device transformation is scaled by integral amounts in the x and y directions. GDI requests the integral scaling of a font by including the axial scalings in the notional to device transformation passed to the driver when creating the font. This flag is meaningful only when the FM_INFO_ARB_XFORMS flag has not been set.





#### FM_INFO_ISOTROPIC_SCALING_ONLY

Indicates that the font supports arbitrary isotropic scaling only. That is, transforms are equivalent to the identity matrix multiplied by a positive real number. If this flag is set, then neither the FM_INFO_ARB_XFORMS nor the FM_INFO_ANISOTROPIC_SCALING_ONLY flags can be set. If the FM_INFO_90DEGREE_ROTATIONS flag is set, the font supports transformations equivalent to an isotropic scaling followed by a rotation by a multiple of 90 degrees.





#### FM_INFO_OPTICALLY_FIXED_PITCH

Indicates that this font is considered typographically as fixed pitch. This is an optical quality of the font and does not necessarily indicate that all the glyphs of the font have the same character increment.





#### FM_INFO_NONNEGATIVE_AC

Indicates that all glyphs of this font have nonnegative <i>a</i> and <i>c</i> spacing. That is, the glyph black box never extends outside the region bordered by the character origin and the character concatenation point.





#### FM_INFO_NOT_CONTIGUOUS

Indicates that the supported character set is not contiguous.





#### FM_INFO_RETURNS_BITMAPS

Indicates that the font contains a valid digital signature.





#### FM_INFO_RETURNS_OUTLINES

Indicates that for any glyph supported by the driver, GDI can request a <a href="/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a> structure that describes the outline of that glyph. If possible, when the outline is filled using GDI's path filling conventions, the resulting bitmap should be identical to the bitmap returned by the driver. The FM_INFO_RETURNS_OUTLINES and FM_INFO_RETURNS_STOKES flags cannot be set concurrently.





#### FM_INFO_RETURNS_STROKES

Indicates that for any glyph supported by the drivers, GDI can request a PATHOBJ structure that describes the spline of the glyph. This path cannot be filled but can be stroked to give a representation of the glyph. The FM_INFO_RETURNS_OUTLINES and FM_INFO_RETURNS_STOKES flags cannot be set concurrently.





#### FM_INFO_RIGHT_HANDED

Indicates that the ascent direction of the font is 90 degrees counterclockwise from the baseline direction. The ascent direction is the direction along which height is measured and is always perpendicular to the baseline direction.





#### FM_INFO_TECH_BITMAP

Indicates that the font is a bitmap font.





#### FM_INFO_TECH_CFF

Indicates that the font is a Pscript OpenType font that contains a Compact Font Format (CFF) table.





#### FM_INFO_TECH_MM

Indicates that this is a Multiple Master (MM) font.





#### FM_INFO_TECH_OUTLINE_NOT_TRUETYPE

Indicates that the font is based on a scalable font technology that uses outline paths, but is not based on TrueType. This flag does not specify whether the paths returned for this font should be filled or stroked; the consumer should examine the FM_INFO_RETURNS_STROKES and FM_INFO_RETURNS_OUTLINES flags for this information.





#### FM_INFO_TECH_STROKE

Indicates that the font is based on a stroked font technology. This flag does not specify whether the paths returned for this font should be filled or stroked; the consumer should examine the FM_INFO_RETURNS_STROKES and FM_INFO_RETURNS_OUTLINES flags for this information.





#### FM_INFO_TECH_TRUETYPE

Indicates that the font is a TrueType font.





#### FM_INFO_TECH_TYPE1

Indicates that this font is a PostScript screen font (either Type1 or OpenType PostScript).

### -field fsSelection

Specifies a combination of the following flags:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
FM_SEL_BOLD

</td>
<td>
Set if the characters of the font are bold.

</td>
</tr>
<tr>
<td>
FM_SEL_ITALIC

</td>
<td>
Set if the characters of the font are italic.

</td>
</tr>
<tr>
<td>
FM_SEL_NEGATIVE

</td>
<td>
Set if the characters of the font have the foreground and background reversed.

</td>
</tr>
<tr>
<td>
FM_SEL_OUTLINED

</td>
<td>
Set if the characters of the font are hollow.

</td>
</tr>
<tr>
<td>
FM_SEL_REGULAR

</td>
<td>
Set if the characters of the font are normal weight.

</td>
</tr>
<tr>
<td>
FM_SEL_STRIKEOUT

</td>
<td>
Set if the characters of the font are struck out by default; otherwise strikeouts must be simulated.

</td>
</tr>
<tr>
<td>
FM_SEL_UNDERSCORE

</td>
<td>
Set if all the characters of the font are underscored by default; otherwise underscoring must be simulated.

</td>
</tr>
</table>

### -field fsType

This is a TrueType-specific bitfield indicating certain properties for the font, such as font embedding and licensing rights for the font. Embeddable fonts can be stored in a document. When a document with embedded fonts is opened on a system that does not have the font installed (the remote system), the embedded font can be loaded for temporary (and in some cases permanent) use on that system by an embedding-aware application. Embedding licensing rights are granted by the font vendor. The following flags can be set:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
FM_EDITABLE_EMBED

</td>
<td>
Set if the font can be embedded and temporarily loaded on other systems. Documents containing Editable fonts can be opened for reading and writing.

</td>
</tr>
<tr>
<td>
FM_READONLY_EMBED

</td>
<td>
Set if read/write embedding is not permitted; only "preview and print" encapsulation is allowed. When this bit is set, the font can be embedded and temporarily loaded on the remote system. Documents containing "preview and print" fonts must be opened "read-only;" no edits can be applied to the document.

</td>
</tr>
<tr>
<td>

<dl>
<dt>FM_TYPE_LICENSED</dt>
<dt>FM_NO_EMBEDDING</dt>
</dl>


</td>
<td>
Set if the font is a Restricted License font. When only this bit is set, this font <i>must not be modified, embedded, or exchanged in any manner</i> without first obtaining permission of the legal owner. For Restricted License embedding to take effect, it must be the only level of embedding selected.

</td>
</tr>
</table>
 

Fonts with the FM_READONLY_EMBED bit set indicate that they can be embedded within documents but must only be installed <i>temporarily</i> on the remote system. Any document that includes an FM_READONLY_EMBED font must be opened "read-only." That is, the application can let the user view and/or print the document, but not edit it.

Fonts with the FM_EDITABLE_EMBED bit set indicate that they can be embedded in documents, but must only be installed <i>temporarily</i> on the remote system. In contrast to FM_READONLY_EMBED fonts, documents containing Editable fonts can be opened "read/write;" editing is permitted, and changes can be saved.

Fonts with no <b>fsType</b> bits set indicate that they can be embedded and permanently installed on the remote system by an application. The user of the remote system acquires the identical rights, obligations, and licenses for that font as the original purchaser of the font, and is subject to the same end-user license agreement, copyright, design patent, and/or trademark as was the original purchaser.

Applications that implement support for font embedding, either through use of the Font Embedding DLL or through other means, must not embed fonts that are not licensed to permit embedding. Further, applications loading embedded fonts for temporary use <i>must</i> delete the fonts when the document containing the embedded font is closed.

If multiple embedding bits are set, the <i>least</i> restrictive license granted takes precedence. For example, if bits 1 and 3 are set, bit 3 takes precedence over bit 1and the font can be embedded with Editable rights. For compatibility purposes, most vendors granting Editable embedding rights also set the Preview &amp; Print bit (0x000C). This permits an application that only supports Preview &amp; Print embedding to detect that font embedding is allowed.

### -field fwdUnitsPerEm

Specifies the em-height of the font.

### -field fwdLowestPPEm

Specifies the smallest readable size of the font, in pixels. This value is ignored for bitmap fonts.

### -field fwdWinAscender

Specifies the Windows ascender value for the font.

### -field fwdWinDescender

Specifies the Windows descender value for the font.

### -field fwdMacAscender

Specifies the Macintosh ascender value for the font.

### -field fwdMacDescender

Specifies the Macintosh descender value for the font. This number is typically less than zero. It measures the signed displacement from the base line of the lowest descender in the Macintosh character set.

### -field fwdMacLineGap

Specifies the Macintosh line gap for the font. The suggested Macintosh interline spacing is equal to <b>fwdMacLineGap</b> + <b>fwdMacAscender</b> − <b>fwdMacDescender</b>.

### -field fwdTypoAscender

Specifies the typographic ascender value for the font.

### -field fwdTypoDescender

Specifies the typographic descender value for the font. This value specifies the signed displacement of the lowest descender from the baseline.

### -field fwdTypoLineGap

Specifies the typographic line gap for the font.

### -field fwdAveCharWidth

Specifies the arithmetic average of the width of all of the 26 lower case letters 'a' through 'z' of the Latin alphabet and the space character. If any of the 26 lowercase letters are not present, then this member should be set equal to the weighted average of all glyphs in the font.

### -field fwdMaxCharInc

Specifies the maximum character increment of all glyphs in the font.

### -field fwdCapHeight

Specifies the height of the optical line describing the top of the uppercase 'H' in font units (FUnits). This might not be the same as the measured height of the uppercase 'H.' If this information does not exist, <b>fwdCapHeight</b> should be set to zero, which indicates that it is undefined.

### -field fwdXHeight

Specifies the height of the optical line describing the height of the lowercase 'x' in font units. This might not be the same as the measured height of the lowercase 'x.' A value of zero indicates that this member is undefined.

### -field fwdSubscriptXSize

Specifies the suggested character width (the size along the baseline direction) of the subscript font.

### -field fwdSubscriptYSize

Specifies the suggested character height (the size along the ascender direction) of the subscript font.

### -field fwdSubscriptXOffset

Specifies the suggested offset in the baseline direction of the subscript character. The offset is with respect to the character origin of the base character.

### -field fwdSubscriptYOffset

Specifies the suggested offset in the baseline direction of the subscript character. The offset is taken from the character origin of the base character.

### -field fwdSuperscriptXSize

Specifies the suggested character width (the size along the baseline direction) of the superscript font.

### -field fwdSuperscriptYSize

Specifies the suggested character height (the size along the ascender direction) of the superscript font.

### -field fwdSuperscriptXOffset

Specifies the suggested offset in the baseline direction of the superscript character. The offset is taken from the character origin of the base character.

### -field fwdSuperscriptYOffset

Specifies the suggested offset in the baseline direction of the superscript character. The offset is taken from the character origin of the base character.

### -field fwdUnderscoreSize

Specifies the suggested width of the underscore bar, in font units.

### -field fwdUnderscorePosition

Specifies the suggested displacement, in font units, from the base line to the middle of the underscore bar.

### -field fwdStrikeoutSize

Specifies the suggested width of the strike-out bar, in font coordinates.

### -field fwdStrikeoutPosition

Specifies the suggested displacement of the middle of the strikeout bar from the baseline.

### -field chFirstChar

Specifies the lowest supported character in the code page specified in <b>jWinCharSet</b>. This field is provided for Windows 3.1 compatibility.

### -field chLastChar

Specifies the highest supported character in the code page specified in <b>jWinCharSet</b>. This field is provided for Windows 3.1 compatibility.

### -field chDefaultChar

Specifies the default character in the code page specified in <b>jWinCharSet</b>. This field is provided for Windows 3.1 compatibility.

### -field chBreakChar

Specifies the break character in the code page specified in <b>jWinCharSet</b>. This field is provided for Windows 3.1 compatibility.

### -field wcFirstChar

Specifies the supported character with the smallest Unicode character code.

### -field wcLastChar

Specifies the supported character with the largest Unicode character code.

### -field wcDefaultChar

Specifies the character to be substituted when an application requests a character that is not supported by the font.

### -field wcBreakChar

Specifies the code point of the space character or its equivalent.

### -field ptlBaseline

Specifies a <a href="/windows/desktop/api/windef/ns-windef-pointl">POINTL</a> structure that contains the intended writing direction of this font. For example, a typical Latin font specifies a value of (1,0).

### -field ptlAspect

Specifies a POINTL structure that contains the aspect ratio of the pixel centers for which the bitmap font was designed. This value is used only by bitmap fonts.

### -field ptlCaret

Specifies a POINTL structure that contains the direction of the ascender direction of the font. For example, the value for a nonitalicized Latin font is (0,1) while an italicized Latin font might specify a value of (2,5).

### -field rclFontBox

Specifies a <a href="/windows/desktop/api/windef/ns-windef-rectl">RECTL</a> structure that describes the bounding box of all glyphs in the font in design space.

### -field achVendId

Specifies a four character identifier for the font vendor. Identifiers are documented in the Microsoft TrueType specification.

### -field cKerningPairs

Specifies the number of kerning pairs associated with this font.

### -field ulPanoseCulture

Specifies the manner in which to interpret the panose number. This number should be set to FM_PANOSE_CULTURE_LATIN for Latin-based fonts. See the Microsoft Window SDK documentation for information about the PANOSE structure.

### -field panose

Is an array of 10 bytes used to describe the visual characteristics of a given typeface. These characteristics are then used to associate the font with other fonts of similar appearance having different names. See the Window SDK documentation for information about the PANOSE structure.

### -field Align

<i>This member is defined only if the _WIN64 constant is defined</i>. Its only purpose is to ensure that this structure is aligned correctly under the Itanium architecture.

## -remarks

Additional information for a typeface can optionally be specified in the <a href="/windows/desktop/api/winddi/ns-winddi-ifiextra">IFIEXTRA</a> structure.

A driver's <a href="/windows/desktop/api/winddi/nf-winddi-drvqueryfont">DrvQueryFont</a> routine fills out and returns an IFIMETRICS structure to GDI.

The IFIMETRICS structure defines all the information for a typeface that GDI understands. Most of the members are FWORD values, which are signed 16-bit quantities in design space. If the font is a raster font, design space and device space are the same and a font unit is equivalent to the distance between pixels.

The coordinate system in the font/notional space is such that the y coordinate increases in an upward direction and the x coordinate increases to the right.

The IFIMETRICS structure's <b>Align</b> member causes it to be larger for x64 machines than for x32 machines, which has ramifications for binary font format files formatted according to this structure. Starting with Windows Server 2003 SP1, an additional, fixed-size structure has been added to Prntfont.h: <a href="/windows-hardware/drivers/ddi/content/prntfont/ns-prntfont-_printifi32">PRINTIFI32</a>. The PRINTIFI32 structure is identical to the IFIMETRICS structure, except that it does not contain an <b>Align</b> member.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvqueryfont">DrvQueryFont</a>



<a href="/windows/desktop/api/winddi/ns-winddi-ifiextra">IFIEXTRA</a>



<a href="/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a>
