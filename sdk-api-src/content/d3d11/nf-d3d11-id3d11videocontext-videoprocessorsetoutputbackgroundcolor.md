---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetOutputBackgroundColor
title: ID3D11VideoContext::VideoProcessorSetOutputBackgroundColor
author: windows-sdk-content
description: Sets the background color for the video processor.
old-location: mf\id3d11videocontext_videoprocessorsetoutputbackgroundcolor.htm
tech.root: MedFound
ms.assetid: 6D6DAECC-8D20-4ABB-A20B-55EC4F68D8F1
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorSetOutputBackgroundColor method, ID3D11VideoContext.VideoProcessorSetOutputBackgroundColor, ID3D11VideoContext::VideoProcessorSetOutputBackgroundColor, VideoProcessorSetOutputBackgroundColor, VideoProcessorSetOutputBackgroundColor method [Media Foundation], VideoProcessorSetOutputBackgroundColor method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetOutputBackgroundColor, mf.id3d11videocontext_videoprocessorsetoutputbackgroundcolor
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
 - ID3D11VideoContext.VideoProcessorSetOutputBackgroundColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext::VideoProcessorSetOutputBackgroundColor


## -description


Sets the background color for the video processor.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/5A5FB7F9-F299-4E67-AFAD-E7056CBAEE76">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param YCbCr [in]

If <b>TRUE</b>, the color is specified as a YCbCr value. Otherwise, the color is specified as an RGB value.


### -param pColor [in]

A pointer to a <a href="https://msdn.microsoft.com/F8E070EE-F8F6-4AAF-9A8A-6D0AF6B857B5">D3D11_VIDEO_COLOR</a> structure that specifies the background color.


## -returns



This method does not return a value.




## -remarks



The video processor uses the background color to fill areas of the target rectangle that do not contain a video image. Areas outside the target rectangle are not affected.




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

