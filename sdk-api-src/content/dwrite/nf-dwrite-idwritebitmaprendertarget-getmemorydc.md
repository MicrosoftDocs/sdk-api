---
UID: NF:dwrite.IDWriteBitmapRenderTarget.GetMemoryDC
title: IDWriteBitmapRenderTarget::GetMemoryDC (dwrite.h)
description: Gets a handle to the memory device context.
helpviewer_keywords: ["GetMemoryDC","GetMemoryDC method [Direct Write]","GetMemoryDC method [Direct Write]","IDWriteBitmapRenderTarget interface","IDWriteBitmapRenderTarget interface [Direct Write]","GetMemoryDC method","IDWriteBitmapRenderTarget.GetMemoryDC","IDWriteBitmapRenderTarget::GetMemoryDC","directwrite.IDWriteBitmapRenderTarget_GetMemoryDC","dwrite/IDWriteBitmapRenderTarget::GetMemoryDC"]
old-location: directwrite\IDWriteBitmapRenderTarget_GetMemoryDC.htm
tech.root: DirectWrite
ms.assetid: 9ca9a002-2a78-4c7c-926c-52414dd801bb
ms.date: 12/05/2018
ms.keywords: GetMemoryDC, GetMemoryDC method [Direct Write], GetMemoryDC method [Direct Write],IDWriteBitmapRenderTarget interface, IDWriteBitmapRenderTarget interface [Direct Write],GetMemoryDC method, IDWriteBitmapRenderTarget.GetMemoryDC, IDWriteBitmapRenderTarget::GetMemoryDC, directwrite.IDWriteBitmapRenderTarget_GetMemoryDC, dwrite/IDWriteBitmapRenderTarget::GetMemoryDC
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IDWriteBitmapRenderTarget::GetMemoryDC
 - dwrite/IDWriteBitmapRenderTarget::GetMemoryDC
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
 - IDWriteBitmapRenderTarget.GetMemoryDC
---

# IDWriteBitmapRenderTarget::GetMemoryDC


## -description

 Gets a handle to the memory device context.



## -returns

Type: <b>HDC</b>

Returns a device context handle to the memory device context.

## -remarks

 An application can use the device context to draw using GDI functions. An application can obtain the bitmap handle
     (HBITMAP) by calling <a href="/windows/win32/api/wingdi/nf-wingdi-getcurrentobject">GetCurrentObject</a>. An application that wants information about the underlying bitmap, including
     a pointer to the pixel data, can call <a href="/windows/win32/api/wingdi/nf-wingdi-getobject">GetObject</a> to fill in a <a href="/windows/win32/api/wingdi/ns-wingdi-dibsection">DIBSECTION</a> structure. The bitmap is always a 32-bit 
     top-down DIB.

Note that this method takes no parameters and returns an HDC variable, not an HRESULT.


```cpp
memoryHdc = g_pBitmapRenderTarget->GetMemoryDC();

```


The HDC returned here is still owned by the bitmap render target object and should not be released or deleted by the client.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget">IDWriteBitmapRenderTarget</a>

