---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetOutputBackgroundColor
title: ID3D11VideoContext::VideoProcessorGetOutputBackgroundColor (d3d11.h)
description: Gets the current background color for the video processor.
helpviewer_keywords: ["ID3D11VideoContext interface [Media Foundation]","VideoProcessorGetOutputBackgroundColor method","ID3D11VideoContext.VideoProcessorGetOutputBackgroundColor","ID3D11VideoContext::VideoProcessorGetOutputBackgroundColor","VideoProcessorGetOutputBackgroundColor","VideoProcessorGetOutputBackgroundColor method [Media Foundation]","VideoProcessorGetOutputBackgroundColor method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::VideoProcessorGetOutputBackgroundColor","mf.id3d11videocontext_videoprocessorgetoutputbackgroundcolor"]
old-location: mf\id3d11videocontext_videoprocessorgetoutputbackgroundcolor.htm
tech.root: mf
ms.assetid: B22666BC-EADF-4812-B299-1EA45F1943C4
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorGetOutputBackgroundColor method, ID3D11VideoContext.VideoProcessorGetOutputBackgroundColor, ID3D11VideoContext::VideoProcessorGetOutputBackgroundColor, VideoProcessorGetOutputBackgroundColor, VideoProcessorGetOutputBackgroundColor method [Media Foundation], VideoProcessorGetOutputBackgroundColor method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorGetOutputBackgroundColor, mf.id3d11videocontext_videoprocessorgetoutputbackgroundcolor
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
 - ID3D11VideoContext::VideoProcessorGetOutputBackgroundColor
 - d3d11/ID3D11VideoContext::VideoProcessorGetOutputBackgroundColor
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
 - ID3D11VideoContext.VideoProcessorGetOutputBackgroundColor
---

# ID3D11VideoContext::VideoProcessorGetOutputBackgroundColor


## -description

Gets the current background color for the video processor.

## -parameters

### -param pVideoProcessor [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.

### -param pYCbCr [out]

Receives the value <b>TRUE</b> if the background color is a YCbCr color, or <b>FALSE</b> if the background color is an RGB color.

### -param pColor [out]

A pointer to a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_color">D3D11_VIDEO_COLOR</a> structure. The method fills in the structure with the background color.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>