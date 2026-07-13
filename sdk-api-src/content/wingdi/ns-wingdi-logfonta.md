---
UID: NS:wingdi.tagLOGFONTA
title: LOGFONTA (wingdi.h)
description: The LOGFONT structure defines the attributes of a font. (ANSI)
helpviewer_keywords: ["*LPLOGFONTA","*NPLOGFONTA","*PLOGFONTA","LOGFONT","LOGFONT structure [Windows GDI]","LOGFONTA","LOGFONTW","PLOGFONT","PLOGFONT structure pointer [Windows GDI]","_win32_LOGFONT_str","gdi.logfont","wingdi/LOGFONT","wingdi/LOGFONTA","wingdi/LOGFONTW","wingdi/PLOGFONT"]
old-location: gdi\logfont.htm
tech.root: gdi
ms.assetid: 57658a03-0a6d-4a28-a7c1-c65ec145beb4
ms.date: 12/05/2018
ms.keywords: '*LPLOGFONTA, *NPLOGFONTA, *PLOGFONTA, LOGFONT, LOGFONT structure [Windows GDI], LOGFONTA, LOGFONTW, PLOGFONT, PLOGFONT structure pointer [Windows GDI], _win32_LOGFONT_str, gdi.logfont, wingdi/LOGFONT, wingdi/LOGFONTA, wingdi/LOGFONTW, wingdi/PLOGFONT'
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LOGFONTW (Unicode) and LOGFONTA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: LOGFONTA, *PLOGFONTA, *NPLOGFONTA, *LPLOGFONTA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagLOGFONTA
 - wingdi/tagLOGFONTA
 - PLOGFONTA
 - wingdi/PLOGFONTA
 - LOGFONTA
 - wingdi/LOGFONTA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - LOGFONT
 - LOGFONTA
 - LOGFONTW
---

# LOGFONTA structure


## -description

The <b>LOGFONT</b> structure defines the attributes of a font.

## -struct-fields

### -field lfHeight

The height, in logical units, of the font's character cell or character. The character height value (also known as the em height) is the character cell height value minus the internal-leading value. The font mapper interprets the value specified in <b>lfHeight</b> in the following manner.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>&gt; 0</td>
<td>The font mapper transforms this value into device units and matches it against the cell height of the available fonts.</td>
</tr>
<tr>
<td>0</td>
<td>The font mapper uses a default height value when it searches for a match.</td>
</tr>
<tr>
<td>&lt; 0</td>
<td>The font mapper transforms this value into device units and matches its absolute value against the character height of the available fonts.</td>
</tr>
</table>
 

For all height comparisons, the font mapper looks for the largest font that does not exceed the requested size.

This mapping occurs when the font is used for the first time.

For the MM_TEXT mapping mode, you can use the following formula to specify a height for a font with a specified point size:


```cpp

lfHeight = -MulDiv(PointSize, GetDeviceCaps(hDC, LOGPIXELSY), 72);

```

### -field lfWidth

The average width, in logical units, of characters in the font. If <b>lfWidth</b> is zero, the aspect ratio of the device is matched against the digitization aspect ratio of the available fonts to find the closest match, determined by the absolute value of the difference.

### -field lfEscapement

The angle, in tenths of degrees, between the escapement vector and the x-axis of the device. The escapement vector is parallel to the base line of a row of text.

 When the graphics mode is set to GM_ADVANCED, you can specify the escapement angle of the string independently of the orientation angle of the string's characters.

When the graphics mode is set to GM_COMPATIBLE, <b>lfEscapement</b> specifies both the escapement and orientation. You should set <b>lfEscapement</b> and <b>lfOrientation</b> to the same value.

### -field lfOrientation

The angle, in tenths of degrees, between each character's base line and the x-axis of the device.

### -field lfWeight

The weight of the font in the range 0 through 1000. For example, 400 is normal and 700 is bold. If this value is zero, a default weight is used.

The following values are defined for convenience.

