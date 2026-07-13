---
UID: NF:wingdi.CreateFontA
title: CreateFontA function (wingdi.h)
description: The CreateFont function creates a logical font with the specified characteristics. The logical font can subsequently be selected as the font for any device. (ANSI)
helpviewer_keywords: ["ANTIALIASED_QUALITY", "CLEARTYPE_QUALITY", "CLIP_CHARACTER_PRECIS", "CLIP_DEFAULT_PRECIS", "CLIP_DFA_DISABLE", "CLIP_DFA_OVERRIDE", "CLIP_EMBEDDED", "CLIP_LH_ANGLES", "CLIP_MASK", "CLIP_STROKE_PRECIS", "CLIP_TT_ALWAYS", "CreateFontA", "DEFAULT_QUALITY", "DRAFT_QUALITY", "FF_DECORATIVE", "FF_DONTCARE", "FF_MODERN", "FF_ROMAN", "FF_SCRIPT", "FF_SWISS", "FW_BLACK", "FW_BOLD", "FW_DEMIBOLD", "FW_DONTCARE", "FW_EXTRABOLD", "FW_EXTRALIGHT", "FW_HEAVY", "FW_LIGHT", "FW_MEDIUM", "FW_NORMAL", "FW_REGULAR", "FW_SEMIBOLD", "FW_THIN", "FW_ULTRABOLD", "FW_ULTRALIGHT", "NONANTIALIASED_QUALITY", "OUT_CHARACTER_PRECIS", "OUT_DEFAULT_PRECIS", "OUT_DEVICE_PRECIS", "OUT_OUTLINE_PRECIS", "OUT_PS_ONLY_PRECIS", "OUT_RASTER_PRECIS", "OUT_STRING_PRECIS", "OUT_STROKE_PRECIS", "OUT_TT_ONLY_PRECIS", "OUT_TT_PRECIS", "PROOF_QUALITY", "wingdi/CreateFontA"]
old-location: gdi\createfont.htm
tech.root: gdi
ms.assetid: 373bac6e-5d4d-4909-8096-2f0e909d2f1d
ms.date: 12/05/2018
ms.keywords: ANTIALIASED_QUALITY, CLEARTYPE_QUALITY, CLIP_CHARACTER_PRECIS, CLIP_DEFAULT_PRECIS, CLIP_DFA_DISABLE, CLIP_DFA_OVERRIDE, CLIP_EMBEDDED, CLIP_LH_ANGLES, CLIP_MASK, CLIP_STROKE_PRECIS, CLIP_TT_ALWAYS, CreateFont, CreateFont function [Windows GDI], CreateFontA, CreateFontW, DEFAULT_QUALITY, DRAFT_QUALITY, FF_DECORATIVE, FF_DONTCARE, FF_MODERN, FF_ROMAN, FF_SCRIPT, FF_SWISS, FW_BLACK, FW_BOLD, FW_DEMIBOLD, FW_DONTCARE, FW_EXTRABOLD, FW_EXTRALIGHT, FW_HEAVY, FW_LIGHT, FW_MEDIUM, FW_NORMAL, FW_REGULAR, FW_SEMIBOLD, FW_THIN, FW_ULTRABOLD, FW_ULTRALIGHT, NONANTIALIASED_QUALITY, OUT_CHARACTER_PRECIS, OUT_DEFAULT_PRECIS, OUT_DEVICE_PRECIS, OUT_OUTLINE_PRECIS, OUT_PS_ONLY_PRECIS, OUT_RASTER_PRECIS, OUT_STRING_PRECIS, OUT_STROKE_PRECIS, OUT_TT_ONLY_PRECIS, OUT_TT_PRECIS, PROOF_QUALITY, _win32_CreateFont, gdi.createfont, wingdi/CreateFont, wingdi/CreateFontA, wingdi/CreateFontW
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateFontW (Unicode) and CreateFontA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateFontA
 - wingdi/CreateFontA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - ext-ms-win-gdi-font-l1-1-2.dll
 - Ext-MS-Win-GDI-Font-L1-1-3.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - CreateFont
 - CreateFontA
 - CreateFontW
---

# CreateFontA function


## -description

The <b>CreateFont</b> function creates a logical font with the specified characteristics. The logical font can subsequently be selected as the font for any device.

