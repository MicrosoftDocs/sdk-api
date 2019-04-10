---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetOutputColorSpace
title: ID3D11VideoContext::VideoProcessorGetOutputColorSpace (d3d11.h)
author: windows-sdk-content
description: Gets the current output color space for the video processor.
old-location: mf\id3d11videocontext_videoprocessorgetoutputcolorspace.htm
tech.root: medfound
ms.assetid: 26D9C908-D8A6-44F9-895F-48C52F4C8B59
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorGetOutputColorSpace method, ID3D11VideoContext.VideoProcessorGetOutputColorSpace, ID3D11VideoContext::VideoProcessorGetOutputColorSpace, VideoProcessorGetOutputColorSpace, VideoProcessorGetOutputColorSpace method [Media Foundation], VideoProcessorGetOutputColorSpace method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorGetOutputColorSpace, mf.id3d11videocontext_videoprocessorgetoutputcolorspace
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

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/5A5FB7F9-F299-4E67-AFAD-E7056CBAEE76">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param pColorSpace [out]

A pointer to a <a href="https://msdn.microsoft.com/D5F36CFC-ED36-47F3-A07A-9B163F904D74">D3D11_VIDEO_PROCESSOR_COLOR_SPACE</a> structure. The method fills in the structure with the output color space.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

