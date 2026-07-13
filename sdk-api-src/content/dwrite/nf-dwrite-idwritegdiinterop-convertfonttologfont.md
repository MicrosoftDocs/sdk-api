---
UID: NF:dwrite.IDWriteGdiInterop.ConvertFontToLOGFONT
title: IDWriteGdiInterop::ConvertFontToLOGFONT (dwrite.h)
description: Initializes a LOGFONT structure based on the GDI-compatible properties of the specified font. (IDWriteGdiInterop.ConvertFontToLOGFONT)
helpviewer_keywords: ["ConvertFontToLOGFONT","ConvertFontToLOGFONT method [Direct Write]","ConvertFontToLOGFONT method [Direct Write]","IDWriteGdiInterop interface","IDWriteGdiInterop interface [Direct Write]","ConvertFontToLOGFONT method","IDWriteGdiInterop.ConvertFontToLOGFONT","IDWriteGdiInterop::ConvertFontToLOGFONT","directwrite.IDWriteGdiInterop_ConvertFontToLOGFONT","dwrite/IDWriteGdiInterop::ConvertFontToLOGFONT"]
old-location: directwrite\IDWriteGdiInterop_ConvertFontToLOGFONT.htm
tech.root: DirectWrite
ms.assetid: 7b6e65a6-a3cd-438b-8116-7f9614e420df
ms.date: 12/05/2018
ms.keywords: ConvertFontToLOGFONT, ConvertFontToLOGFONT method [Direct Write], ConvertFontToLOGFONT method [Direct Write],IDWriteGdiInterop interface, IDWriteGdiInterop interface [Direct Write],ConvertFontToLOGFONT method, IDWriteGdiInterop.ConvertFontToLOGFONT, IDWriteGdiInterop::ConvertFontToLOGFONT, directwrite.IDWriteGdiInterop_ConvertFontToLOGFONT, dwrite/IDWriteGdiInterop::ConvertFontToLOGFONT
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
 - IDWriteGdiInterop::ConvertFontToLOGFONT
 - dwrite/IDWriteGdiInterop::ConvertFontToLOGFONT
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
 - IDWriteGdiInterop.ConvertFontToLOGFONT
---

# IDWriteGdiInterop::ConvertFontToLOGFONT


## -description

 Initializes a <b>LOGFONT</b> structure based on the GDI-compatible properties of the specified font.

## -parameters

### -param font

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefont">IDWriteFont</a>*</b>

An <a href="/windows/win32/api/dwrite/nn-dwrite-idwritefont">IDWriteFont</a> object to be converted into a GDI-compatible <b>LOGFONT</b> structure.

### -param logFont [out]

Type: <b>LOGFONTW*</b>

When this method returns, contains a structure that receives a GDI-compatible font description.

### -param isSystemFont [out]

Type: <b>BOOL*</b>

When this method returns, contains <b>TRUE</b> if the specified font object is part of the system font collection; otherwise, <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The conversion to a  <b>LOGFONT</b> by using <b>ConvertFontToLOGFONT</b> operates at the logical font level and does not guarantee that it will map to a specific physical font. It is not guaranteed that GDI will select the same physical font for displaying  text formatted by a <b>LOGFONT</b> as the <a href="/windows/win32/api/dwrite/nn-dwrite-idwritefont">IDWriteFont</a> object that was converted.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop">IDWriteGdiInterop</a>