<table>
<tr>
<th>Value</th>
<th>Weight</th>
</tr>
<tr>
<td>FW_DONTCARE</td>
<td>0</td>
</tr>
<tr>
<td>FW_THIN</td>
<td>100</td>
</tr>
<tr>
<td>FW_EXTRALIGHT</td>
<td>200</td>
</tr>
<tr>
<td>FW_ULTRALIGHT</td>
<td>200</td>
</tr>
<tr>
<td>FW_LIGHT</td>
<td>300</td>
</tr>
<tr>
<td>FW_NORMAL</td>
<td>400</td>
</tr>
<tr>
<td>FW_REGULAR</td>
<td>400</td>
</tr>
<tr>
<td>FW_MEDIUM</td>
<td>500</td>
</tr>
<tr>
<td>FW_SEMIBOLD</td>
<td>600</td>
</tr>
<tr>
<td>FW_DEMIBOLD</td>
<td>600</td>
</tr>
<tr>
<td>FW_BOLD</td>
<td>700</td>
</tr>
<tr>
<td>FW_EXTRABOLD</td>
<td>800</td>
</tr>
<tr>
<td>FW_ULTRABOLD</td>
<td>800</td>
</tr>
<tr>
<td>FW_HEAVY</td>
<td>900</td>
</tr>
<tr>
<td>FW_BLACK</td>
<td>900</td>
</tr>
</table>

### -field lfItalic

An italic font if set to <b>TRUE</b>.

### -field lfUnderline

An underlined font if set to <b>TRUE</b>.

### -field lfStrikeOut

A strikeout font if set to <b>TRUE</b>.

### -field lfCharSet

The character set. The following values are predefined:

| Value | Description |
|--|--|
| **ANSI_CHARSET** | This font supports the Windows ANSI character set. |
| **ARABIC_CHARSET** | This font supports the Arabic character set. |
| **BALTIC_CHARSET** | This font supports the Baltic character set. |
| **CHINESEBIG5_CHARSET** | This font supports the traditional Chinese (Big 5) character set. |
| **DEFAULT_CHARSET** | This font supports character set value based on the system default Windows ANSI code page. For example, when the system locale is English (United States), it is set as ANSI_CHARSET. |
| **EASTEUROPE_CHARSET** | This font supports the Eastern European character set. |
| **GB2312_CHARSET** | This font supports the simplified (PRC) Chinese character set. |
| **GREEK_CHARSET** | This font supports the Greek character set. |
| **HANGEUL_CHARSET** | This font supports the Korean (Hangul) character set. |
| **HEBREW_CHARSET** | This font supports the Hebrew character set. |
| **JOHAB_CHARSET** | This font supports the Korean (Johab) character set. |
| **MAC_CHARSET** | This font supports character set value based on the current system Macintosh code page. This value is used primarily in legacy code and should not generally be needed since modern Macintosh computers use Unicode for encoding. |
| **OEM_CHARSET** | This font supports an OEM-specific character set. The OEM character set is system dependent. |
| **RUSSIAN_CHARSET** | This font supports the Cyrillic character set. |
| **SHIFTJIS_CHARSET** | This font supports the Shift-JIS (Japanese Industry Standard) character set. |
| **SYMBOL_CHARSET** | This font supports the Windows symbol character set. |
| **THAI_CHARSET** | This font supports the Thai character set. |
| **TURKISH_CHARSET** | This font supports the Turkish character set. |
| **VIETNAMESE_CHARSET** | This font supports the Vietnamese character set. |

Fonts with other character sets may exist in the operating system. If an application uses a font with an unknown character set, it should not attempt to translate or interpret strings that are rendered with that font.

This parameter is important in the font mapping process. To ensure consistent results when creating a font, do not specify **OEM_CHARSET** or **DEFAULT_CHARSET**. If you specify a typeface name in the <b>lfFaceName</b> member, make sure that the <b>lfCharSet</b> value matches the character set of the typeface specified in <b>lfFaceName</b>.

### -field lfOutPrecision

