---
UID: NF:windows.graphics.imaging.interop.ISoftwareBitmapNativeFactory.CreateFromWICBitmap
title: ISoftwareBitmapNativeFactory::CreateFromWICBitmap (windows.graphics.imaging.interop.h)
description: Creates an ISoftwareBitmapNative from the provided IWICBitmap.
helpviewer_keywords: ["CreateFromWICBitmap","CreateFromWICBitmap method [Windows Runtime]","CreateFromWICBitmap method [Windows Runtime]","ISoftwareBitmapNativeFactory interface","ISoftwareBitmapNativeFactory interface [Windows Runtime]","CreateFromWICBitmap method","ISoftwareBitmapNativeFactory.CreateFromWICBitmap","ISoftwareBitmapNativeFactory.imaging","ISoftwareBitmapNativeFactory::CreateFromWICBitmap","ISoftwareBitmapNativeFactory::imaging","windows/ISoftwareBitmapNativeFactory::CreateFromWICBitmap","winrt.isoftwarebitmapnativefactory_createfromwicbitmap"]
old-location: winrt\isoftwarebitmapnativefactory_createfromwicbitmap.htm
tech.root: WinRT
ms.assetid: D52F70E8-AF26-40A5-8E9E-1A5B9D20E35F
ms.date: 12/05/2018
ms.keywords: CreateFromWICBitmap, CreateFromWICBitmap method [Windows Runtime], CreateFromWICBitmap method [Windows Runtime],ISoftwareBitmapNativeFactory interface, ISoftwareBitmapNativeFactory interface [Windows Runtime],CreateFromWICBitmap method, ISoftwareBitmapNativeFactory.CreateFromWICBitmap, ISoftwareBitmapNativeFactory.imaging, ISoftwareBitmapNativeFactory::CreateFromWICBitmap, ISoftwareBitmapNativeFactory::imaging, windows/ISoftwareBitmapNativeFactory::CreateFromWICBitmap, winrt.isoftwarebitmapnativefactory_createfromwicbitmap
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISoftwareBitmapNativeFactory::CreateFromWICBitmap
 - windows.graphics.imaging.interop/ISoftwareBitmapNativeFactory::CreateFromWICBitmap
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - windows.graphics.imaging.interop.dll
api_name:
 - ISoftwareBitmapNativeFactory.CreateFromWICBitmap
---

# ISoftwareBitmapNativeFactory::CreateFromWICBitmap (windows.graphics.imaging.interop.h)


## -description

Creates a Windows Runtime <a href="/uwp/api/windows.graphics.imaging.softwarebitmap">SoftwareBitmap</a> object from the provided <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmap">IWICBitmap</a>.

## -parameters

### -param data [in]

Type: <b>IWICBitmap*</b>

The source WIC bitmap.

### -param forceReadOnly [in]

Type: <b>BOOL</b>

A value indicating whether the created software bitmap is read-only.

<div class="alert"><b>Note</b>  The read-only access applies only to the Windows Runtime <a href="/uwp/api/windows.graphics.imaging.softwarebitmap">SoftwareBitmap</a> object. Access to the underlying WIC bitmap is not restricted.</div>

### -param riid [in]

Type: <b>REFIID</b>

The interface to obtain from the created <a href="/uwp/api/windows.graphics.imaging.softwarebitmap">SoftwareBitmap</a> object.
This is usually Windows.Graphics.Imaging.ISoftwareBitmap.

### -param ppv [out]

Type: <b>LPVOID*</b>

When this method returns successfully, contains the requested interface.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK on successful completion.

## -see-also

<a href="/windows/desktop/api/windows.graphics.imaging.interop/nn-windows-graphics-imaging-interop-isoftwarebitmapnativefactory">ISoftwareBitmapNativeFactory</a>
