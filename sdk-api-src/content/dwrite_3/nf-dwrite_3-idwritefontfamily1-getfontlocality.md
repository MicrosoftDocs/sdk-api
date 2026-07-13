---
UID: NF:dwrite_3.IDWriteFontFamily1.GetFontLocality
title: IDWriteFontFamily1::GetFontLocality (dwrite_3.h)
description: Gets the current location of a font given its zero-based index. (IDWriteFontFamily1.GetFontLocality)
helpviewer_keywords: ["GetFontLocality","GetFontLocality method [Direct Write]","GetFontLocality method [Direct Write]","IDWriteFontFamily1 interface","IDWriteFontFamily1 interface [Direct Write]","GetFontLocality method","IDWriteFontFamily1.GetFontLocality","IDWriteFontFamily1::GetFontLocality","directwrite.idwritefontfamily1_getfontlocality","dwrite_3/IDWriteFontFamily1::GetFontLocality"]
old-location: directwrite\idwritefontfamily1_getfontlocality.htm
tech.root: DirectWrite
ms.assetid: 9D262E5C-4407-4110-A315-F529B809EDE2
ms.date: 09/10/2025
ms.keywords: GetFontLocality, GetFontLocality method [Direct Write], GetFontLocality method [Direct Write],IDWriteFontFamily1 interface, IDWriteFontFamily1 interface [Direct Write],GetFontLocality method, IDWriteFontFamily1.GetFontLocality, IDWriteFontFamily1::GetFontLocality, directwrite.idwritefontfamily1_getfontlocality, dwrite_3/IDWriteFontFamily1::GetFontLocality
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
 - IDWriteFontFamily1::GetFontLocality
 - dwrite_3/IDWriteFontFamily1::GetFontLocality
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
 - IDWriteFontFamily1.GetFontLocality
---

# IDWriteFontFamily1::GetFontLocality


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

For fully local files, the result will always be <b>DWRITE_LOCALITY_LOCAL</b>. For streamed files, the result depends on how much of the file has been downloaded. <a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfamily1-getfont">GetFont</a> fails if the locality is <b>DWRITE_LOCALITY_REMOTE</b> and potentially fails if <b>DWRITE_LOCALITY_PARTIAL</b>.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfamily1">IDWriteFontFamily1</a>

