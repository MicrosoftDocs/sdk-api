---
UID: NF:wingdi.GetCharWidthI
title: GetCharWidthI function (wingdi.h)
description: The GetCharWidthI function retrieves the widths, in logical coordinates, of consecutive glyph indices in a specified range from the current font.
helpviewer_keywords: ["GetCharWidthI","GetCharWidthI function [Windows GDI]","_win32_GetCharWidthI","gdi.getcharwidthi","wingdi/GetCharWidthI"]
old-location: gdi\getcharwidthi.htm
tech.root: gdi
ms.assetid: 5f532149-7c2f-4972-9900-68c2f185d255
ms.date: 12/05/2018
ms.keywords: GetCharWidthI, GetCharWidthI function [Windows GDI], _win32_GetCharWidthI, gdi.getcharwidthi, wingdi/GetCharWidthI
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
 - GetCharWidthI
 - wingdi/GetCharWidthI
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
 - GetCharWidthI
---

# GetCharWidthI function


## -description

The <b>GetCharWidthI</b> function retrieves the widths, in logical coordinates, of consecutive glyph indices in a specified range from the current font.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param giFirst [in]

The first glyph index in the group of consecutive glyph indices.

### -param cgi [in]

The number of glyph indices.

### -param pgi [in]

A pointer to an array of glyph indices. If this parameter is not <b>NULL</b>, it is used instead of the <i>giFirst</i> parameter.

### -param piWidths [out]

A pointer to a buffer that receives the widths, in logical coordinates.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The <b>GetCharWidthI</b> function processes a consecutive glyph indices if the <i>pgi</i> parameter is <b>NULL</b> with the <i>giFirst</i> parameter indicating the first glyph index to process and the <i>cgi</i> parameter indicating how many glyph indices to process. Otherwise the <b>GetCharWidthI</b> function processes the array of glyph indices pointed to by the <i>pgi</i> parameter with the <i>cgi</i> parameter indicating how many glyph indices to process.

If a character does not exist in the current font, it is assigned the width of the default character.

## -see-also

<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getcharabcwidthsa">GetCharABCWidths</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getcharabcwidthsfloata">GetCharABCWidthsFloat</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getcharwidth32a">GetCharWidth32</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getcharwidthfloata">GetCharWidthFloat</a>