## -parameters

### -param cHeight [in]

The height, in logical units, of the font's character cell or character. The character height value (also known as the em height) is the character cell height value minus the internal-leading value. The font mapper interprets the value specified in <i>nHeight</i> in the following manner.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>&gt; 0</dt>
</dl>
</td>
<td width="60%">
The font mapper transforms this value into device units and matches it against the cell height of the available fonts.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The font mapper uses a default height value when it searches for a match.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>&lt; 0</dt>
</dl>
</td>
<td width="60%">
The font mapper transforms this value into device units and matches its absolute value against the character height of the available fonts.

</td>
</tr>
</table>
 

For all height comparisons, the font mapper looks for the largest font that does not exceed the requested size.

This mapping occurs when the font is used for the first time.

For the MM_TEXT mapping mode, you can use the following formula to specify a height for a font with a specified point size:


```cpp

nHeight = -MulDiv(PointSize, GetDeviceCaps(hDC, LOGPIXELSY), 72);

```

### -param cWidth [in]

The average width, in logical units, of characters in the requested font. If this value is zero, the font mapper chooses a closest match value. The closest match value is determined by comparing the absolute values of the difference between the current device's aspect ratio and the digitized aspect ratio of available fonts.

### -param cEscapement [in]

The angle, in tenths of degrees, between the escapement vector and the x-axis of the device. The escapement vector is parallel to the base line of a row of text.

When the graphics mode is set to GM_ADVANCED, you can specify the escapement angle of the string independently of the orientation angle of the string's characters.

When the graphics mode is set to GM_COMPATIBLE, <i>nEscapement</i> specifies both the escapement and orientation. You should set <i>nEscapement</i> and <i>nOrientation</i> to the same value.

### -param cOrientation [in]

The angle, in tenths of degrees, between each character's base line and the x-axis of the device.

### -param cWeight [in]

The weight of the font in the range 0 through 1000. For example, 400 is normal and 700 is bold. If this value is zero, a default weight is used.

The following values are defined for convenience.

<table>
<tr>
<th>Weight</th>
<th>Value</th>
</tr>
<tr>
<td width="40%"><a id="FW_DONTCARE"></a><a id="fw_dontcare"></a><dl>
<dt><b>FW_DONTCARE</b></dt>
</dl>
</td>
<td width="60%">
0

</td>
</tr>
<tr>
<td width="40%"><a id="FW_THIN"></a><a id="fw_thin"></a><dl>
<dt><b>FW_THIN</b></dt>
</dl>
</td>
<td width="60%">
100

</td>
</tr>
<tr>
<td width="40%"><a id="FW_EXTRALIGHT"></a><a id="fw_extralight"></a><dl>
<dt><b>FW_EXTRALIGHT</b></dt>
</dl>
</td>
<td width="60%">
200

</td>
</tr>
<tr>
<td width="40%"><a id="FW_ULTRALIGHT"></a><a id="fw_ultralight"></a><dl>
<dt><b>FW_ULTRALIGHT</b></dt>
</dl>
</td>
<td width="60%">
200

</td>
</tr>
<tr>
<td width="40%"><a id="FW_LIGHT"></a><a id="fw_light"></a><dl>
<dt><b>FW_LIGHT</b></dt>
</dl>
</td>
<td width="60%">
300

</td>
</tr>
<tr>
<td width="40%"><a id="FW_NORMAL"></a><a id="fw_normal"></a><dl>
<dt><b>FW_NORMAL</b></dt>
</dl>
</td>
<td width="60%">
400

</td>
</tr>
<tr>
<td width="40%"><a id="FW_REGULAR"></a><a id="fw_regular"></a><dl>
<dt><b>FW_REGULAR</b></dt>
</dl>
</td>
<td width="60%">
400

</td>
</tr>
<tr>
<td width="40%"><a id="FW_MEDIUM"></a><a id="fw_medium"></a><dl>
<dt><b>FW_MEDIUM</b></dt>
</dl>
</td>
<td width="60%">
500

</td>
</tr>
<tr>
<td width="40%"><a id="FW_SEMIBOLD"></a><a id="fw_semibold"></a><dl>
<dt><b>FW_SEMIBOLD</b></dt>
</dl>
</td>
<td width="60%">
600

