---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetOutputStereoMode
title: ID3D11VideoContext::VideoProcessorSetOutputStereoMode
author: windows-sdk-content
description: Specifies whether the video processor produces stereo video frames.
old-location: mf\id3d11videocontext_videoprocessorsetoutputstereomode.htm
tech.root: medfound
ms.assetid: 86449010-6F46-460B-9972-4186FD84B407
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorSetOutputStereoMode method, ID3D11VideoContext.VideoProcessorSetOutputStereoMode, ID3D11VideoContext::VideoProcessorSetOutputStereoMode, VideoProcessorSetOutputStereoMode, VideoProcessorSetOutputStereoMode method [Media Foundation], VideoProcessorSetOutputStereoMode method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetOutputStereoMode, mf.id3d11videocontext_videoprocessorsetoutputstereomode
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
 - ID3D11VideoContext.VideoProcessorSetOutputStereoMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext::VideoProcessorSetOutputStereoMode


## -description


Specifies whether the video processor produces stereo video frames.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/5A5FB7F9-F299-4E67-AFAD-E7056CBAEE76">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param Enable

If <b>TRUE</b>, stereo output is enabled. Otherwise, the video processor produces mono video frames.


## -returns



This method does not return a value.




## -remarks



By default, the video processor produces mono video frames.

To use this feature, the driver must support stereo video, indicated by the <b>D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_STEREO</b> capability flag. To query for this capability, call <a href="https://msdn.microsoft.com/BE213FFE-FB1D-4BDC-A1AA-2EA487DF8D4A">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a>.




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

