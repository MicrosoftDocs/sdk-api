---
UID: NF:dwrite.IDWriteGdiInterop.CreateBitmapRenderTarget
title: IDWriteGdiInterop::CreateBitmapRenderTarget (dwrite.h)
description: Creates an object that encapsulates a bitmap and memory DC (device context) which can be used for rendering glyphs.
helpviewer_keywords: ["CreateBitmapRenderTarget","CreateBitmapRenderTarget method [Direct Write]","CreateBitmapRenderTarget method [Direct Write]","IDWriteGdiInterop interface","IDWriteGdiInterop interface [Direct Write]","CreateBitmapRenderTarget method","IDWriteGdiInterop.CreateBitmapRenderTarget","IDWriteGdiInterop::CreateBitmapRenderTarget","directwrite.IDWriteGdiInterop_CreateBitmapRenderTarget","dwrite/IDWriteGdiInterop::CreateBitmapRenderTarget"]
old-location: directwrite\IDWriteGdiInterop_CreateBitmapRenderTarget.htm
tech.root: DirectWrite
ms.assetid: 1a1bd200-6da6-4e4d-83d3-1f6a4a5e7152
ms.date: 12/05/2018
ms.keywords: CreateBitmapRenderTarget, CreateBitmapRenderTarget method [Direct Write], CreateBitmapRenderTarget method [Direct Write],IDWriteGdiInterop interface, IDWriteGdiInterop interface [Direct Write],CreateBitmapRenderTarget method, IDWriteGdiInterop.CreateBitmapRenderTarget, IDWriteGdiInterop::CreateBitmapRenderTarget, directwrite.IDWriteGdiInterop_CreateBitmapRenderTarget, dwrite/IDWriteGdiInterop::CreateBitmapRenderTarget
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
 - IDWriteGdiInterop::CreateBitmapRenderTarget
 - dwrite/IDWriteGdiInterop::CreateBitmapRenderTarget
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
 - IDWriteGdiInterop.CreateBitmapRenderTarget
---

# IDWriteGdiInterop::CreateBitmapRenderTarget


## -description

 Creates an object that encapsulates a bitmap and memory DC (device context) which can be used for rendering glyphs.

## -parameters

### -param hdc [in, optional]

Type: <b>HDC</b>

A handle to the optional device context used to create a compatible memory DC (device context).

### -param width

Type: <b>UINT32</b>

The width of the bitmap render target.

### -param height

Type: <b>UINT32</b>

The height of the bitmap render target.

### -param renderTarget [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget">IDWriteBitmapRenderTarget</a>**</b>

When this method returns, contains an address of a pointer to the newly created <a href="/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget">IDWriteBitmapRenderTarget</a> object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop">IDWriteGdiInterop</a>

