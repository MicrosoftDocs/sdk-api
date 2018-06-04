---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns S_OK on successful completion.




## -see-also




<a href="https://msdn.microsoft.com/A884D0B5-6E12-4225-A46B-DD0C0A77B58E">IVideoFrameNativeFactory</a>
 

 

