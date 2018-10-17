---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetOutputBackgroundColor
title: ID3D11VideoContext::VideoProcessorGetOutputBackgroundColor
author: windows-sdk-content
description: Gets the current background color for the video processor.
old-location: mf\id3d11videocontext_videoprocessorgetoutputbackgroundcolor.htm
tech.root: medfound
ms.assetid: B22666BC-EADF-4812-B299-1EA45F1943C4
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorGetOutputBackgroundColor method, ID3D11VideoContext.VideoProcessorGetOutputBackgroundColor, ID3D11VideoContext::VideoProcessorGetOutputBackgroundColor, VideoProcessorGetOutputBackgroundColor, VideoProcessorGetOutputBackgroundColor method [Media Foundation], VideoProcessorGetOutputBackgroundColor method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorGetOutputBackgroundColor, mf.id3d11videocontext_videoprocessorgetoutputbackgroundcolor
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
 - ID3D11VideoContext.VideoProcessorGetOutputBackgroundColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext::VideoProcessorGetOutputBackgroundColor


## -description


Gets the current background color for the video processor.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/5A5FB7F9-F299-4E67-AFAD-E7056CBAEE76">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param pYCbCr [out]

Receives the value <b>TRUE</b> if the background color is a YCbCr color, or <b>FALSE</b> if the background color is an RGB color.


### -param pColor [out]

A pointer to a <a href="https://msdn.microsoft.com/F8E070EE-F8F6-4AAF-9A8A-6D0AF6B857B5">D3D11_VIDEO_COLOR</a> structure. The method fills in the structure with the background color.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

