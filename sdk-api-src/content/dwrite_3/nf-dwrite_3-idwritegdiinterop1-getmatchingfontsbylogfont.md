---
UID: NF:dwrite_3.IDWriteGdiInterop1.GetMatchingFontsByLOGFONT
title: IDWriteGdiInterop1::GetMatchingFontsByLOGFONT (dwrite_3.h)
description: Gets a list of matching fonts based on the specified LOGFONT values. Only fonts of that family name will be returned.
helpviewer_keywords: ["GetMatchingFontsByLOGFONT","GetMatchingFontsByLOGFONT method [Direct Write]","GetMatchingFontsByLOGFONT method [Direct Write]","IDWriteGdiInterop1 interface","IDWriteGdiInterop1 interface [Direct Write]","GetMatchingFontsByLOGFONT method","IDWriteGdiInterop1.GetMatchingFontsByLOGFONT","IDWriteGdiInterop1::GetMatchingFontsByLOGFONT","directwrite.idwritegdiinterop1_getmatchingfontsbylogfont","dwrite_3/IDWriteGdiInterop1::GetMatchingFontsByLOGFONT"]
old-location: directwrite\idwritegdiinterop1_getmatchingfontsbylogfont.htm
tech.root: DirectWrite
ms.assetid: 38D547D2-0C1C-4673-83BD-38458DFD7E5A
ms.date: 09/10/2025
ms.keywords: GetMatchingFontsByLOGFONT, GetMatchingFontsByLOGFONT method [Direct Write], GetMatchingFontsByLOGFONT method [Direct Write],IDWriteGdiInterop1 interface, IDWriteGdiInterop1 interface [Direct Write],GetMatchingFontsByLOGFONT method, IDWriteGdiInterop1.GetMatchingFontsByLOGFONT, IDWriteGdiInterop1::GetMatchingFontsByLOGFONT, directwrite.idwritegdiinterop1_getmatchingfontsbylogfont, dwrite_3/IDWriteGdiInterop1::GetMatchingFontsByLOGFONT
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
 - IDWriteGdiInterop1::GetMatchingFontsByLOGFONT
 - dwrite_3/IDWriteGdiInterop1::GetMatchingFontsByLOGFONT
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
 - IDWriteGdiInterop1.GetMatchingFontsByLOGFONT
---

# IDWriteGdiInterop1::GetMatchingFontsByLOGFONT


## -description

Gets a list of matching fonts based on the specified LOGFONT values. Only fonts
        of that family name will be returned.

## -parameters

### -param logFont [in]

Type: <b>LOGFONT</b>

Structure containing a GDI-compatible font description.

### -param fontSet [in]

Type: <b><a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset">IDWriteFontSet</a>*</b>

The font set to search.

### -param filteredSet [out]

Type: <b><a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset">IDWriteFontSet</a>**</b>

&gt;Receives the filtered font set if successful.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritegdiinterop1">IDWriteGdiInterop1</a>

