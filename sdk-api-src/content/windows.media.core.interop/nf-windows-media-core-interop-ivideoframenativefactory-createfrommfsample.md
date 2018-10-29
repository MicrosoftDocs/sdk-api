---
UID: NF:windows.media.core.interop.IVideoFrameNativeFactory.CreateFromMFSample
title: IVideoFrameNativeFactory::core
author: windows-sdk-content
description: Creates an IVideoFrameNative from the provided IMFSample.
old-location: winrt\ivideoframenativefactory_createfrommfsample.htm
tech.root: WinRT
ms.assetid: EE925680-42A1-4C7E-A39D-15EA93F11FA1
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CreateFromMFSample, CreateFromMFSample method [Windows Runtime], CreateFromMFSample method [Windows Runtime],IVideoFrameNativeFactory interface, IVideoFrameNativeFactory interface [Windows Runtime],CreateFromMFSample method, IVideoFrameNativeFactory.CreateFromMFSample, IVideoFrameNativeFactory.core, IVideoFrameNativeFactory::CreateFromMFSample, IVideoFrameNativeFactory::core, windows/IVideoFrameNativeFactory::CreateFromMFSample, winrt.ivideoframenativefactory_createfrommfsample
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoFrameNativeFactory::core


## -description


Creates an <a href="https://msdn.microsoft.com/6B5E19EA-F66B-447C-B8D5-C98260E82789">IVideoFrameNative</a> from the provided <a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a>.


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

The IID of the <a href="https://msdn.microsoft.com/6B5E19EA-F66B-447C-B8D5-C98260E82789">IVideoFrameNative</a> interface.


### -param ppv [out]

Type: <b>LPVOID*</b>

When this method returns successfully, contains the requested interface.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns S_OK on successful completion.




## -see-also




<a href="https://msdn.microsoft.com/A884D0B5-6E12-4225-A46B-DD0C0A77B58E">IVideoFrameNativeFactory</a>
 

 

