---
UID: NF:dwrite.IDWriteGdiInterop.ConvertFontFaceToLOGFONT
title: IDWriteGdiInterop::ConvertFontFaceToLOGFONT (dwrite.h)
description: Initializes a LOGFONT structure based on the GDI-compatible properties of the specified font. (IDWriteGdiInterop.ConvertFontFaceToLOGFONT)
helpviewer_keywords: ["ConvertFontFaceToLOGFONT","ConvertFontFaceToLOGFONT method [Direct Write]","ConvertFontFaceToLOGFONT method [Direct Write]","IDWriteGdiInterop interface","IDWriteGdiInterop interface [Direct Write]","ConvertFontFaceToLOGFONT method","IDWriteGdiInterop.ConvertFontFaceToLOGFONT","IDWriteGdiInterop::ConvertFontFaceToLOGFONT","directwrite.IDWriteGdiInterop_ConvertFontFaceToLOGFONT","dwrite/IDWriteGdiInterop::ConvertFontFaceToLOGFONT"]
old-location: directwrite\IDWriteGdiInterop_ConvertFontFaceToLOGFONT.htm
tech.root: DirectWrite
ms.assetid: 1f863d1b-fdf5-4c2b-97ff-682b22c61a81
ms.date: 12/05/2018
ms.keywords: ConvertFontFaceToLOGFONT, ConvertFontFaceToLOGFONT method [Direct Write], ConvertFontFaceToLOGFONT method [Direct Write],IDWriteGdiInterop interface, IDWriteGdiInterop interface [Direct Write],ConvertFontFaceToLOGFONT method, IDWriteGdiInterop.ConvertFontFaceToLOGFONT, IDWriteGdiInterop::ConvertFontFaceToLOGFONT, directwrite.IDWriteGdiInterop_ConvertFontFaceToLOGFONT, dwrite/IDWriteGdiInterop::ConvertFontFaceToLOGFONT
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
 - IDWriteGdiInterop::ConvertFontFaceToLOGFONT
 - dwrite/IDWriteGdiInterop::ConvertFontFaceToLOGFONT
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
 - IDWriteGdiInterop.ConvertFontFaceToLOGFONT
---

# IDWriteGdiInterop::ConvertFontFaceToLOGFONT


## -description

 Initializes a LOGFONT structure based on the GDI-compatible properties of the specified font.

## -parameters

### -param font

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontface">IDWriteFontFace</a>*</b>

An <a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontface">IDWriteFontFace</a> object to be converted into a GDI-compatible LOGFONT structure.

### -param logFont [out]

Type: <b>LOGFONTW*</b>

When this method returns, contains a pointer to a structure that receives a GDI-compatible font description.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The conversion to a  LOGFONT by using <b>ConvertFontFaceToLOGFONT</b> operates at the logical font level and does not guarantee that it will map to a specific physical font. It is not guaranteed that GDI will select the same physical font for displaying  text formatted by a LOGFONT as the <a href="/windows/win32/api/dwrite/nn-dwrite-idwritefont">IDWriteFont</a> object that was converted.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop">IDWriteGdiInterop</a>

