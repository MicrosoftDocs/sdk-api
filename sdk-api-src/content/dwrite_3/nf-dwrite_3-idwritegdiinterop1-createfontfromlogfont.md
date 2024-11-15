---
UID: NF:dwrite_3.IDWriteGdiInterop1.CreateFontFromLOGFONT
title: IDWriteGdiInterop1::CreateFontFromLOGFONT (dwrite_3.h)
description: Creates a font object that matches the properties specified by the LOGFONT structure. (IDWriteGdiInterop1.CreateFontFromLOGFONT)
helpviewer_keywords: ["CreateFontFromLOGFONT","CreateFontFromLOGFONT method [Direct Write]","CreateFontFromLOGFONT method [Direct Write]","IDWriteGdiInterop1 interface","IDWriteGdiInterop1 interface [Direct Write]","CreateFontFromLOGFONT method","IDWriteGdiInterop1.CreateFontFromLOGFONT","IDWriteGdiInterop1::CreateFontFromLOGFONT","directwrite.idwritegdiinterop1_createfontfromlogfont","dwrite_3/IDWriteGdiInterop1::CreateFontFromLOGFONT"]
old-location: directwrite\idwritegdiinterop1_createfontfromlogfont.htm
tech.root: DirectWrite
ms.assetid: AA28755A-C2E3-4177-A5DD-61D9809A9D0E
ms.date: 12/05/2018
ms.keywords: CreateFontFromLOGFONT, CreateFontFromLOGFONT method [Direct Write], CreateFontFromLOGFONT method [Direct Write],IDWriteGdiInterop1 interface, IDWriteGdiInterop1 interface [Direct Write],CreateFontFromLOGFONT method, IDWriteGdiInterop1.CreateFontFromLOGFONT, IDWriteGdiInterop1::CreateFontFromLOGFONT, directwrite.idwritegdiinterop1_createfontfromlogfont, dwrite_3/IDWriteGdiInterop1::CreateFontFromLOGFONT
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
 - IDWriteGdiInterop1::CreateFontFromLOGFONT
 - dwrite_3/IDWriteGdiInterop1::CreateFontFromLOGFONT
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
 - IDWriteGdiInterop1.CreateFontFromLOGFONT
---

# IDWriteGdiInterop1::CreateFontFromLOGFONT


## -description

Creates a font object that matches the properties specified by the LOGFONT structure.

## -parameters

### -param logFont [in]

Type: <b>LOGFONTW</b>

Structure containing a GDI-compatible font description.

### -param fontCollection [in, optional]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection">IDWriteFontCollection</a>*</b>

The font collection to search. If NULL, the local system font collection is used.

### -param font [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefont">IDWriteFont</a>**</b>

Receives a newly created font object if successful, or NULL in case of error.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritegdiinterop1">IDWriteGdiInterop1</a>

