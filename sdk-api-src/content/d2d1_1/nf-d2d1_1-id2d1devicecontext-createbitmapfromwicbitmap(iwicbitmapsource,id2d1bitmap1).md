---
UID: NF:d2d1_1.ID2D1DeviceContext.CreateBitmapFromWicBitmap(IWICBitmapSource,ID2D1Bitmap1)
title: ID2D1DeviceContext::CreateBitmapFromWicBitmap(IWICBitmapSource,ID2D1Bitmap1)
author: windows-sdk-content
description: Creates an ID2D1Bitmap by copying the specified Microsoft Windows Imaging Component (WIC) bitmap.
old-location: direct2d\id2d1devicecontext_createbitmapfromwicbitmap_3.htm
tech.root: Direct2D
ms.assetid: 6E8CAD85-DADD-4EF1-BD22-6437DEC3BD23
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CreateBitmapFromWicBitmap, CreateBitmapFromWicBitmap interface [Direct2D],CreateBitmapFromWicBitmap method, CreateBitmapFromWicBitmap method [Direct2D], CreateBitmapFromWicBitmap method [Direct2D],CreateBitmapFromWicBitmap interface, CreateBitmapFromWicBitmap::CreateBitmapFromWicBitmap, ID2D1DeviceContext.CreateBitmapFromWicBitmap, ID2D1DeviceContext.CreateBitmapFromWicBitmap(IWICBitmapSource,ID2D1Bitmap1), ID2D1DeviceContext::CreateBitmapFromWicBitmap, ID2D1DeviceContext::CreateBitmapFromWicBitmap(IWICBitmapSource,ID2D1Bitmap1), d2d1_3/CreateBitmapFromWicBitmap::CreateBitmapFromWicBitmap, direct2d.id2d1devicecontext_createbitmapfromwicbitmap_3
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1_3.dll
api_name:
 - CreateBitmapFromWicBitmap.CreateBitmapFromWicBitmap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d2d1_1.h
: 
- ID2D1DeviceContext.CreateBitmapFromWicBitmap
: 
---

# ID2D1DeviceContext::CreateBitmapFromWicBitmap(IWICBitmapSource,ID2D1Bitmap1)


## -description


Creates an <a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a> by copying the specified Microsoft Windows Imaging Component (WIC) bitmap.
        


## -parameters




### -param wicBitmapSource [in]

Type: <b><a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a>*</b>

The WIC bitmap to copy.


### -param bitmap [out]

Type: <b><a href="https://msdn.microsoft.com/669a9377-248c-4a86-b447-ed117fff43a6">ID2D1Bitmap1</a>**</b>

When this method returns, contains a pointer to a pointer to the new bitmap. This parameter is passed uninitialized.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>
 

 

