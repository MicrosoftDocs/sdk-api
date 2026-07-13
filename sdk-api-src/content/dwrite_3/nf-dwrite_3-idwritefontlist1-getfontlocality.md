---
UID: NF:dwrite_3.IDWriteFontList1.GetFontLocality
title: IDWriteFontList1::GetFontLocality (dwrite_3.h)
description: Gets the current location of a font given its zero-based index. (IDWriteFontList1.GetFontLocality)
helpviewer_keywords: ["GetFontLocality","GetFontLocality method [Direct Write]","GetFontLocality method [Direct Write]","IDWriteFontList1 interface","IDWriteFontList1 interface [Direct Write]","GetFontLocality method","IDWriteFontList1.GetFontLocality","IDWriteFontList1::GetFontLocality","directwrite.idwritefontlist1_getfontlocality","dwrite_3/IDWriteFontList1::GetFontLocality"]
old-location: directwrite\idwritefontlist1_getfontlocality.htm
tech.root: DirectWrite
ms.assetid: A48641B8-0BFF-42B9-A093-A26404EC22C5
ms.date: 09/10/2025
ms.keywords: GetFontLocality, GetFontLocality method [Direct Write], GetFontLocality method [Direct Write],IDWriteFontList1 interface, IDWriteFontList1 interface [Direct Write],GetFontLocality method, IDWriteFontList1.GetFontLocality, IDWriteFontList1::GetFontLocality, directwrite.idwritefontlist1_getfontlocality, dwrite_3/IDWriteFontList1::GetFontLocality
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IDWriteFontList1::GetFontLocality
 - dwrite_3/IDWriteFontList1::GetFontLocality
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
 - IDWriteFontList1.GetFontLocality
---

# IDWriteFontList1::GetFontLocality


## -description

Gets the current location of a font given its zero-based index.

## -parameters

### -param listIndex [in]

Type: <b>UINT32</b>

Zero-based index of the font in the font list.

## -returns

Type: <b><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_locality">DWRITE_LOCALITY</a></b>

Returns a <a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_locality">DWRITE_LOCALITY</a>-typed value that specifies the location of the specified font.

## -remarks

For fully local files, the result will always be <b>DWRITE_LOCALITY_LOCAL</b>. For streamed files, the result depends on how much of the file has been downloaded. <a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontlist1-getfont">GetFont</a> fails if the locality is <b>DWRITE_LOCALITY_REMOTE</b> and potentially fails if <b>DWRITE_LOCALITY_PARTIAL</b>.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontlist1">IDWriteFontList1</a>