</td>
</tr>
<tr>
<td width="40%"><a id="FW_DEMIBOLD"></a><a id="fw_demibold"></a><dl>
<dt><b>FW_DEMIBOLD</b></dt>
</dl>
</td>
<td width="60%">
600

</td>
</tr>
<tr>
<td width="40%"><a id="FW_BOLD"></a><a id="fw_bold"></a><dl>
<dt><b>FW_BOLD</b></dt>
</dl>
</td>
<td width="60%">
700

</td>
</tr>
<tr>
<td width="40%"><a id="FW_EXTRABOLD"></a><a id="fw_extrabold"></a><dl>
<dt><b>FW_EXTRABOLD</b></dt>
</dl>
</td>
<td width="60%">
800

</td>
</tr>
<tr>
<td width="40%"><a id="FW_ULTRABOLD"></a><a id="fw_ultrabold"></a><dl>
<dt><b>FW_ULTRABOLD</b></dt>
</dl>
</td>
<td width="60%">
800

</td>
</tr>
<tr>
<td width="40%"><a id="FW_HEAVY"></a><a id="fw_heavy"></a><dl>
<dt><b>FW_HEAVY</b></dt>
</dl>
</td>
<td width="60%">
900

</td>
</tr>
<tr>
<td width="40%"><a id="FW_BLACK"></a><a id="fw_black"></a><dl>
<dt><b>FW_BLACK</b></dt>
</dl>
</td>
<td width="60%">
900

</td>
</tr>
</table>

### -param bItalic [in]

Specifies an italic font if set to <b>TRUE</b>.

### -param bUnderline [in]

Specifies an underlined font if set to <b>TRUE</b>.

### -param bStrikeOut [in]

A strikeout font if set to <b>TRUE</b>.

### -param iCharSet [in]

The character set. For a list of possible values, see *lfCharSet* field of the <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT structure</a>.

Fonts with other character sets may exist in the operating system. If an application uses a font with an unknown character set, it should not attempt to translate or interpret strings that are rendered with that font.

To ensure consistent results when creating a font, do not specify **OEM_CHARSET** or **DEFAULT_CHARSET**. If you specify a typeface name in the *pszFaceName* parameter, make sure that the *iCharSet* value matches the character set of the typeface specified in *pszFaceName*.

### -param iOutPrecision [in]

The output precision. The output precision defines how closely the output must match the requested font's height, width, character orientation, escapement, pitch, and font type. It can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="OUT_CHARACTER_PRECIS"></a><a id="out_character_precis"></a><dl>
<dt><b>OUT_CHARACTER_PRECIS</b></dt>
</dl>
</td>
<td width="60%">
Not used.

</td>
</tr>
<tr>
<td width="40%"><a id="OUT_DEFAULT_PRECIS"></a><a id="out_default_precis"></a><dl>
<dt><b>OUT_DEFAULT_PRECIS</b></dt>
</dl>
</td>
<td width="60%">
The default font mapper behavior.

</td>
</tr>
<tr>
<td width="40%"><a id="OUT_DEVICE_PRECIS"></a><a id="out_device_precis"></a><dl>
<dt><b>OUT_DEVICE_PRECIS</b></dt>
</dl>
</td>
<td width="60%">
Instructs the font mapper to choose a Device font when the system contains multiple fonts with the same name.

</td>
</tr>
<tr>
<td width="40%"><a id="OUT_OUTLINE_PRECIS"></a><a id="out_outline_precis"></a><dl>
<dt><b>OUT_OUTLINE_PRECIS</b></dt>
</dl>
</td>
<td width="60%">
This value instructs the font mapper to choose from TrueType and other outline-based fonts.

</td>
</tr>
<tr>
<td width="40%"><a id="OUT_PS_ONLY_PRECIS"></a><a id="out_ps_only_precis"></a><dl>
<dt><b>OUT_PS_ONLY_PRECIS</b></dt>
</dl>
</td>
<td width="60%">
Instructs the font mapper to choose from only PostScript fonts. If there are no PostScript fonts installed in the system, the font mapper returns to default behavior.

