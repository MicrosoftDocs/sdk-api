---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetOutputColorSpace
title: ID3D11VideoContext::VideoProcessorGetOutputColorSpace
author: windows-sdk-content
description: Gets the current output color space for the video processor.
old-location: mf\id3d11videocontext_videoprocessorgetoutputcolorspace.htm
tech.root: medfound
ms.assetid: 26D9C908-D8A6-44F9-895F-48C52F4C8B59
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorGetOutputColorSpace method, ID3D11VideoContext.VideoProcessorGetOutputColorSpace, ID3D11VideoContext::VideoProcessorGetOutputColorSpace, VideoProcessorGetOutputColorSpace, VideoProcessorGetOutputColorSpace method [Media Foundation], VideoProcessorGetOutputColorSpace method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorGetOutputColorSpace, mf.id3d11videocontext_videoprocessorgetoutputcolorspace
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - d3d11.h
api_name:
 - ID3D11VideoContext.VideoProcessorGetOutputColorSpace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext::VideoProcessorGetOutputColorSpace


## -description


Gets the current output color space for the video processor.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/en-us/library/Hh447799(v=VS.85).aspx">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/en-us/library/Hh447788(v=VS.85).aspx">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param pColorSpace [out]

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Hh447651(v=VS.85).aspx">D3D11_VIDEO_PROCESSOR_COLOR_SPACE</a> structure. The method fills in the structure with the output color space.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh447703(v=VS.85).aspx">ID3D11VideoContext</a>
 

 

