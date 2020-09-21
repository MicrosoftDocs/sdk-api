---
UID: NF:wingdi.GetFontUnicodeRanges
title: GetFontUnicodeRanges function (wingdi.h)
description: The GetFontUnicodeRanges function returns information about which Unicode characters are supported by a font. The information is returned as a GLYPHSET structure.
helpviewer_keywords: ["GetFontUnicodeRanges","GetFontUnicodeRanges function [Windows GDI]","_win32_GetFontUnicodeRanges","gdi.getfontunicoderanges","wingdi/GetFontUnicodeRanges"]
old-location: gdi\getfontunicoderanges.htm
tech.root: gdi
ms.assetid: 51b0ab12-c467-4a89-8173-fdc513868aae
ms.date: 12/05/2018
ms.keywords: GetFontUnicodeRanges, GetFontUnicodeRanges function [Windows GDI], _win32_GetFontUnicodeRanges, gdi.getfontunicoderanges, wingdi/GetFontUnicodeRanges
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
 - GetFontUnicodeRanges
 - wingdi/GetFontUnicodeRanges
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Font-L1-1-2.dll
 - Ext-MS-Win-GDI-Font-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - GetFontUnicodeRanges
---

# GetFontUnicodeRanges function


## -description

The <b>GetFontUnicodeRanges</b> function returns information about which Unicode characters are supported by a font. The information is returned as a <a href="/windows/desktop/api/wingdi/ns-wingdi-glyphset">GLYPHSET</a> structure.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param lpgs [out]

A pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-glyphset">GLYPHSET</a> structure that receives the glyph set information. If this parameter is <b>NULL</b>, the function returns the size of the <b>GLYPHSET</b> structure required to store the information.

## -returns

If the function succeeds, it returns number of bytes written to the GLYPHSET structure or, if the <i>lpgs</i> parameter is <b>NULL</b>, it returns the size of the GLYPHSET structure required to store the information.

If the function fails, it returns zero. No extended error information is available.

## -see-also

<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-glyphset">GLYPHSET</a>