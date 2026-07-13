---
UID: NF:windows.graphics.imaging.interop.ISoftwareBitmapNativeFactory.CreateFromMF2DBuffer2
title: ISoftwareBitmapNativeFactory::CreateFromMF2DBuffer2 (windows.graphics.imaging.interop.h)
description: Creates an ISoftwareBitmapNative from the provided IMF2DBuffer2.
helpviewer_keywords: ["CreateFromMF2DBuffer2","CreateFromMF2DBuffer2 method [Windows Runtime]","CreateFromMF2DBuffer2 method [Windows Runtime]","ISoftwareBitmapNativeFactory interface","ISoftwareBitmapNativeFactory interface [Windows Runtime]","CreateFromMF2DBuffer2 method","ISoftwareBitmapNativeFactory.CreateFromMF2DBuffer2","ISoftwareBitmapNativeFactory.imaging","ISoftwareBitmapNativeFactory::CreateFromMF2DBuffer2","ISoftwareBitmapNativeFactory::imaging","windows/ISoftwareBitmapNativeFactory::CreateFromMF2DBuffer2","winrt.isoftwarebitmapnativefactory_createfrommf2dbuffer2"]
old-location: winrt\isoftwarebitmapnativefactory_createfrommf2dbuffer2.htm
tech.root: WinRT
ms.assetid: F6B9E8B2-19CF-4921-9E9E-E387084E5F8B
ms.date: 12/05/2018
ms.keywords: CreateFromMF2DBuffer2, CreateFromMF2DBuffer2 method [Windows Runtime], CreateFromMF2DBuffer2 method [Windows Runtime],ISoftwareBitmapNativeFactory interface, ISoftwareBitmapNativeFactory interface [Windows Runtime],CreateFromMF2DBuffer2 method, ISoftwareBitmapNativeFactory.CreateFromMF2DBuffer2, ISoftwareBitmapNativeFactory.imaging, ISoftwareBitmapNativeFactory::CreateFromMF2DBuffer2, ISoftwareBitmapNativeFactory::imaging, windows/ISoftwareBitmapNativeFactory::CreateFromMF2DBuffer2, winrt.isoftwarebitmapnativefactory_createfrommf2dbuffer2
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
 - ISoftwareBitmapNativeFactory::CreateFromMF2DBuffer2
 - windows.graphics.imaging.interop/ISoftwareBitmapNativeFactory::CreateFromMF2DBuffer2
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
 - ISoftwareBitmapNativeFactory.CreateFromMF2DBuffer2
---

# ISoftwareBitmapNativeFactory::CreateFromMF2DBuffer2 (windows.graphics.imaging.interop.h)


## -description

Creates a Windows Runtime <a href="/uwp/api/windows.graphics.imaging.softwarebitmap">SoftwareBitmap</a> object from the provided <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer2">IMF2DBuffer2</a>.

## -parameters

### -param data [in]

Type: <b>IMF2DBuffer2*</b>

The source buffer containing a two-dimensional surface, such as a video frame.

### -param subtype [in]

Type: <b>REFGUID</b>

A GUID specifying the video subtype of the source buffer.

### -param width [in]

Type: <b>UINT32</b>

The width of the source surface.

### -param height [in]

Type: <b>UINT32</b>

The height of the source surface.

### -param forceReadOnly [in]

Type: <b>BOOL</b>

A value indicating whether the created software bitmap is read-only.

<div class="alert"><b>Note</b>  The read-only access applies only to the Windows Runtime <a href="/uwp/api/windows.graphics.imaging.softwarebitmap">SoftwareBitmap</a> object. Access to the underlying Media Foundation buffer is not restricted.</div>

### -param minDisplayAperture [in, optional]

Type: <b>const MFVideoArea*</b>

The rectangular area within the surface that contains valid image data. Use NULL if the full frame is valid.

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
