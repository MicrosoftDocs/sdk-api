---
UID: NF:wingdi.CreateFontIndirectW
title: CreateFontIndirectW function (wingdi.h)
description: The CreateFontIndirect function creates a logical font that has the specified characteristics. The font can subsequently be selected as the current font for any device context. (Unicode)
helpviewer_keywords: ["CreateFontIndirect", "CreateFontIndirect function [Windows GDI]", "CreateFontIndirectW", "_win32_CreateFontIndirect", "gdi.createfontindirect", "wingdi/CreateFontIndirect", "wingdi/CreateFontIndirectW"]
old-location: gdi\createfontindirect.htm
tech.root: gdi
ms.assetid: b7919fb6-8515-4f1b-af9c-dc7eac381b90
ms.date: 12/05/2018
ms.keywords: CreateFontIndirect, CreateFontIndirect function [Windows GDI], CreateFontIndirectA, CreateFontIndirectW, _win32_CreateFontIndirect, gdi.createfontindirect, wingdi/CreateFontIndirect, wingdi/CreateFontIndirectA, wingdi/CreateFontIndirectW
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateFontIndirectW (Unicode) and CreateFontIndirectA (ANSI)
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
 - CreateFontIndirectW
 - wingdi/CreateFontIndirectW
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
 - CreateFontIndirect
 - CreateFontIndirectA
 - CreateFontIndirectW
---

# CreateFontIndirectW function


## -description

The <b>CreateFontIndirect</b> function creates a logical font that has the specified characteristics. The font can subsequently be selected as the current font for any device context.

## -parameters

### -param lplf [in]

A pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure that defines the characteristics of the logical font.

## -returns

If the function succeeds, the return value is a handle to a logical font.

If the function fails, the return value is <b>NULL</b>.

## -remarks

The <b>CreateFontIndirect</b> function creates a logical font with the characteristics specified in the <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure. When this font is selected by using the <a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a> function, GDI's font mapper attempts to match the logical font with an existing physical font. If it fails to find an exact match, it provides an alternative whose characteristics match as many of the requested characteristics as possible.

To get the appropriate font on different language versions of the OS, call <a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesexa">EnumFontFamiliesEx</a> with the desired font characteristics in the <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure, retrieve the appropriate typeface name, and create the font using <a href="/windows/desktop/api/wingdi/nf-wingdi-createfonta">CreateFont</a> or <b>CreateFontIndirect</b>.

When you no longer need the font, call the <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> function to delete it.

The fonts for many East Asian languages have two typeface names: an English name and a localized name. <a href="/windows/desktop/api/wingdi/nf-wingdi-createfonta">CreateFont</a> and <b>CreateFontIndirect</b> take the localized typeface name only on a system locale that matches the language, while they take the English typeface name on all other system locales. The best method is to try one name and, on failure, try the other. Note that <a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontsa">EnumFonts</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesa">EnumFontFamilies</a>, and <a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesexa">EnumFontFamiliesEx</a> return the English typeface name if the system locale does not match the language of the font.

The font mapper for <a href="/windows/desktop/api/wingdi/nf-wingdi-createfonta">CreateFont</a>, <b>CreateFontIndirect</b>, and <a href="/windows/desktop/api/wingdi/nf-wingdi-createfontindirectexa">CreateFontIndirectEx</a> recognizes both the English and the localized typeface name, regardless of locale.


#### Examples

For an example, see <a href="/windows/desktop/gdi/creating-a-logical-font">Creating a Logical Font</a>.

<div class="code"></div>




> [!NOTE]
> The wingdi.h header defines CreateFontIndirect as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-createfonta">CreateFont
      </a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createfontindirectexa">CreateFontIndirectEx
      </a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject
      </a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesa">EnumFontFamilies
      </a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesexa">EnumFontFamiliesEx
      </a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontsa">EnumFonts
      </a>



<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT
      </a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject
      </a>
