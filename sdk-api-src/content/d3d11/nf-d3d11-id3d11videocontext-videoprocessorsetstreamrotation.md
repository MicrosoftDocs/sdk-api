---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetStreamRotation
title: ID3D11VideoContext::VideoProcessorSetStreamRotation (d3d11.h)
description: Sets the stream rotation for an input stream on the video processor.
helpviewer_keywords: ["ID3D11VideoContext interface [Media Foundation]","VideoProcessorSetStreamRotation method","ID3D11VideoContext.VideoProcessorSetStreamRotation","ID3D11VideoContext::VideoProcessorSetStreamRotation","VideoProcessorSetStreamRotation","VideoProcessorSetStreamRotation method [Media Foundation]","VideoProcessorSetStreamRotation method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::VideoProcessorSetStreamRotation","mf.id3d11videocontext_videoprocessorsetstreamrotation"]
old-location: mf\id3d11videocontext_videoprocessorsetstreamrotation.htm
tech.root: mf
ms.assetid: f94d283c-5eea-4248-8c06-46ef66e86b22
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorSetStreamRotation method, ID3D11VideoContext.VideoProcessorSetStreamRotation, ID3D11VideoContext::VideoProcessorSetStreamRotation, VideoProcessorSetStreamRotation, VideoProcessorSetStreamRotation method [Media Foundation], VideoProcessorSetStreamRotation method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetStreamRotation, mf.id3d11videocontext_videoprocessorsetstreamrotation
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - ID3D11VideoContext::VideoProcessorSetStreamRotation
 - d3d11/ID3D11VideoContext::VideoProcessorSetStreamRotation
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
 - ID3D11VideoContext.VideoProcessorSetStreamRotation
---

# ID3D11VideoContext::VideoProcessorSetStreamRotation


## -description

Sets the stream rotation for an input stream on the video processor.

## -parameters

### -param pVideoProcessor

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.

### -param StreamIndex

The zero-based index of the input stream. To get the maximum number of streams, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorcaps">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.

### -param Enable

Specifies if the stream is to be rotated in a clockwise orientation.

### -param Rotation

Specifies the rotation of the stream.

## -remarks

This is an optional state and the application should only use it if    <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_feature_caps">D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_ROTATION</a> is reported in  <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_processor_caps">D3D11_VIDEO_PROCESSOR_CAPS.FeatureCaps</a>.

The stream source rectangle will be specified in the pre-rotation coordinates (typically landscape) and the stream destination rectangle will be specified in the post-rotation coordinates (typically portrait).   The application must update the stream destination rectangle correctly when using a rotation value other than 0° and 180°.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>