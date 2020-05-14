---
UID: NF:windows.graphics.imaging.interop.ISoftwareBitmapNativeFactory.CreateFromWICBitmap
title: ISoftwareBitmapNativeFactory::imaging (windows.graphics.imaging.interop.h)
description: Creates an ISoftwareBitmapNative from the provided IWICBitmap.helpviewer_keywords: ["CreateFromWICBitmap","CreateFromWICBitmap method [Windows Runtime]","CreateFromWICBitmap method [Windows Runtime]","ISoftwareBitmapNativeFactory interface","ISoftwareBitmapNativeFactory interface [Windows Runtime]","CreateFromWICBitmap method","ISoftwareBitmapNativeFactory.CreateFromWICBitmap","ISoftwareBitmapNativeFactory.imaging","ISoftwareBitmapNativeFactory::CreateFromWICBitmap","ISoftwareBitmapNativeFactory::imaging","windows/ISoftwareBitmapNativeFactory::CreateFromWICBitmap","winrt.isoftwarebitmapnativefactory_createfromwicbitmap"]
old-location: winrt\isoftwarebitmapnativefactory_createfromwicbitmap.htm
tech.root: WinRT
ms.assetid: D52F70E8-AF26-40A5-8E9E-1A5B9D20E35F
ms.date: 12/05/2018
ms.keywords: CreateFromWICBitmap, CreateFromWICBitmap method [Windows Runtime], CreateFromWICBitmap method [Windows Runtime],ISoftwareBitmapNativeFactory interface, ISoftwareBitmapNativeFactory interface [Windows Runtime],CreateFromWICBitmap method, ISoftwareBitmapNativeFactory.CreateFromWICBitmap, ISoftwareBitmapNativeFactory.imaging, ISoftwareBitmapNativeFactory::CreateFromWICBitmap, ISoftwareBitmapNativeFactory::imaging, windows/ISoftwareBitmapNativeFactory::CreateFromWICBitmap, winrt.isoftwarebitmapnativefactory_createfromwicbitmap
f1_keywords:
- windows.graphics.imaging.interop/ISoftwareBitmapNativeFactory.CreateFromWICBitmap
dev_langs:
- c++
req.header: windows.graphics.imaging.interop.h
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
req.lib: Windows.graphics.imaging.interop.lib
req.dll: Windows.graphics.imaging.interop.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- windows.graphics.imaging.interop.dll
api_name:
- ISoftwareBitmapNativeFactory.CreateFromWICBitmap
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISoftwareBitmapNativeFactory::imaging


## -description


Creates an <a href="https://docs.microsoft.com/windows/desktop/api/windows.graphics.imaging.interop/nn-windows-graphics-imaging-interop-isoftwarebitmapnative">ISoftwareBitmapNative</a>  from the provided <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmap">IWICBitmap</a>.


## -parameters




### -param data [in]

Type: <b>IWICBitmap*</b>

The source WIC bitmap.


### -param forceReadOnly [in]

Type: <b>BOOL</b>

A value indicating whether the created software bitmap is read-only.

<div class="alert"><b>Note</b>  The read-only access applies only to the Windows Runtime<a href="https://docs.microsoft.com/uwp/api/windows.graphics.imaging.softwarebitmap">SoftwareBitmap</a> wrapper. Access to the underlying Media Foundation buffer is not restricted.</div>
<div> </div>

### -param riid [in]

Type: <b>REFIID</b>

The IID of the <a href="https://docs.microsoft.com/windows/desktop/api/windows.graphics.imaging.interop/nn-windows-graphics-imaging-interop-isoftwarebitmapnative">ISoftwareBitmapNative</a> interface.


### -param ppv [out]

Type: <b>LPVOID*</b>

When this method returns successfully, contains the requested interface.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK on successful completion.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/windows.graphics.imaging.interop/nn-windows-graphics-imaging-interop-isoftwarebitmapnativefactory">ISoftwareBitmapNativeFactory</a>
 

 

