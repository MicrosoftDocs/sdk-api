---
UID: NF:dwrite.IDWriteGdiInterop.CreateFontFromLOGFONT
title: IDWriteGdiInterop::CreateFontFromLOGFONT (dwrite.h)
description: Creates a font object that matches the properties specified by the LOGFONT structure. (IDWriteGdiInterop.CreateFontFromLOGFONT)
helpviewer_keywords: ["CreateFontFromLOGFONT","CreateFontFromLOGFONT method [Direct Write]","CreateFontFromLOGFONT method [Direct Write]","IDWriteGdiInterop interface","IDWriteGdiInterop interface [Direct Write]","CreateFontFromLOGFONT method","IDWriteGdiInterop.CreateFontFromLOGFONT","IDWriteGdiInterop::CreateFontFromLOGFONT","directwrite.IDWriteGdiInterop_CreateFontFromLOGFONT","dwrite/IDWriteGdiInterop::CreateFontFromLOGFONT"]
old-location: directwrite\IDWriteGdiInterop_CreateFontFromLOGFONT.htm
tech.root: DirectWrite
ms.assetid: d083123a-1b45-4c18-9490-6ce038bb6b22
ms.date: 12/05/2018
ms.keywords: CreateFontFromLOGFONT, CreateFontFromLOGFONT method [Direct Write], CreateFontFromLOGFONT method [Direct Write],IDWriteGdiInterop interface, IDWriteGdiInterop interface [Direct Write],CreateFontFromLOGFONT method, IDWriteGdiInterop.CreateFontFromLOGFONT, IDWriteGdiInterop::CreateFontFromLOGFONT, directwrite.IDWriteGdiInterop_CreateFontFromLOGFONT, dwrite/IDWriteGdiInterop::CreateFontFromLOGFONT
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - IDWriteGdiInterop::CreateFontFromLOGFONT
 - dwrite/IDWriteGdiInterop::CreateFontFromLOGFONT
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
 - IDWriteGdiInterop.CreateFontFromLOGFONT
---

# IDWriteGdiInterop::CreateFontFromLOGFONT


## -description

 Creates a font object that matches the properties specified by the <b>LOGFONT</b> structure.

## -parameters

### -param logFont [in]

Type: <b>const LOGFONTW*</b>

A structure containing a GDI-compatible font description.

### -param font [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefont">IDWriteFont</a>**</b>

When this method returns, contains an address of a  pointer to a newly created <a href="/windows/win32/api/dwrite/nn-dwrite-idwritefont">IDWriteFont</a>  object if successful; otherwise, <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop">IDWriteGdiInterop</a>

