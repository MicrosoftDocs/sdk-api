---
UID: NF:mfobjects.IMFVideoMediaType.GetVideoFormat
title: IMFVideoMediaType::GetVideoFormat
author: windows-sdk-content
description: GetVideoFormat is no longer available for use as of Windows 7.
old-location: mf\imfvideomediatype_getvideoformat.htm
tech.root: medfound
ms.assetid: 2168c76e-2b83-40ad-8ac1-9b76f1a31b7b
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: 2168c76e-2b83-40ad-8ac1-9b76f1a31b7b, GetVideoFormat, GetVideoFormat method [Media Foundation], GetVideoFormat method [Media Foundation],IMFVideoMediaType interface, IMFVideoMediaType interface [Media Foundation],GetVideoFormat method, IMFVideoMediaType.GetVideoFormat, IMFVideoMediaType::GetVideoFormat, mf.imfvideomediatype_getvideoformat, mfobjects/IMFVideoMediaType::GetVideoFormat
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFVideoMediaType.GetVideoFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFVideoMediaType::GetVideoFormat


## -description


<p class="CCE_Message">[<b>GetVideoFormat</b> is no longer available for use as of Windows 7. Instead, use the media type attributes to get the properties of the video format.]

Returns a pointer to an <a href="https://msdn.microsoft.com/7fbc4a35-117c-4f0c-9e9b-ff44e30a1618">MFVIDEOFORMAT</a> structure that describes the video format.


## -parameters






## -returns



This method returns a pointer to an <a href="https://msdn.microsoft.com/7fbc4a35-117c-4f0c-9e9b-ff44e30a1618">MFVIDEOFORMAT</a> structure.
          




## -remarks



If you need to convert the media type into an <a href="https://msdn.microsoft.com/7fbc4a35-117c-4f0c-9e9b-ff44e30a1618">MFVIDEOFORMAT</a> structure, call <a href="https://msdn.microsoft.com/c83e3605-d345-4192-a6fd-26d1a78eb259">MFCreateMFVideoFormatFromMFMediaType</a>.

There are no guarantees about how long the returned pointer is valid.




## -see-also




<a href="https://msdn.microsoft.com/9109b0dd-c44d-41d4-9480-1ca5c667dbd7">IMFVideoMediaType</a>



<a href="https://msdn.microsoft.com/690fda6e-dcbd-44dc-968d-cc949126da81">Media Types</a>
 

 

