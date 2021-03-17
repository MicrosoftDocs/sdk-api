---
UID: NF:wingdi.GetFontData
title: GetFontData function (wingdi.h)
description: The GetFontData function retrieves font metric data for a TrueType font.
helpviewer_keywords: ["GetFontData","GetFontData function [Windows GDI]","_win32_GetFontData","gdi.getfontdata","wingdi/GetFontData"]
old-location: gdi\getfontdata.htm
tech.root: gdi
ms.assetid: ec716ad8-bdc2-4f61-968e-f86288123cec
ms.date: 12/05/2018
ms.keywords: GetFontData, GetFontData function [Windows GDI], _win32_GetFontData, gdi.getfontdata, wingdi/GetFontData
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
 - GetFontData
 - wingdi/GetFontData
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
 - GetFontData
---

# GetFontData function


## -description

The <b>GetFontData</b> function retrieves font metric data for a TrueType font.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param dwTable [in]

The name of a font metric table from which the font data is to be retrieved. This parameter can identify one of the metric tables documented in the TrueType Font Files specification published by Microsoft Corporation. If this parameter is zero, the information is retrieved starting at the beginning of the file for TrueType font files or from the beginning of the data for the currently selected font for TrueType Collection files. To retrieve the data from the beginning of the file for TrueType Collection files specify 'ttcf' (0x66637474).

### -param dwOffset [in]

The offset from the beginning of the font metric table to the location where the function should begin retrieving information. If this parameter is zero, the information is retrieved starting at the beginning of the table specified by the <i>dwTable</i> parameter. If this value is greater than or equal to the size of the table, an error occurs.

### -param pvBuffer [out]

A pointer to a buffer that receives the font information. If this parameter is <b>NULL</b>, the function returns the size of the buffer required for the font data.

### -param cjBuffer [in]

The length, in bytes, of the information to be retrieved. If this parameter is zero, <b>GetFontData</b> returns the size of the data specified in the <i>dwTable</i> parameter.

## -returns

If the function succeeds, the return value is the number of bytes returned.

If the function fails, the return value is GDI_ERROR.

## -remarks

This function is intended to be used to retrieve TrueType font information directly from the font file by font-manipulation applications. For information about embedding fonts see the <a href="/windows/desktop/gdi/font-embedding-reference">Font Embedding Reference</a>.

An application can sometimes use the <b>GetFontData</b> function to save a TrueType font with a document. To do this, the application determines whether the font can be embedded by checking the <b>otmfsType</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-outlinetextmetrica">OUTLINETEXTMETRIC</a> structure. If bit 1 of <b>otmfsType</b> is set, embedding is not permitted for the font. If bit 1 is clear, the font can be embedded. If bit 2 is set, the embedding is read-only. If embedding is permitted, the application can retrieve the entire font file, specifying zero for the <i>dwTable</i>, <i>dwOffset</i>, and <i>cbData</i> parameters.

If an application attempts to use this function to retrieve information for a non-TrueType font, an error occurs.

## -see-also

<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-gettextmetrics">GetTextMetrics</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-outlinetextmetrica">OUTLINETEXTMETRIC</a>