The output precision. The output precision defines how closely the output must match the requested font's height, width, character orientation, escapement, pitch, and font type. It can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>OUT_CHARACTER_PRECIS</td>
<td>Not used.</td>
</tr>
<tr>
<td>OUT_DEFAULT_PRECIS</td>
<td>Specifies the default font mapper behavior.</td>
</tr>
<tr>
<td>OUT_DEVICE_PRECIS</td>
<td>Instructs the font mapper to choose a Device font when the system contains multiple fonts with the same name.</td>
</tr>
<tr>
<td>OUT_OUTLINE_PRECIS</td>
<td> This value instructs the font mapper to choose from TrueType and other outline-based fonts.</td>
</tr>
<tr>
<td>OUT_PS_ONLY_PRECIS</td>
<td> Instructs the font mapper to choose from only PostScript fonts. If there are no PostScript fonts installed in the system, the font mapper returns to default behavior.</td>
</tr>
<tr>
<td>OUT_RASTER_PRECIS</td>
<td>Instructs the font mapper to choose a raster font when the system contains multiple fonts with the same name.</td>
</tr>
<tr>
<td>OUT_STRING_PRECIS</td>
<td>This value is not used by the font mapper, but it is returned when raster fonts are enumerated.</td>
</tr>
<tr>
<td>OUT_STROKE_PRECIS</td>
<td> This value is not used by the font mapper, but it is returned when TrueType, other outline-based fonts, and vector fonts are enumerated.</td>
</tr>
<tr>
<td>OUT_TT_ONLY_PRECIS</td>
<td>Instructs the font mapper to choose from only TrueType fonts. If there are no TrueType fonts installed in the system, the font mapper returns to default behavior.</td>
</tr>
<tr>
<td>OUT_TT_PRECIS</td>
<td>Instructs the font mapper to choose a TrueType font when the system contains multiple fonts with the same name.</td>
</tr>
</table>
 

Applications can use the OUT_DEVICE_PRECIS, OUT_RASTER_PRECIS, OUT_TT_PRECIS, and OUT_PS_ONLY_PRECIS values to control how the font mapper chooses a font when the operating system contains more than one font with a specified name. For example, if an operating system contains a font named Symbol in raster and TrueType form, specifying OUT_TT_PRECIS forces the font mapper to choose the TrueType version. Specifying OUT_TT_ONLY_PRECIS forces the font mapper to choose a TrueType font, even if it must substitute a TrueType font of another name.

### -field lfClipPrecision

The clipping precision. The clipping precision defines how to clip characters that are partially outside the clipping region. It can be one or more of the following values.

For more information about the orientation of coordinate systems, see the description of the <i>nOrientation</i> parameter.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>CLIP_CHARACTER_PRECIS</td>
<td>Not used.</td>
</tr>
<tr>
<td>CLIP_DEFAULT_PRECIS</td>
<td>Specifies default clipping behavior.</td>
</tr>
<tr>
<td>CLIP_DFA_DISABLE</td>
<td><b>Windows XP SP1:</b> Turns off font association for the font. Note that this flag is not guaranteed to have any effect on any platform after Windows Server 2003.</td>
</tr>
<tr>
<td>CLIP_EMBEDDED</td>
<td>You must specify this flag to use an embedded read-only font.</td>
</tr>
<tr>
<td>CLIP_LH_ANGLES</td>
<td>When this value is used, the rotation for all fonts depends on whether the orientation of the coordinate system is left-handed or right-handed.If not used, device fonts always rotate counterclockwise, but the rotation of other fonts is dependent on the orientation of the coordinate system.

</td>
</tr>
<tr>
<td>CLIP_MASK</td>
<td>Not used.</td>
</tr>
<tr>
<td>CLIP_DFA_OVERRIDE</td>
<td> Turns off font association for the font. This is identical to CLIP_DFA_DISABLE, but it can have problems in some situations; the recommended flag to use is CLIP_DFA_DISABLE.</td>
</tr>
<tr>
<td>CLIP_STROKE_PRECIS</td>
<td>Not used by the font mapper, but is returned when raster, vector, or TrueType fonts are enumerated. For compatibility, this value is always returned when enumerating fonts.

</td>
</tr>
<tr>
<td>CLIP_TT_ALWAYS</td>
<td>Not used.</td>
</tr>
</table>

### -field lfQuality

