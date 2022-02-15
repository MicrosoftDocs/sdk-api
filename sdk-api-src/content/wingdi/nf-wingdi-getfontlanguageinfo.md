---
UID: NF:wingdi.GetFontLanguageInfo
title: GetFontLanguageInfo function (wingdi.h)
description: The GetFontLanguageInfo function returns information about the currently selected font for the specified display context. Applications typically use this information and the GetCharacterPlacement function to prepare a character string for display.
helpviewer_keywords: ["GetFontLanguageInfo","GetFontLanguageInfo function [Windows GDI]","_win32_GetFontLanguageInfo","gdi.getfontlanguageinfo","wingdi/GetFontLanguageInfo"]
old-location: gdi\getfontlanguageinfo.htm
tech.root: gdi
ms.assetid: c2f19423-4410-44dd-83f1-5b858852051d
ms.date: 12/05/2018
ms.keywords: GetFontLanguageInfo, GetFontLanguageInfo function [Windows GDI], _win32_GetFontLanguageInfo, gdi.getfontlanguageinfo, wingdi/GetFontLanguageInfo
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - GetFontLanguageInfo
 - wingdi/GetFontLanguageInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - GetFontLanguageInfo
---

# GetFontLanguageInfo function


## -description

The <b>GetFontLanguageInfo</b> function returns information about the currently selected font for the specified display context. Applications typically use this information and the <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a> function to prepare a character string for display.

## -parameters

### -param hdc [in]

Handle to a display device context.

## -returns

The return value identifies characteristics of the currently selected font. The function returns 0 if the font is "normalized" and can be treated as a simple Latin font; it returns GCP_ERROR if an error occurs. Otherwise, the function returns a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>GCP_DBCS</td>
<td>The character set is DBCS.</td>
</tr>
<tr>
<td>GCP_DIACRITIC</td>
<td>The font/language contains diacritic glyphs.</td>
</tr>
<tr>
<td>FLI_GLYPHS</td>
<td>The font contains extra glyphs not normally accessible using the code page. Use <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a> to access the glyphs. This value is for information only and is not intended to be passed to <b>GetCharacterPlacement</b>.</td>
</tr>
<tr>
<td>GCP_GLYPHSHAPE</td>
<td>The font/language contains multiple glyphs per code point or per code point combination (supports shaping and/or ligation), and the font contains advanced glyph tables to provide extra glyphs for the extra shapes. If this value is specified, the <b>lpGlyphs</b> array must be used with the <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a> function and the ETO_GLYPHINDEX value must be passed to the <a href="/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOut</a> function when the string is drawn.</td>
</tr>
<tr>
<td>GCP_KASHIDA</td>
<td>The font/ language permits Kashidas.</td>
</tr>
<tr>
<td>GCP_LIGATE</td>
<td>The font/language contains ligation glyphs which can be substituted for specific character combinations.</td>
</tr>
<tr>
<td>GCP_USEKERNING</td>
<td>The font contains a kerning table which can be used to provide better spacing between the characters and glyphs.</td>
</tr>
<tr>
<td>GCP_REORDER</td>
<td>The language requires reordering for display for example, Hebrew or Arabic.</td>
</tr>
</table>
 

The return value, when masked with FLI_MASK, can be passed directly to the <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a> function.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOut</a>



<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a>