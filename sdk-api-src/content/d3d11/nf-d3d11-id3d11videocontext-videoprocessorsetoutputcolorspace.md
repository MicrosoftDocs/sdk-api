---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetOutputColorSpace
title: ID3D11VideoContext::VideoProcessorSetOutputColorSpace (d3d11.h)
description: Sets the output color space for the video processor.
old-location: mf\id3d11videocontext_videoprocessorsetoutputcolorspace.htm
tech.root: medfound
ms.assetid: 5B4B2C26-CFC8-43BD-A889-8838DEF3582A
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorSetOutputColorSpace method, ID3D11VideoContext.VideoProcessorSetOutputColorSpace, ID3D11VideoContext::VideoProcessorSetOutputColorSpace, VideoProcessorSetOutputColorSpace, VideoProcessorSetOutputColorSpace method [Media Foundation], VideoProcessorSetOutputColorSpace method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetOutputColorSpace, mf.id3d11videocontext_videoprocessorsetoutputcolorspace
f1_keywords:
- d3d11/ID3D11VideoContext.VideoProcessorSetOutputColorSpace
dev_langs:
- c++
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
- ID3D11VideoContext.VideoProcessorSetOutputColorSpace
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11VideoContext::VideoProcessorSetOutputColorSpace


## -description


Sets the output color space for the video processor.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param pColorSpace [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_processor_color_space">D3D11_VIDEO_PROCESSOR_COLOR_SPACE</a> structure that specifies the color space.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>
 

 

