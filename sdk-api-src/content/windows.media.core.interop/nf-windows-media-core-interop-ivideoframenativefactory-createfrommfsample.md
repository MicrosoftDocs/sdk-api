---
UID: NF:windows.media.core.interop.IVideoFrameNativeFactory.CreateFromMFSample
title: IVideoFrameNativeFactory::core (windows.media.core.interop.h)
author: windows-sdk-content
description: Creates an IVideoFrameNative from the provided IMFSample.
old-location: winrt\ivideoframenativefactory_createfrommfsample.htm
tech.root: WinRT
ms.assetid: EE925680-42A1-4C7E-A39D-15EA93F11FA1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateFromMFSample, CreateFromMFSample method [Windows Runtime], CreateFromMFSample method [Windows Runtime],IVideoFrameNativeFactory interface, IVideoFrameNativeFactory interface [Windows Runtime],CreateFromMFSample method, IVideoFrameNativeFactory.CreateFromMFSample, IVideoFrameNativeFactory.core, IVideoFrameNativeFactory::CreateFromMFSample, IVideoFrameNativeFactory::core, windows/IVideoFrameNativeFactory::CreateFromMFSample, winrt.ivideoframenativefactory_createfrommfsample
ms.topic: method
f1_keywords: 
 - "windows.media.core.interop/IVideoFrameNativeFactory.CreateFromMFSample"
dev_langs:
 - c++
req.header: windows.media.core.interop.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - windows.media.core.interop.h
api_name:
 - IVideoFrameNativeFactory.CreateFromMFSample
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVideoFrameNativeFactory::core


## -description


Creates an <a href="https://docs.microsoft.com/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative">IVideoFrameNative</a> from the provided <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a>.


## -parameters




### -param data [in]

Type: <b>IMFSample*</b>

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


### -param minDisplayAperture [in, optional]

Type: <b>const MFVideoArea*</b>

The rectangular area within the surface that contains valid image data. Use NULL if the full frame is valid.


### -param device [in, optional]

Type: <b>IMFDXGIDeviceManager*</b>

Pointer to the device associated with the image data.


### -param riid [in]

Type: <b>REFIID</b>

The IID of the <a href="https://docs.microsoft.com/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative">IVideoFrameNative</a> interface.


### -param ppv [out]

Type: <b>LPVOID*</b>

When this method returns successfully, contains the requested interface.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK on successful completion.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenativefactory">IVideoFrameNativeFactory</a>
 

 

