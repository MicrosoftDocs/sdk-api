---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetOutputBackgroundColor
title: ID3D11VideoContext::VideoProcessorSetOutputBackgroundColor (d3d11.h)
description: Sets the background color for the video processor.
helpviewer_keywords: ["ID3D11VideoContext interface [Media Foundation]","VideoProcessorSetOutputBackgroundColor method","ID3D11VideoContext.VideoProcessorSetOutputBackgroundColor","ID3D11VideoContext::VideoProcessorSetOutputBackgroundColor","VideoProcessorSetOutputBackgroundColor","VideoProcessorSetOutputBackgroundColor method [Media Foundation]","VideoProcessorSetOutputBackgroundColor method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::VideoProcessorSetOutputBackgroundColor","mf.id3d11videocontext_videoprocessorsetoutputbackgroundcolor"]
old-location: mf\id3d11videocontext_videoprocessorsetoutputbackgroundcolor.htm
tech.root: mf
ms.assetid: 6D6DAECC-8D20-4ABB-A20B-55EC4F68D8F1
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorSetOutputBackgroundColor method, ID3D11VideoContext.VideoProcessorSetOutputBackgroundColor, ID3D11VideoContext::VideoProcessorSetOutputBackgroundColor, VideoProcessorSetOutputBackgroundColor, VideoProcessorSetOutputBackgroundColor method [Media Foundation], VideoProcessorSetOutputBackgroundColor method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetOutputBackgroundColor, mf.id3d11videocontext_videoprocessorsetoutputbackgroundcolor
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11VideoContext::VideoProcessorSetOutputBackgroundColor
 - d3d11/ID3D11VideoContext::VideoProcessorSetOutputBackgroundColor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.h
api_name:
 - ID3D11VideoContext.VideoProcessorSetOutputBackgroundColor
---

# ID3D11VideoContext::VideoProcessorSetOutputBackgroundColor


## -description

Sets the background color for the video processor.

## -parameters

### -param pVideoProcessor [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.

### -param YCbCr [in]

If <b>TRUE</b>, the color is specified as a YCbCr value. Otherwise, the color is specified as an RGB value.

### -param pColor [in]

A pointer to a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_color">D3D11_VIDEO_COLOR</a> structure that specifies the background color.

## -remarks

The video processor uses the background color to fill areas of the target rectangle that do not contain a video image. Areas outside the target rectangle are not affected.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>