</td>
</tr>
<tr>
<td width="40%"><a id="OUT_RASTER_PRECIS"></a><a id="out_raster_precis"></a><dl>
<dt><b>OUT_RASTER_PRECIS</b></dt>
</dl>
</td>
<td width="60%">
Instructs the font mapper to choose a raster font when the system contains multiple fonts with the same name.

</td>
</tr>
<tr>
<td width="40%"><a id="OUT_STRING_PRECIS"></a><a id="out_string_precis"></a><dl>
<dt><b>OUT_STRING_PRECIS</b></dt>
</dl>
</td>
<td width="60%">
This value is not used by the font mapper, but it is returned when raster fonts are enumerated.

</td>
</tr>
<tr>
<td width="40%"><a id="OUT_STROKE_PRECIS"></a><a id="out_stroke_precis"></a><dl>
<dt><b>OUT_STROKE_PRECIS</b></dt>
</dl>
</td>
<td width="60%">
This value is not used by the font mapper, but it is returned when TrueType, other outline-based fonts, and vector fonts are enumerated.

</td>
</tr>
<tr>
<td width="40%"><a id="OUT_TT_ONLY_PRECIS"></a><a id="out_tt_only_precis"></a><dl>
<dt><b>OUT_TT_ONLY_PRECIS</b></dt>
</dl>
</td>
<td width="60%">
Instructs the font mapper to choose from only TrueType fonts. If there are no TrueType fonts installed in the system, the font mapper returns to default behavior.

</td>
</tr>
<tr>
<td width="40%"><a id="OUT_TT_PRECIS"></a><a id="out_tt_precis"></a><dl>
<dt><b>OUT_TT_PRECIS</b></dt>
</dl>
</td>
<td width="60%">
Instructs the font mapper to choose a TrueType font when the system contains multiple fonts with the same name.

</td>
</tr>
</table>
 

Applications can use the OUT_DEVICE_PRECIS, OUT_RASTER_PRECIS, OUT_TT_PRECIS, and OUT_PS_ONLY_PRECIS values to control how the font mapper chooses a font when the operating system contains more than one font with a specified name. For example, if an operating system contains a font named Symbol in raster and TrueType form, specifying OUT_TT_PRECIS forces the font mapper to choose the TrueType version. Specifying OUT_TT_ONLY_PRECIS forces the font mapper to choose a TrueType font, even if it must substitute a TrueType font of another name.

### -param iClipPrecision [in]

The clipping precision. The clipping precision defines how to clip characters that are partially outside the clipping region. It can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CLIP_CHARACTER_PRECIS"></a><a id="clip_character_precis"></a><dl>
<dt><b>CLIP_CHARACTER_PRECIS</b></dt>
</dl>
</td>
<td width="60%">
Not used.

</td>
</tr>
<tr>
<td width="40%"><a id="CLIP_DEFAULT_PRECIS"></a><a id="clip_default_precis"></a><dl>
<dt><b>CLIP_DEFAULT_PRECIS</b></dt>
</dl>
</td>
<td width="60%">
Specifies default clipping behavior.

</td>
</tr>
<tr>
<td width="40%"><a id="CLIP_DFA_DISABLE"></a><a id="clip_dfa_disable"></a><dl>
<dt><b>CLIP_DFA_DISABLE</b></dt>
</dl>
</td>
<td width="60%">
Windows XP SP1: Turns off font association for the font. Note that this flag is not guaranteed to have any effect on any platform after Windows Server 2003.

</td>
</tr>
<tr>
<td width="40%"><a id="CLIP_EMBEDDED"></a><a id="clip_embedded"></a><dl>
<dt><b>CLIP_EMBEDDED</b></dt>
</dl>
</td>
<td width="60%">
You must specify this flag to use an embedded read-only font.

</td>
</tr>
<tr>
<td width="40%"><a id="CLIP_LH_ANGLES"></a><a id="clip_lh_angles"></a><dl>
<dt><b>CLIP_LH_ANGLES</b></dt>
</dl>
</td>
<td width="60%">
When this value is used, the rotation for all fonts depends on whether the orientation of the coordinate system is left-handed or right-handed.

If not used, device fonts always rotate counterclockwise, but the rotation of other fonts is dependent on the orientation of the coordinate system.

For more information about the orientation of coordinate systems, see the description of the <i>nOrientation</i> parameter

