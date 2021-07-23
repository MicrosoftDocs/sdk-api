---
UID: NF:d2d1.ID2D1RenderTarget.CreateBitmap(D2D1_SIZE_U,constD2D1_BITMAP_PROPERTIES&,ID2D1Bitmap)
title: ID2D1RenderTarget::CreateBitmap(D2D1_SIZE_U,const D2D1_BITMAP_PROPERTIES &,ID2D1Bitmap) (d2d1.h)
description: Creates an uninitialized Direct2D bitmap.
helpviewer_keywords: ["CreateBitmap","CreateBitmap method [Direct2D]","CreateBitmap method [Direct2D]","ID2D1RenderTarget interface","ID2D1RenderTarget interface [Direct2D]","CreateBitmap method","ID2D1RenderTarget.CreateBitmap","ID2D1RenderTarget.CreateBitmap(D2D1_SIZE_U","const D2D1_BITMAP_PROPERTIES &","ID2D1Bitmap)","ID2D1RenderTarget::CreateBitmap","ID2D1RenderTarget::CreateBitmap(D2D1_SIZE_U","const D2D1_BITMAP_PROPERTIES &","ID2D1Bitmap)","d2d1/ID2D1RenderTarget::CreateBitmap","direct2d.ID2D1RenderTarget_CreateBitmap_D2D_SIZE_U_ref_D2D1_BITMAP_PROPERTIES_ptr_ptr_ID2D1Bitmap"]
old-location: direct2d\ID2D1RenderTarget_CreateBitmap_D2D_SIZE_U_ref_D2D1_BITMAP_PROPERTIES_ptr_ptr_ID2D1Bitmap.htm
tech.root: Direct2D
ms.assetid: 134453e3-180a-4682-a748-b74c6113be6e
ms.date: 12/05/2018
ms.keywords: CreateBitmap, CreateBitmap method [Direct2D], CreateBitmap method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],CreateBitmap method, ID2D1RenderTarget.CreateBitmap, ID2D1RenderTarget.CreateBitmap(D2D1_SIZE_U,const D2D1_BITMAP_PROPERTIES &,ID2D1Bitmap), ID2D1RenderTarget::CreateBitmap, ID2D1RenderTarget::CreateBitmap(D2D1_SIZE_U,const D2D1_BITMAP_PROPERTIES &,ID2D1Bitmap), d2d1/ID2D1RenderTarget::CreateBitmap, direct2d.ID2D1RenderTarget_CreateBitmap_D2D_SIZE_U_ref_D2D1_BITMAP_PROPERTIES_ptr_ptr_ID2D1Bitmap
req.header: d2d1.h
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1RenderTarget::CreateBitmap
 - d2d1/ID2D1RenderTarget::CreateBitmap
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1RenderTarget.CreateBitmap
---

## -description

Creates an uninitialized Direct2D bitmap.

## -parameters

### -param size

Type: [in] <b><a href="/windows/win32/Direct2D/d2d1-size-u">D2D1_SIZE_U</a></b>

The dimension of the bitmap to create in pixels.

### -param bitmapProperties

Type: [in] <b>const <a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_bitmap_properties">D2D1_BITMAP_PROPERTIES</a> &</b>

The pixel format and dots per inch (DPI) of the bitmap to create.

### -param bitmap

Type: [out] <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a>**</b>

When this method returns, contains a pointer to a pointer to the new bitmap. This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

