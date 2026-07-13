---
UID: NF:wingdi.EnumFontFamiliesExW
title: EnumFontFamiliesExW function (wingdi.h)
description: The EnumFontFamiliesEx function enumerates all uniquely-named fonts in the system that match the font characteristics specified by the LOGFONT structure. EnumFontFamiliesEx enumerates fonts based on typeface name, character set, or both. (Unicode)
helpviewer_keywords: ["EnumFontFamiliesEx", "EnumFontFamiliesEx function [Windows GDI]", "EnumFontFamiliesExW", "_win32_EnumFontFamiliesEx", "gdi.enumfontfamiliesex", "wingdi/EnumFontFamiliesEx", "wingdi/EnumFontFamiliesExW"]
old-location: gdi\enumfontfamiliesex.htm
tech.root: gdi
ms.assetid: 4d70906d-8005-4c4a-869e-16dd3e6fa3f2
ms.date: 12/05/2018
ms.keywords: EnumFontFamiliesEx, EnumFontFamiliesEx function [Windows GDI], EnumFontFamiliesExA, EnumFontFamiliesExW, _win32_EnumFontFamiliesEx, gdi.enumfontfamiliesex, wingdi/EnumFontFamiliesEx, wingdi/EnumFontFamiliesExA, wingdi/EnumFontFamiliesExW
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumFontFamiliesExW (Unicode) and EnumFontFamiliesExA (ANSI)
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
 - EnumFontFamiliesExW
 - wingdi/EnumFontFamiliesExW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Font-l1-1-0.dll
 - Ext-MS-Win-GDI-Font-l1-1-1.dll
 - ext-ms-win-gdi-font-l1-1-2.dll
 - Ext-MS-Win-GDI-Font-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - EnumFontFamiliesEx
 - EnumFontFamiliesExA
 - EnumFontFamiliesExW
---

# EnumFontFamiliesExW function


## -description

The <b>EnumFontFamiliesEx</b> function enumerates all uniquely-named fonts in the system that match the font characteristics specified by the <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure. <b>EnumFontFamiliesEx</b> enumerates fonts based on typeface name, character set, or both.

## -parameters

### -param hdc [in]

A handle to the device context from which to enumerate the fonts.

### -param lpLogfont [in]

A pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure that contains information about the fonts to enumerate. The function examines the following members.

<table>
<tr>
<th>Member</th>
<th>Description</th>
</tr>
<tr>
<td><b>lfCharSet</b></td>
<td>If set to DEFAULT_CHARSET, the function enumerates all uniquely-named fonts in all character sets. (If there are two fonts with the same name, only one is enumerated.) If set to a valid character set value, the function enumerates only fonts in the specified character set.</td>
</tr>
<tr>
<td><b>lfFaceName</b></td>
<td>If set to an empty string, the function enumerates one font in each available typeface name. If set to a valid typeface name, the function enumerates all fonts with the specified name.</td>
</tr>
<tr>
<td><b>lfPitchAndFamily</b></td>
<td>Must be set to zero for all language versions of the operating system.</td>
</tr>
</table>

### -param lpProc [in]

A pointer to the application defined callback function. For more information, see the <a href="/previous-versions/dd162618(v=vs.85)">EnumFontFamExProc</a> function.

### -param lParam [in]

An application defined value. The function passes this value to the callback function along with font information.

### -param dwFlags

This parameter is not used and must be zero.

## -returns

The return value is the last value returned by the callback function. This value depends on which font families are available for the specified device.

## -remarks

The <b>EnumFontFamiliesEx</b> function does not use tagged typeface names to identify character sets. Instead, it always passes the correct typeface name and a separate character set value to the callback function. The function enumerates fonts based on the values of the <b>lfCharSet</b> and <b>lfFaceName</b> members in the <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure.