</td>
</tr>
<tr>
<td width="40%"><a id="CLIP_MASK"></a><a id="clip_mask"></a><dl>
<dt><b>CLIP_MASK</b></dt>
</dl>
</td>
<td width="60%">
Not used.

</td>
</tr>
<tr>
<td width="40%"><a id="CLIP_DFA_OVERRIDE"></a><a id="clip_dfa_override"></a><dl>
<dt><b>CLIP_DFA_OVERRIDE</b></dt>
</dl>
</td>
<td width="60%">
Turns off font association for the font. This is identical to CLIP_DFA_DISABLE, but it can have problems in some situations; the recommended flag to use is CLIP_DFA_DISABLE.

</td>
</tr>
<tr>
<td width="40%"><a id="CLIP_STROKE_PRECIS"></a><a id="clip_stroke_precis"></a><dl>
<dt><b>CLIP_STROKE_PRECIS</b></dt>
</dl>
</td>
<td width="60%">
Not used by the font mapper, but is returned when raster, vector, or TrueType fonts are enumerated.

For compatibility, this value is always returned when enumerating fonts.

</td>
</tr>
<tr>
<td width="40%"><a id="CLIP_TT_ALWAYS"></a><a id="clip_tt_always"></a><dl>
<dt><b>CLIP_TT_ALWAYS</b></dt>
</dl>
</td>
<td width="60%">
Not used.

</td>
</tr>
</table>

### -param iQuality [in]

The output quality. The output quality defines how carefully GDI must attempt to match the logical-font attributes to those of an actual physical font. It can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ANTIALIASED_QUALITY"></a><a id="antialiased_quality"></a><dl>
<dt><b>ANTIALIASED_QUALITY</b></dt>
</dl>
</td>
<td width="60%">
Font is antialiased, or smoothed, if the font supports it and the size of the font is not too small or too large.

</td>
</tr>
<tr>
<td width="40%"><a id="CLEARTYPE_QUALITY"></a><a id="cleartype_quality"></a><dl>
<dt><b>CLEARTYPE_QUALITY</b></dt>
</dl>
</td>
<td width="60%">
If set, text is rendered (when possible) using ClearType antialiasing method. See Remarks for more information.

</td>
</tr>
<tr>
<td width="40%"><a id="DEFAULT_QUALITY"></a><a id="default_quality"></a><dl>
<dt><b>DEFAULT_QUALITY</b></dt>
</dl>
</td>
<td width="60%">
Appearance of the font does not matter.

</td>
</tr>
<tr>
<td width="40%"><a id="DRAFT_QUALITY"></a><a id="draft_quality"></a><dl>
<dt><b>DRAFT_QUALITY</b></dt>
</dl>
</td>
<td width="60%">
Appearance of the font is less important than when the PROOF_QUALITY value is used. For GDI raster fonts, scaling is enabled, which means that more font sizes are available, but the quality may be lower. Bold, italic, underline, and strikeout fonts are synthesized, if necessary.

</td>
</tr>
<tr>
<td width="40%"><a id="NONANTIALIASED_QUALITY"></a><a id="nonantialiased_quality"></a><dl>
<dt><b>NONANTIALIASED_QUALITY</b></dt>
</dl>
</td>
<td width="60%">
Font is never antialiased, that is, font smoothing is not done.

</td>
</tr>
<tr>
<td width="40%"><a id="PROOF_QUALITY"></a><a id="proof_quality"></a><dl>
<dt><b>PROOF_QUALITY</b></dt>
</dl>
</td>
<td width="60%">
Character quality of the font is more important than exact matching of the logical-font attributes. For GDI raster fonts, scaling is disabled and the font closest in size is chosen. Although the chosen font size may not be mapped exactly when PROOF_QUALITY is used, the quality of the font is high and there is no distortion of appearance. Bold, italic, underline, and strikeout fonts are synthesized, if necessary.

</td>
</tr>
</table>
 

If the output quality is DEFAULT_QUALITY, DRAFT_QUALITY, or PROOF_QUALITY, then the font is antialiased if the SPI_GETFONTSMOOTHING system parameter is <b>TRUE</b>. Users can control this system parameter from the Control Panel. (The precise wording of the setting in the Control panel depends on the version of Windows, but it will be words to the effect of "Smooth edges of screen fonts".)