The output quality. The output quality defines how carefully the graphics device interface (GDI) must attempt to match the logical-font attributes to those of an actual physical font. It can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>ANTIALIASED_QUALITY</td>
<td> Font is always antialiased if the font supports it and the size of the font is not too small or too large.</td>
</tr>
<tr>
<td>CLEARTYPE_QUALITY</td>
<td> If set, text is rendered (when possible) using ClearType antialiasing method. See Remarks for more information.</td>
</tr>
<tr>
<td>DEFAULT_QUALITY</td>
<td>Appearance of the font does not matter.</td>
</tr>
<tr>
<td>DRAFT_QUALITY</td>
<td>Appearance of the font is less important than when PROOF_QUALITY is used. For GDI raster fonts, scaling is enabled, which means that more font sizes are available, but the quality may be lower. Bold, italic, underline, and strikeout fonts are synthesized if necessary.</td>
</tr>
<tr>
<td>NONANTIALIASED_QUALITY</td>
<td> Font is never antialiased.</td>
</tr>
<tr>
<td>PROOF_QUALITY</td>
<td>Character quality of the font is more important than exact matching of the logical-font attributes. For GDI raster fonts, scaling is disabled and the font closest in size is chosen. Although the chosen font size may not be mapped exactly when PROOF_QUALITY is used, the quality of the font is high and there is no distortion of appearance. Bold, italic, underline, and strikeout fonts are synthesized if necessary.</td>
</tr>
</table>
 

If neither ANTIALIASED_QUALITY nor NONANTIALIASED_QUALITY is selected, the font is antialiased only if the user chooses smooth screen fonts in Control Panel.

### -field lfPitchAndFamily

The pitch and family of the font. The two low-order bits specify the pitch of the font and can be one of the following values.

<ul>
<li>DEFAULT_PITCH</li>
<li>FIXED_PITCH</li>
<li>VARIABLE_PITCH</li>
</ul>
Bits 4 through 7 of the member specify the font family and can be one of the following values.

<ul>
<li>FF_DECORATIVE</li>
<li>FF_DONTCARE</li>
<li>FF_MODERN</li>
<li>FF_ROMAN</li>
<li>FF_SCRIPT</li>
<li>FF_SWISS</li>
</ul>
The proper value can be obtained by using the Boolean OR operator to join one pitch constant with one family constant.

Font families describe the look of a font in a general way. They are intended for specifying fonts when the exact typeface desired is not available. The values for font families are as follows.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>FF_DECORATIVE</td>
<td>Novelty fonts. Old English is an example.</td>
</tr>
<tr>
<td>FF_DONTCARE</td>
<td>Use default font.</td>
</tr>
<tr>
<td>FF_MODERN</td>
<td>Fonts with constant stroke width (monospace), with or without serifs. Monospace fonts are usually modern. Pica, Elite, and CourierNew are examples.</td>
</tr>
<tr>
<td>FF_ROMAN</td>
<td>Fonts with variable stroke width (proportional) and with serifs. MS Serif is an example.</td>
</tr>
<tr>
<td>FF_SCRIPT</td>
<td>Fonts designed to look like handwriting. Script and Cursive are examples.</td>
</tr>
<tr>
<td>FF_SWISS</td>
<td>Fonts with variable stroke width (proportional) and without serifs. MS Sans Serif is an example.</td>
</tr>
</table>

### -field lfFaceName

A null-terminated string that specifies the typeface name of the font. The length of this string must not exceed 32 <b>TCHAR</b> values, including the terminating <b>NULL</b>. The <a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesexa">EnumFontFamiliesEx</a> function can be used to enumerate the typeface names of all currently available fonts. If <b>lfFaceName</b> is an empty string, GDI uses the first font that matches the other specified attributes.

## -remarks

The following situations do not support ClearType antialiasing:

<ul>
<li>Text is rendered on a printer.</li>
<li>Display set for 256 colors or less.</li>
<li>Text is rendered to a terminal server client.</li>
<li>The font is not a TrueType font or an OpenType font with TrueType outlines. For example, the following do not support ClearType antialiasing: Type 1 fonts, Postscript OpenType fonts without TrueType outlines, bitmap fonts, vector fonts, and device fonts.</li>
<li>The font has tuned embedded bitmaps, for any font sizes that contain the embedded bitmaps. For example, this occurs commonly in East Asian fonts.</li>
</ul>




> [!NOTE]
> The wingdi.h header defines LOGFONT as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-createfonta">CreateFont</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createfontindirecta">CreateFontIndirect</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesexa">EnumFontFamiliesEx</a>



<a href="/windows/desktop/gdi/font-and-text-structures">Font and Text Structures</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>
