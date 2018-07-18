---
UID: NF:windows.graphics.imaging.interop.ISoftwareBitmapNativeFactory.CreateFromMF2DBuffer2
title: ISoftwareBitmapNativeFactory::imaging
author: windows-sdk-content
description: Creates an ISoftwareBitmapNative from the provided IMF2DBuffer2.
old-location: winrt\isoftwarebitmapnativefactory_createfrommf2dbuffer2.htm
old-project: WinRT
ms.assetid: F6B9E8B2-19CF-4921-9E9E-E387084E5F8B
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: CreateFromMF2DBuffer2, CreateFromMF2DBuffer2 method [Windows Runtime], CreateFromMF2DBuffer2 method [Windows Runtime],ISoftwareBitmapNativeFactory interface, ISoftwareBitmapNativeFactory interface [Windows Runtime],CreateFromMF2DBuffer2 method, ISoftwareBitmapNativeFactory.CreateFromMF2DBuffer2, ISoftwareBitmapNativeFactory.imaging, ISoftwareBitmapNativeFactory::CreateFromMF2DBuffer2, ISoftwareBitmapNativeFactory::imaging, windows/ISoftwareBitmapNativeFactory::CreateFromMF2DBuffer2, winrt.isoftwarebitmapnativefactory_createfrommf2dbuffer2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: PDF_RENDER_PARAMS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - windows.graphics.imaging.interop.dll
api_name:
 - ISoftwareBitmapNativeFactory.CreateFromMF2DBuffer2
product: Windows
targetos: Windows
req.lib: Windows.graphics.imaging.interop.lib
req.dll: Windows.graphics.imaging.interop.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISoftwareBitmapNativeFactory::imaging


## -description


Creates an <a href="https://msdn.microsoft.com/9EB9C74E-A056-4A40-AFAD-0056E139BA28">ISoftwareBitmapNative</a>  from the provided <a href="https://msdn.microsoft.com/BFA73B1A-F8A7-4100-9DBD-234CCA06F9F5">IMF2DBuffer2</a>.


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

<div class="alert"><b>Note</b>  The read-only access applies only to the Windows Runtime<a href="https://msdn.microsoft.com/cf4130af-344e-454e-ab61-a8238db94a06">SoftwareBitmap</a> wrapper. Access to the underlying Media Foundation buffer is not restricted.</div>
<div> </div>

### -param minDisplayAperture [in, optional]

Type: <b>const MFVideoArea*</b>

The rectangular area within the surface that contains valid image data. Use NULL if the full frame is valid.


### -param riid [in]

Type: <b>REFIID</b>

The IID of the <a href="https://msdn.microsoft.com/9EB9C74E-A056-4A40-AFAD-0056E139BA28">ISoftwareBitmapNative</a> interface.


### -param ppv [out]

Type: <b>LPVOID*</b>

When this method returns successfully, contains the requested interface.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns S_OK on successful completion.




## -see-also




<a href="https://msdn.microsoft.com/613BFE81-AC55-4786-B6BD-0FFB7506D7F1">ISoftwareBitmapNativeFactory</a>
 

 