As with <a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesa">EnumFontFamilies</a>, <b>EnumFontFamiliesEx</b> enumerates all font styles. Not all styles of a font cover the same character sets. For example, Fontorama Bold might contain ANSI, Greek, and Cyrillic characters, but Fontorama Italic might contain only ANSI characters. For this reason, it's best not to assume that a specified font covers a specific character set, even if it is the ANSI character set. The following table shows the results of various combinations of values for <b>lfCharSet</b> and <b>lfFaceName</b>.

<table>
<tr>
<th>Values</th>
<th>Meaning</th>
</tr>
<tr>
<td>
<b>lfCharSet</b> = DEFAULT_CHARSET

<b>lfFaceName</b> = '\0'

</td>
<td>
Enumerates all uniquely-named fonts within all character sets. If there are two fonts with the same name, only one is enumerated.

</td>
</tr>
<tr>
<td>
<b>lfCharSet</b> = DEFAULT_CHARSET

<b>lfFaceName</b> = a specific font

</td>
<td>
Enumerates all character sets and styles in a specific font.

</td>
</tr>
<tr>
<td>
<b>lfCharSet</b> =a specific character set

<b>lfFaceName</b> = '\0'

</td>
<td>
Enumerates all styles of all fonts in the specific character set.

</td>
</tr>
<tr>
<td>
<b>lfCharSet</b> =a specific character set

<b>lfFaceName</b> = a specific font

</td>
<td>
Enumerates all styles of a font in a specific character set.

</td>
</tr>
</table>
 

The following code sample shows how these values are used.


```cpp

// To enumerate all styles and charsets of all fonts: 
lf.lfFaceName[0] = '\0';
lf.lfCharSet = DEFAULT_CHARSET;
HRESULT hr;

// To enumerate all styles and character sets of the Arial font: 
hr = StringCchCopy( (LPSTR)lf.lfFaceName, LF_FACESIZE, "Arial" );
if (FAILED(hr))
{
// TODO: write error handler 
}

lf.lfCharSet = DEFAULT_CHARSET;

```



```cpp

// To enumerate all styles of all fonts for the ANSI character set 
lf.lfFaceName[0] = '\0';
lf.lfCharSet = ANSI_CHARSET;

// To enumerate all styles of Arial font that cover the ANSI charset 
hr = StringCchCopy( (LPSTR)lf.lfFaceName, LF_FACESIZE, "Arial" );
if (FAILED(hr))
{
// TODO: write error handler 
}

lf.lfCharSet = ANSI_CHARSET;

```


The callback functions for <a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesa">EnumFontFamilies</a> and <b>EnumFontFamiliesEx</b> are very similar. The main difference is that the <a href="/windows/desktop/api/wingdi/ns-wingdi-enumlogfontexa">ENUMLOGFONTEX</a> structure includes a script field.

Note, based on the values of <b>lfCharSet</b> and <b>lfFaceName</b>, <b>EnumFontFamiliesEx</b> will enumerate the same font as many times as there are distinct character sets in the font. This can create an extensive list of fonts which can be burdensome to a user. For example, the Century Schoolbook font can appear for the Baltic, Western, Greek, Turkish, and Cyrillic character sets. To avoid this, an application should filter the list of fonts.

The fonts for many East Asian languages have two typeface names: an English name and a localized name. <a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontsa">EnumFonts</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesa">EnumFontFamilies</a>, and <b>EnumFontFamiliesEx</b> return the English typeface name if the system locale does not match the language of the font.

When the graphics mode on the device context is set to GM_ADVANCED using the SetGraphicsMode function and the DEVICE_FONTTYPE flag is passed to the FontType parameter, this function returns a list of type 1 and OpenType fonts on the system. When the graphics mode is not set to GM_ADVANCED, this function returns a list of type 1, OpenType, and TrueType fonts on the system.





> [!NOTE]
> The wingdi.h header defines EnumFontFamiliesEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/dd162618(v=vs.85)">EnumFontFamExProc</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesa">EnumFontFamilies</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontsa">EnumFonts</a>



<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a>
