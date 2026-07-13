---
UID: NF:wingdi.CreateFontIndirectExW
title: CreateFontIndirectExW function (wingdi.h)
description: The CreateFontIndirectEx function specifies a logical font that has the characteristics in the specified structure. The font can subsequently be selected as the current font for any device context. (Unicode)
helpviewer_keywords: ["CreateFontIndirectEx", "CreateFontIndirectEx function [Windows GDI]", "CreateFontIndirectExW", "_win32_CreateFontIndirectEx", "gdi.createfontindirectex", "wingdi/CreateFontIndirectEx", "wingdi/CreateFontIndirectExW"]
old-location: gdi\createfontindirectex.htm
tech.root: gdi
ms.assetid: 1161b79e-f9c8-4073-97c4-1ccc1a78279b
ms.date: 12/05/2018
ms.keywords: CreateFontIndirectEx, CreateFontIndirectEx function [Windows GDI], CreateFontIndirectExA, CreateFontIndirectExW, _win32_CreateFontIndirectEx, gdi.createfontindirectex, wingdi/CreateFontIndirectEx, wingdi/CreateFontIndirectExA, wingdi/CreateFontIndirectExW
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateFontIndirectExW (Unicode) and CreateFontIndirectExA (ANSI)
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
 - CreateFontIndirectExW
 - wingdi/CreateFontIndirectExW
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
 - CreateFontIndirectEx
 - CreateFontIndirectExA
 - CreateFontIndirectExW
---

# CreateFontIndirectExW function


## -description

The <b>CreateFontIndirectEx</b> function specifies a logical font that has the characteristics in the specified structure. The font can subsequently be selected as the current font for any device context.

## -parameters

### -param unnamedParam1 [in]

Pointer to an <a href="/windows/desktop/api/wingdi/ns-wingdi-enumlogfontexdva">ENUMLOGFONTEXDV</a> structure that defines the characteristics of a multiple master font.

Note, this function ignores the <b>elfDesignVector</b> member in <a href="/windows/desktop/api/wingdi/ns-wingdi-enumlogfontexdva">ENUMLOGFONTEXDV</a>.

## -returns

If the function succeeds, the return value is the handle to the new <a href="/windows/desktop/api/wingdi/ns-wingdi-enumlogfontexdva">ENUMLOGFONTEXDV</a> structure.

If the function fails, the return value is zero. No extended error information is available.

## -remarks

The <b>CreateFontIndirectEx</b> function creates a logical font with the characteristics specified in the <a href="/windows/desktop/api/wingdi/ns-wingdi-enumlogfontexdva">ENUMLOGFONTEXDV</a> structure. When this font is selected by using the <a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a> function, GDI's font mapper attempts to match the logical font with an existing physical font. If it fails to find an exact match, it provides an alternative whose characteristics match as many of the requested characteristics as possible.

When you no longer need the font, call the <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> function to delete it.

The font mapper for <a href="/windows/desktop/api/wingdi/nf-wingdi-createfonta">CreateFont</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-createfontindirecta">CreateFontIndirect</a>, and <b>CreateFontIndirectEx</b> recognizes both the English and the localized typeface name, regardless of locale.





> [!NOTE]
> The wingdi.h header defines CreateFontIndirectEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-createfonta">CreateFont
      </a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createfontindirecta">CreateFontIndirect
      </a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-enumlogfontexdva">ENUMLOGFONTEXDV
      </a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesa">EnumFontFamilies
      </a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesexa">EnumFontFamiliesEx
      </a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontsa">EnumFonts
      </a>



<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>
