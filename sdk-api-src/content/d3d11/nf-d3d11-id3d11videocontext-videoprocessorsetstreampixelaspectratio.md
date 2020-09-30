---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetStreamPixelAspectRatio
title: ID3D11VideoContext::VideoProcessorSetStreamPixelAspectRatio (d3d11.h)
description: Sets the pixel aspect ratio for an input stream on the video processor.
helpviewer_keywords: ["ID3D11VideoContext interface [Media Foundation]","VideoProcessorSetStreamPixelAspectRatio method","ID3D11VideoContext.VideoProcessorSetStreamPixelAspectRatio","ID3D11VideoContext::VideoProcessorSetStreamPixelAspectRatio","VideoProcessorSetStreamPixelAspectRatio","VideoProcessorSetStreamPixelAspectRatio method [Media Foundation]","VideoProcessorSetStreamPixelAspectRatio method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::VideoProcessorSetStreamPixelAspectRatio","mf.id3d11videocontext_videoprocessorsetstreampixelaspectratio"]
old-location: mf\id3d11videocontext_videoprocessorsetstreampixelaspectratio.htm
tech.root: mf
ms.assetid: 4205F6F0-4AF3-42B1-8636-64FCFC865856
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorSetStreamPixelAspectRatio method, ID3D11VideoContext.VideoProcessorSetStreamPixelAspectRatio, ID3D11VideoContext::VideoProcessorSetStreamPixelAspectRatio, VideoProcessorSetStreamPixelAspectRatio, VideoProcessorSetStreamPixelAspectRatio method [Media Foundation], VideoProcessorSetStreamPixelAspectRatio method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetStreamPixelAspectRatio, mf.id3d11videocontext_videoprocessorsetstreampixelaspectratio
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
 - ID3D11VideoContext::VideoProcessorSetStreamPixelAspectRatio
 - d3d11/ID3D11VideoContext::VideoProcessorSetStreamPixelAspectRatio
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
 - ID3D11VideoContext.VideoProcessorSetStreamPixelAspectRatio
---

# ID3D11VideoContext::VideoProcessorSetStreamPixelAspectRatio


## -description

Sets the pixel aspect ratio for an input stream on the video processor.

## -parameters

### -param pVideoProcessor [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.

### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorcaps">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.

### -param Enable [in]

Specifies whether the <i>pSourceAspectRatio</i> and <i>pDestinationAspectRatio</i> parameters contain valid values. Otherwise, the pixel aspect ratios are unspecified.

### -param pSourceAspectRatio [in]

A pointer to a <a href="/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_rational">DXGI_RATIONAL</a> structure that contains the pixel aspect ratio of the source rectangle. If <i>Enable</i> is <b>FALSE</b>, this parameter can be <b>NULL</b>.

### -param pDestinationAspectRatio [in]

A pointer to a <a href="/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_rational">DXGI_RATIONAL</a> structure that contains the pixel aspect ratio of the destination rectangle. If <i>Enable</i> is <b>FALSE</b>, this parameter can be <b>NULL</b>.

## -remarks

This function can only be called if the driver reports the     <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_feature_caps">D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_PIXEL_ASPECT_RATIO</a>  capability. If this capability is not set, this function will have no effect.

Pixel aspect ratios of the form 0/n and n/0 are not valid.

The default pixel aspect ratio is 1:1 (square pixels).

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>



<a href="/windows/desktop/medfound/picture-aspect-ratio">Picture Aspect Ratio</a>