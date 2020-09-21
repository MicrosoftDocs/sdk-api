---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetStreamFrameFormat
title: ID3D11VideoContext::VideoProcessorGetStreamFrameFormat (d3d11.h)
description: Gets the format of an input stream on the video processor.
helpviewer_keywords: ["ID3D11VideoContext interface [Media Foundation]","VideoProcessorGetStreamFrameFormat method","ID3D11VideoContext.VideoProcessorGetStreamFrameFormat","ID3D11VideoContext::VideoProcessorGetStreamFrameFormat","VideoProcessorGetStreamFrameFormat","VideoProcessorGetStreamFrameFormat method [Media Foundation]","VideoProcessorGetStreamFrameFormat method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::VideoProcessorGetStreamFrameFormat","mf.id3d11videocontext_videoprocessorgetstreamframeformat"]
old-location: mf\id3d11videocontext_videoprocessorgetstreamframeformat.htm
tech.root: mf
ms.assetid: 43879368-1730-4881-B77E-0A975DD5E473
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorGetStreamFrameFormat method, ID3D11VideoContext.VideoProcessorGetStreamFrameFormat, ID3D11VideoContext::VideoProcessorGetStreamFrameFormat, VideoProcessorGetStreamFrameFormat, VideoProcessorGetStreamFrameFormat method [Media Foundation], VideoProcessorGetStreamFrameFormat method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorGetStreamFrameFormat, mf.id3d11videocontext_videoprocessorgetstreamframeformat
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
 - ID3D11VideoContext::VideoProcessorGetStreamFrameFormat
 - d3d11/ID3D11VideoContext::VideoProcessorGetStreamFrameFormat
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
 - ID3D11VideoContext.VideoProcessorGetStreamFrameFormat
---

# ID3D11VideoContext::VideoProcessorGetStreamFrameFormat


## -description

Gets the format of an input stream on the video processor.

## -parameters

### -param pVideoProcessor [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.

### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorcaps">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.

### -param pFrameFormat [out]

Receives a <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_frame_format">D3D11_VIDEO_FRAME_FORMAT</a> value that specifies whether the stream contains interlaced or progressive frames.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>