### -param iPitchAndFamily [in]

The pitch and family of the font. The two low-order bits specify the pitch of the font and can be one of the following values:

<ul>
<li>DEFAULT_PITCH</li>
<li>FIXED_PITCH</li>
<li>VARIABLE_PITCH</li>
</ul>
The four high-order bits specify the font family and can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FF_DECORATIVE"></a><a id="ff_decorative"></a><dl>
<dt><b>FF_DECORATIVE</b></dt>
</dl>
</td>
<td width="60%">
Novelty fonts. Old English is an example.

</td>
</tr>
<tr>
<td width="40%"><a id="FF_DONTCARE"></a><a id="ff_dontcare"></a><dl>
<dt><b>FF_DONTCARE</b></dt>
</dl>
</td>
<td width="60%">
Use default font.

</td>
</tr>
<tr>
<td width="40%"><a id="FF_MODERN"></a><a id="ff_modern"></a><dl>
<dt><b>FF_MODERN</b></dt>
</dl>
</td>
<td width="60%">
Fonts with constant stroke width, with or without serifs. Pica, Elite, and Courier New are examples.

</td>
</tr>
<tr>
<td width="40%"><a id="FF_ROMAN"></a><a id="ff_roman"></a><dl>
<dt><b>FF_ROMAN</b></dt>
</dl>
</td>
<td width="60%">
Fonts with variable stroke width and with serifs. MS Serif is an example.

</td>
</tr>
<tr>
<td width="40%"><a id="FF_SCRIPT"></a><a id="ff_script"></a><dl>
<dt><b>FF_SCRIPT</b></dt>
</dl>
</td>
<td width="60%">
Fonts designed to look like handwriting. Script and Cursive are examples.

</td>
</tr>
<tr>
<td width="40%"><a id="FF_SWISS"></a><a id="ff_swiss"></a><dl>
<dt><b>FF_SWISS</b></dt>
</dl>
</td>
<td width="60%">
Fonts with variable stroke width and without serifs. MS?Sans Serif is an example.

</td>
</tr>
</table>
 

An application can specify a value for the <i>fdwPitchAndFamily</i> parameter by using the Boolean OR operator to join a pitch constant with a family constant.

Font families describe the look of a font in a general way. They are intended for specifying fonts when the exact typeface requested is not available.

### -param pszFaceName [in]

A pointer to a null-terminated string that specifies the typeface name of the font. The length of this string must not exceed 32 characters, including the terminating null character. The <a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesa">EnumFontFamilies</a> function can be used to enumerate the typeface names of all currently available fonts. For more information, see the Remarks.

If <i>pszFaceName</i> is <b>NULL</b> or empty string, GDI uses the first font that matches the other specified attributes.

## -returns

If the function succeeds, the return value is a handle to a logical font.

If the function fails, the return value is <b>NULL</b>.

## -remarks

When you no longer need the font, call the <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> function to delete it.

To help protect the copyrights of vendors who provide fonts for Windows, applications should always report the exact name of a selected font. Because available fonts can vary from system to system, do not assume that the selected font is always the same as the requested font. For example, if you request a font named Palatino, but no such font is available on the system, the font mapper will substitute a font that has similar attributes but a different name. Always report the name of the selected font to the user.

To get the appropriate font on different language versions of the OS, call <a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesexa">EnumFontFamiliesEx</a> with the desired font characteristics in the <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure, then retrieve the appropriate typeface name and create the font using <b>CreateFont</b> or <a href="/windows/desktop/api/wingdi/nf-wingdi-createfontindirecta">CreateFontIndirect</a>.

The font mapper for <b>CreateFont</b>,<a href="/windows/desktop/api/wingdi/nf-wingdi-createfontindirecta">CreateFontIndirect</a>, and <a href="/windows/desktop/api/wingdi/nf-wingdi-createfontindirectexa">CreateFontIndirectEx</a> recognizes both the English and the localized typeface name, regardless of locale.

The following situations do not support ClearType antialiasing:

