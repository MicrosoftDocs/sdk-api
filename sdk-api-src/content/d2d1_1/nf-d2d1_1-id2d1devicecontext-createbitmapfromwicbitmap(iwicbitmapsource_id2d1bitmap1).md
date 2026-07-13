---
UID: NF:d2d1_1.ID2D1DeviceContext.CreateBitmapFromWicBitmap(IWICBitmapSource,ID2D1Bitmap1)
title: ID2D1DeviceContext::CreateBitmapFromWicBitmap(IWICBitmapSource,ID2D1Bitmap1) (d2d1_1.h)
description: Creates an ID2D1Bitmap by copying the specified Microsoft Windows Imaging Component (WIC) bitmap. (overload 1/4)
helpviewer_keywords: ["CreateBitmapFromWicBitmap","CreateBitmapFromWicBitmap interface [Direct2D]","CreateBitmapFromWicBitmap method","CreateBitmapFromWicBitmap method [Direct2D]","CreateBitmapFromWicBitmap method [Direct2D]","CreateBitmapFromWicBitmap interface","CreateBitmapFromWicBitmap::CreateBitmapFromWicBitmap","ID2D1DeviceContext.CreateBitmapFromWicBitmap","ID2D1DeviceContext.CreateBitmapFromWicBitmap(IWICBitmapSource","ID2D1Bitmap1)","ID2D1DeviceContext::CreateBitmapFromWicBitmap","ID2D1DeviceContext::CreateBitmapFromWicBitmap(IWICBitmapSource","ID2D1Bitmap1)","d2d1_3/CreateBitmapFromWicBitmap::CreateBitmapFromWicBitmap","direct2d.id2d1devicecontext_createbitmapfromwicbitmap_3"]
old-location: direct2d\id2d1devicecontext_createbitmapfromwicbitmap_3.htm
tech.root: Direct2D
ms.assetid: 6E8CAD85-DADD-4EF1-BD22-6437DEC3BD23
ms.date: 12/05/2018
ms.keywords: CreateBitmapFromWicBitmap, CreateBitmapFromWicBitmap interface [Direct2D],CreateBitmapFromWicBitmap method, CreateBitmapFromWicBitmap method [Direct2D], CreateBitmapFromWicBitmap method [Direct2D],CreateBitmapFromWicBitmap interface, CreateBitmapFromWicBitmap::CreateBitmapFromWicBitmap, ID2D1DeviceContext.CreateBitmapFromWicBitmap, ID2D1DeviceContext.CreateBitmapFromWicBitmap(IWICBitmapSource,ID2D1Bitmap1), ID2D1DeviceContext::CreateBitmapFromWicBitmap, ID2D1DeviceContext::CreateBitmapFromWicBitmap(IWICBitmapSource,ID2D1Bitmap1), d2d1_3/CreateBitmapFromWicBitmap::CreateBitmapFromWicBitmap, direct2d.id2d1devicecontext_createbitmapfromwicbitmap_3
req.header: d2d1_1.h
req.include-header: D2d1_1.h
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
req.lib: D2d1_3.lib
req.dll: D2d1_3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1DeviceContext::CreateBitmapFromWicBitmap
 - d2d1_1/ID2D1DeviceContext::CreateBitmapFromWicBitmap
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1_3.dll
api_name:
 - CreateBitmapFromWicBitmap.CreateBitmapFromWicBitmap
---

# ID2D1DeviceContext::CreateBitmapFromWicBitmap(IWICBitmapSource,ID2D1Bitmap1)


## -description

Creates an <a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a> by copying the specified Microsoft Windows Imaging Component (WIC) bitmap.

## -parameters

### -param wicBitmapSource [in]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a>*</b>

The WIC bitmap to copy.

### -param bitmap [out]

Type: <b><a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1bitmap1">ID2D1Bitmap1</a>**</b>

When this method returns, contains a pointer to a pointer to the new bitmap. This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>
