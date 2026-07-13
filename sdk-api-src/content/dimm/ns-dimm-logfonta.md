---
UID: NS:dimm.__MIDL___MIDL_itf_dimm_0000_0000_0003
title: LOGFONTA (dimm.h)
description: The LOGFONTA (ANSI) structure defines the attributes of a font's character cell or character. (LOGFONTA)
helpviewer_keywords: ["LOGFONT","LOGFONT structure [Windows Shell]","LOGFONTA","LOGFONTW","_shell_LOGFONT","_shell_LOGFONT_cpp","dimm/LOGFONT","dimm/LOGFONTA","dimm/LOGFONTW","shell.LOGFONT"]
old-location: shell\LOGFONT.htm
tech.root: shell
ms.assetid: 759c54d9-5b8f-4b48-8380-79e7bcae5bdb
ms.date: 08/02/2022
ms.keywords: LOGFONT, LOGFONT structure [Windows Shell], LOGFONTA, LOGFONTW, _shell_LOGFONT, _shell_LOGFONT_cpp, dimm/LOGFONT, dimm/LOGFONTA, dimm/LOGFONTW, shell.LOGFONT
req.header: dimm.h
req.include-header: Shtypes.h, Dimm.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LOGFONTW (Unicode) and LOGFONTA (ANSI)
req.idl: Shtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: LOGFONTA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_dimm_0000_0000_0003
 - dimm/__MIDL___MIDL_itf_dimm_0000_0000_0003
 - LOGFONTA
 - dimm/LOGFONTA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dimm.h
api_name:
 - LOGFONT
 - LOGFONTA
 - LOGFONTW
---

# LOGFONTA structure


## -description

Defines the attributes of a font.

## -struct-fields

### -field lfHeight

Type: <b>LONG</b>

Specifies the height, in logical units, of the font's character cell or character. The character height value (also known as the em height) is the character cell height value minus the internal-leading value. The font mapper interprets the value specified in <b>lfHeight</b> in the following manner.

<table class="clsStd">
<tr>
<th>Value</th>
<th>Description</th>
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

For the MM_TEXT mapping mode, you may use the following formula to specify a height for a font with a given point size.


```cpp
lfHeight = -MulDiv(PointSize, GetDeviceCaps(hDC, LOGPIXELSY), 72);

```


where <b>MulDiv</b> is defined as follows:


```cpp
#define MulDiv(a,b,c)    (((a)*(b))/(c))

```

### -field lfWidth

Type: <b>LONG</b>

Specifies the average width, in logical units, of characters in the font. If <b>lfWidth</b> is not zero, the aspect ratio of the device is matched against the digitization aspect ratio of the available fonts to find the closest match, determined by the absolute value of the difference.

### -field lfEscapement

Type: <b>LONG</b>

Specifies the angle, in tenths of degrees, between the escapement vector and the x-axis of the device. The escapement vector is parallel to the base line of a row of text.

The <b>lfEscapement</b> member specifies both the escapement and orientation. You should set <b>lfEscapement</b> and <b>lfOrientation</b> to the same value.

### -field lfOrientation

Type: <b>LONG</b>

Specifies the angle, in tenths of degrees, between each character's base line and the x-axis of the device.

### -field lfWeight

Type: <b>LONG</b>

Specifies the weight of the font in the range 0 through 1000. For example, 400 is normal and 700 is bold. If this value is zero, a default weight is used.

The following values are defined in Wingdi.h for convenience.

<table class="clsStd">
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

Type: <b>BYTE</b>

<b>TRUE</b> to specify an italic font.

### -field lfUnderline

Type: <b>BYTE</b>

<b>TRUE</b> to specify an underlined font.

### -field lfStrikeOut

Type: <b>BYTE</b>

<b>TRUE</b> to specify a strikeout font.

### -field lfCharSet

Type: <b>BYTE</b>

Specifies the character set. The following values are predefined:

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

This member is important in the font mapping process. To ensure consistent results, specify a specific character set. If you specify a typeface name in the <b>lfFaceName</b> member, make sure that the <b>lfCharSet</b> value matches the character set of the typeface specified in <b>lfFaceName</b>.

### -field lfOutPrecision

Type: <b>BYTE</b>

Specifies the output precision. The output precision defines how closely the output must match the requested font's height, width, character orientation, escapement, pitch, and font type. It can be one of the following values defined in Wingdi.h:

<table class="clsStd">
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>OUT_DEFAULT_PRECIS</td>
<td>Specifies the default font mapper behavior.</td>
</tr>
<tr>
<td>OUT_RASTER_PRECIS</td>
<td>Instructs the font mapper to choose a raster font when the system contains multiple fonts with the same name.</td>
</tr>
<tr>
<td>OUT_STRING_PRECIS</td>
<td>This value is not used by the font mapper, but it is returned when raster fonts are enumerated.</td>
</tr>
</table>

### -field lfClipPrecision

Type: <b>BYTE</b>

Specifies the clipping precision. The clipping precision defines how to clip characters that are partially outside the clipping region. It can be one or more of the following values defined in Wingdi.h:

<table class="clsStd">
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>CLIP_DEFAULT_PRECIS</td>
<td>Specifies default clipping behavior.</td>
</tr>
<tr>
<td>CLIP_CHARACTER_PRECIS</td>
<td>Not used.</td>
</tr>
<tr>
<td>CLIP_STROKE_PRECIS</td>
<td>Not used by the font mapper, but is returned when raster, vector, or TrueType fonts are enumerated.</td>
</tr>
</table>

### -field lfQuality

Type: <b>BYTE</b>

Specifies the output quality. The output quality defines how carefully the GDI must attempt to match the logical-font attributes to those of an actual physical font. It can be one of the following values defined in Wingdi.h:

<table class="clsStd">
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>ANTIALIASED_QUALITY</td>
<td>Enables antialiasing for the font. The display driver must support antialiased text for this setting to work.</td>
</tr>
<tr>
<td>NONANTIALIASED_QUALITY</td>
<td>Forces use of draft quality when the 
                                <b>HKEY_LOCAL_MACHINE</b>&#92;<b>System</b>&#92;<b>GDI</b>&#92;<b>Fontsmoothing</b> registry subkey is present.</td>
</tr>
<tr>
<td>CLEARTYPE_COMPAT_QUALITY</td>
<td>Enables ClearType text for the font using compatible widths. A compatible width produces text that has the same spacing as non-ClearType text.</td>
</tr>
<tr>
<td>CLEARTYPE_QUALITY</td>
<td>Enables ClearType text for the font. The display driver must support ClearType text for this setting to work.</td>
</tr>
<tr>
<td>DEFAULT_QUALITY</td>
<td>Appearance of the font does not matter.</td>
</tr>
<tr>
<td>DRAFT_QUALITY</td>
<td>For GDI raster fonts, scaling is enabled, which means that more font sizes are available, but the quality may be lower. Bold, italic, underline, and strikeout fonts are synthesized if necessary.</td>
</tr>
</table>

### -field lfPitchAndFamily

Type: <b>BYTE</b>

Specifies the pitch and group of the font. The two low-order bits specify the pitch of the font and can be one of the following values defined in Wingdi.h: 

                    

<ul>
<li>DEFAULT_PITCH</li>
<li>FIXED_PITCH</li>
<li>MONO_FONT</li>
<li>VARIABLE_PITCH</li>
</ul>
Bits 4 through 7 of the member specify the font group and can be one of the following values defined in Wingdi.h:

<ul>
<li>FF_DECORATIVE</li>
<li>FF_DONTCARE</li>
<li>FF_MODERN</li>
<li>FF_ROMAN</li>
<li>FF_SCRIPT</li>
<li>FF_SWISS</li>
</ul>
The proper value can be obtained by using the Boolean OR operator to join one pitch constant with one family constant.

Font families describe the look of a font in a general way. They are intended for specifying fonts when the exact typeface desired is not available. The values for font families are as follows:

<table class="clsStd">
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>FF_DECORATIVE</td>
<td>Novelty fonts, for example, Old English.</td>
</tr>
<tr>
<td>FF_DONTCARE</td>
<td>Do not care or do not know.</td>
</tr>
<tr>
<td>FF_MODERN</td>
<td>Fonts with constant stroke width (monospace), with or without serifs. Monospace fonts are usually modern, for example, Pica, Elite, and Courier New.</td>
</tr>
<tr>
<td>FF_ROMAN</td>
<td>Fonts with variable stroke width (proportional) and with serifs, for example, Serif.</td>
</tr>
<tr>
<td>FF_SCRIPT</td>
<td>Fonts designed to look like handwriting, for example, Script and Cursive.</td>
</tr>
<tr>
<td>FF_SWISS</td>
<td>Fonts with variable stroke width (proportional) and without serifs, for example, Sans Serif.</td>
</tr>
</table>

### -field lfFaceName

Type: <b>TCHAR[LF_FACESIZE]</b>

Specifies a null-terminated string that specifies the typeface name of the font. The length of this string must not exceed 32 characters, including the terminating null character. The <a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesa">EnumFontFamilies</a> function can be used to enumerate the typeface names of all currently available fonts. If <b>lfFaceName</b> is an empty string, GDI uses the first font that matches the other specified attributes.

## -remarks

The following situations do not support ClearType antialiasing:

<ul>
<li>Text is rendered on a printer.</li>
<li>Display set for 256 colors or less.</li>
<li>Text is rendered to a terminal server client.</li>
<li>The font is not a TrueType font or an Microsoft OpenType font with TrueType outlines. For example, the following do not support ClearType antialiasing: Type 1 fonts, Postscript OpenType fonts without TrueType outlines, bitmap fonts, vector fonts, and device fonts.</li>
<li>The font has tuned embedded bitmaps, for any font sizes that contain the embedded bitmaps. For example, this occurs commonly in East Asian fonts.</li>
</ul>
This structure first appeared in Shtypes.idl and Shtypes.h in Windows Vista, for ease of use with members of the <a href="/windows/desktop/api/shobjidl/nn-shobjidl-ivisualproperties">IVisualProperties</a> interface. However, the identical structure is defined in Wingdi.h and Windows.h in earlier versions of Windows.

## -see-also

<a href="/windows/desktop/api/shobjidl/nf-shobjidl-ivisualproperties-getfont">IVisualProperties::GetFont</a>



<a href="/windows/desktop/api/shobjidl/nf-shobjidl-ivisualproperties-setfont">IVisualProperties::SetFont</a>