<ul>
<li>Text rendered on a printer.</li>
<li>A display set for 256 colors or less.</li>
<li>Text rendered to a terminal server client.</li>
<li>The font is not a TrueType font or an OpenType font with TrueType outlines. For example, the following do not support ClearType antialiasing: Type 1 fonts, Postscript OpenType fonts without TrueType outlines, bitmap fonts, vector fonts, and device fonts.</li>
<li>The font has tuned embedded bitmaps, only for the font sizes that contain the embedded bitmaps. For example, this occurs commonly in East Asian fonts.</li>
</ul>

#### Examples


```cpp
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;
    switch (message)
    {
    
    
    case WM_PAINT:
        {
        RECT rect;
        HFONT hFontOriginal, hFont1, hFont2, hFont3;
        hdc = BeginPaint(hWnd, &ps);

            
            //Logical units are device dependent pixels, so this will create a handle to a logical font that is 48 pixels in height.
            //The width, when set to 0, will cause the font mapper to choose the closest matching value.
            //The font face name will be Impact.
            hFont1 = CreateFont(48,0,0,0,FW_DONTCARE,FALSE,TRUE,FALSE,DEFAULT_CHARSET,OUT_OUTLINE_PRECIS,
                CLIP_DEFAULT_PRECIS,CLEARTYPE_QUALITY, VARIABLE_PITCH,TEXT("Impact"));
            hFontOriginal = (HFONT)SelectObject(hdc, hFont1);
            
            //Sets the coordinates for the rectangle in which the text is to be formatted.
            SetRect(&rect, 100,100,700,200);
            SetTextColor(hdc, RGB(255,0,0));
            DrawText(hdc, TEXT("Drawing Text with Impact"), -1,&rect, DT_NOCLIP);
            
            //Logical units are device dependent pixels, so this will create a handle to a logical font that is 36 pixels in height.
            //The width, when set to 20, will cause the font mapper to choose a font which, in this case, is stretched.
            //The font face name will be Times New Roman.  This time nEscapement is at -300 tenths of a degree (-30 degrees)
            hFont2 = CreateFont(36,20,-300,0,FW_DONTCARE,FALSE,TRUE,FALSE,DEFAULT_CHARSET,OUT_OUTLINE_PRECIS,
                CLIP_DEFAULT_PRECIS,CLEARTYPE_QUALITY, VARIABLE_PITCH,TEXT("Times New Roman"));
            SelectObject(hdc,hFont2);
            
            //Sets the coordinates for the rectangle in which the text is to be formatted.
            SetRect(&rect, 100, 200, 900, 800);
            SetTextColor(hdc, RGB(0,128,0));
            DrawText(hdc, TEXT("Drawing Text with Times New Roman"), -1,&rect, DT_NOCLIP);
                
            //Logical units are device dependent pixels, so this will create a handle to a logical font that is 36 pixels in height.
            //The width, when set to 10, will cause the font mapper to choose a font which, in this case, is compressed. 
            //The font face name will be Arial. This time nEscapement is at 250 tenths of a degree (25 degrees)
            hFont3 = CreateFont(36,10,250,0,FW_DONTCARE,FALSE,TRUE,FALSE,DEFAULT_CHARSET,OUT_OUTLINE_PRECIS,
                CLIP_DEFAULT_PRECIS,ANTIALIASED_QUALITY, VARIABLE_PITCH,TEXT("Arial"));
            SelectObject(hdc,hFont3);

            //Sets the coordinates for the rectangle in which the text is to be formatted.
            SetRect(&rect, 500, 200, 1400, 600);
            SetTextColor(hdc, RGB(0,0,255));
            DrawText(hdc, TEXT("Drawing Text with Arial"), -1,&rect, DT_NOCLIP);

            SelectObject(hdc,hFontOriginal);
            DeleteObject(hFont1);
            DeleteObject(hFont2);
            DeleteObject(hFont3);
        
        EndPaint(hWnd, &ps);
        break;
        }
    case WM_DESTROY:
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}

```


For another example, see "Setting Fonts for Menu-Item Text Strings" in <a href="/windows/desktop/menurc/using-menus">Using Menus</a>.

<div class="code"></div>




> [!NOTE]
> The wingdi.h header defines CreateFont as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-createfontindirecta">CreateFontIndirect</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createfontindirectexa">CreateFontIndirectEx</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>



<b>EnumFontFamilies</b>



<a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesexa">EnumFontFamiliesEx</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontsa">EnumFonts</a>



<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a>
