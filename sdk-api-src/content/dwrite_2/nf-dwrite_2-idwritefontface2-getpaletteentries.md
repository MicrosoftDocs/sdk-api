---
UID: NF:dwrite_2.IDWriteFontFace2.GetPaletteEntries
title: IDWriteFontFace2::GetPaletteEntries (dwrite_2.h)
description: Gets color values from the font's color palette.
helpviewer_keywords: ["GetPaletteEntries","GetPaletteEntries method [Direct Write]","GetPaletteEntries method [Direct Write]","IDWriteFontFace2 interface","IDWriteFontFace2 interface [Direct Write]","GetPaletteEntries method","IDWriteFontFace2.GetPaletteEntries","IDWriteFontFace2::GetPaletteEntries","directwrite.idwritefontface2_getpaletteentries","dwrite_2/IDWriteFontFace2::GetPaletteEntries"]
old-location: directwrite\idwritefontface2_getpaletteentries.htm
tech.root: DirectWrite
ms.assetid: 4678E96C-A5E6-4294-8927-B71F55149342
ms.date: 12/05/2018
ms.keywords: GetPaletteEntries, GetPaletteEntries method [Direct Write], GetPaletteEntries method [Direct Write],IDWriteFontFace2 interface, IDWriteFontFace2 interface [Direct Write],GetPaletteEntries method, IDWriteFontFace2.GetPaletteEntries, IDWriteFontFace2::GetPaletteEntries, directwrite.idwritefontface2_getpaletteentries, dwrite_2/IDWriteFontFace2::GetPaletteEntries
req.header: dwrite_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteFontFace2::GetPaletteEntries
 - dwrite_2/IDWriteFontFace2::GetPaletteEntries
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFontFace2.GetPaletteEntries
---

# IDWriteFontFace2::GetPaletteEntries


## -description

Gets color values from the font's color palette.

## -parameters

### -param colorPaletteIndex

Zero-based index of the color palette. If the font does not have a palette with the specified index, the method returns <b>DWRITE_E_NOCOLOR</b>.

### -param firstEntryIndex

Zero-based index of the first palette entry to read.

### -param entryCount

Number of palette entries to read.

### -param paletteEntries [out]

Array that receives the color values.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_INVALIDARG</dt>
</dl>
</td>
<td width="60%">
The sum of <i>firstEntryIndex</i> and <i>entryCount</i> is greater
    than the actual number of palette entries that's returned by the <a href="/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontface2-getpaletteentrycount">GetPaletteEntryCount</a> method.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>DWRITE_E_NOCOLOR</dt>
</dl>
</td>
<td width="60%">
The font doesn't have a palette with the specified palette index.

</td>
</tr>
</table>

## -see-also

<a href="/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontface2">IDWriteFontFace2</a>

