---
UID: NF:dwrite.IDWriteGdiInterop.CreateFontFaceFromHdc
title: IDWriteGdiInterop::CreateFontFaceFromHdc (dwrite.h)
description: Creates an IDWriteFontFace object that corresponds to the currently selected HFONT of the specified HDC.
helpviewer_keywords: ["CreateFontFaceFromHdc","CreateFontFaceFromHdc method [Direct Write]","CreateFontFaceFromHdc method [Direct Write]","IDWriteGdiInterop interface","IDWriteGdiInterop interface [Direct Write]","CreateFontFaceFromHdc method","IDWriteGdiInterop.CreateFontFaceFromHdc","IDWriteGdiInterop::CreateFontFaceFromHdc","directwrite.IDWriteGdiInterop_CreateFontFaceFromHdc","dwrite/IDWriteGdiInterop::CreateFontFaceFromHdc"]
old-location: directwrite\IDWriteGdiInterop_CreateFontFaceFromHdc.htm
tech.root: DirectWrite
ms.assetid: 583acf9a-2982-4491-bc57-8cf6bfc98598
ms.date: 12/05/2018
ms.keywords: CreateFontFaceFromHdc, CreateFontFaceFromHdc method [Direct Write], CreateFontFaceFromHdc method [Direct Write],IDWriteGdiInterop interface, IDWriteGdiInterop interface [Direct Write],CreateFontFaceFromHdc method, IDWriteGdiInterop.CreateFontFaceFromHdc, IDWriteGdiInterop::CreateFontFaceFromHdc, directwrite.IDWriteGdiInterop_CreateFontFaceFromHdc, dwrite/IDWriteGdiInterop::CreateFontFaceFromHdc
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
 - IDWriteGdiInterop::CreateFontFaceFromHdc
 - dwrite/IDWriteGdiInterop::CreateFontFaceFromHdc
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
 - IDWriteGdiInterop.CreateFontFaceFromHdc
---

# IDWriteGdiInterop::CreateFontFaceFromHdc


## -description

 Creates an <b>IDWriteFontFace</b> object that corresponds to the currently selected <b>HFONT</b> of the specified <b>HDC</b>.

## -parameters

### -param hdc

Type: <b>HDC</b>

A handle to a device context into which a font has been selected. It is assumed that the client
     has already performed font mapping and that the font selected into the device context is the actual font to be used 
     for rendering glyphs.

### -param fontFace [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontface">IDWriteFontFace</a>**</b>

Contains an address of a pointer to  the newly created font face object, or <b>NULL</b> in case of failure. The font face returned is guaranteed to reference the same physical typeface that would be used for drawing glyphs (but not necessarily characters) using ExtTextOut.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function is intended for scenarios in which an application wants to use GDI and Uniscribe 1.x for text layout and shaping, but  DirectWrite for final rendering. This function assumes the client is performing text output using glyph indexes.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop">IDWriteGdiInterop</a>

