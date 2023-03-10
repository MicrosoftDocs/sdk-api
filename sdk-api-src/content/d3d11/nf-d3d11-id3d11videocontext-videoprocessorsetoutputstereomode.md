---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetOutputStereoMode
title: ID3D11VideoContext::VideoProcessorSetOutputStereoMode (d3d11.h)
description: Specifies whether the video processor produces stereo video frames.
helpviewer_keywords: ["ID3D11VideoContext interface [Media Foundation]","VideoProcessorSetOutputStereoMode method","ID3D11VideoContext.VideoProcessorSetOutputStereoMode","ID3D11VideoContext::VideoProcessorSetOutputStereoMode","VideoProcessorSetOutputStereoMode","VideoProcessorSetOutputStereoMode method [Media Foundation]","VideoProcessorSetOutputStereoMode method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::VideoProcessorSetOutputStereoMode","mf.id3d11videocontext_videoprocessorsetoutputstereomode"]
old-location: mf\id3d11videocontext_videoprocessorsetoutputstereomode.htm
tech.root: mf
ms.assetid: 86449010-6F46-460B-9972-4186FD84B407
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorSetOutputStereoMode method, ID3D11VideoContext.VideoProcessorSetOutputStereoMode, ID3D11VideoContext::VideoProcessorSetOutputStereoMode, VideoProcessorSetOutputStereoMode, VideoProcessorSetOutputStereoMode method [Media Foundation], VideoProcessorSetOutputStereoMode method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetOutputStereoMode, mf.id3d11videocontext_videoprocessorsetoutputstereomode
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
 - ID3D11VideoContext::VideoProcessorSetOutputStereoMode
 - d3d11/ID3D11VideoContext::VideoProcessorSetOutputStereoMode
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
 - ID3D11VideoContext.VideoProcessorSetOutputStereoMode
---

# ID3D11VideoContext::VideoProcessorSetOutputStereoMode


## -description

Specifies whether the video processor produces stereo video frames.

## -parameters

### -param pVideoProcessor [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.

### -param Enable

If <b>TRUE</b>, stereo output is enabled. Otherwise, the video processor produces mono video frames.

## -remarks

By default, the video processor produces mono video frames.

To use this feature, the driver must support stereo video, indicated by the <b>D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_STEREO</b> capability flag. To query for this capability, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorcaps">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a>.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>