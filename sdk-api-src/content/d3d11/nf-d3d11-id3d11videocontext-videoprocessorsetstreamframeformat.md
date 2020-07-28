---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetStreamFrameFormat
title: ID3D11VideoContext::VideoProcessorSetStreamFrameFormat (d3d11.h)
description: Specifies whether an input stream on the video processor contains interlaced or progressive frames.
helpviewer_keywords: ["ID3D11VideoContext interface [Media Foundation]","VideoProcessorSetStreamFrameFormat method","ID3D11VideoContext.VideoProcessorSetStreamFrameFormat","ID3D11VideoContext::VideoProcessorSetStreamFrameFormat","VideoProcessorSetStreamFrameFormat","VideoProcessorSetStreamFrameFormat method [Media Foundation]","VideoProcessorSetStreamFrameFormat method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::VideoProcessorSetStreamFrameFormat","mf.id3d11videocontext_videoprocessorsetstreamframeformat"]
old-location: mf\id3d11videocontext_videoprocessorsetstreamframeformat.htm
tech.root: mf
ms.assetid: 248BE244-23A9-4F4E-95F7-D3DB678B2D9F
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorSetStreamFrameFormat method, ID3D11VideoContext.VideoProcessorSetStreamFrameFormat, ID3D11VideoContext::VideoProcessorSetStreamFrameFormat, VideoProcessorSetStreamFrameFormat, VideoProcessorSetStreamFrameFormat method [Media Foundation], VideoProcessorSetStreamFrameFormat method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetStreamFrameFormat, mf.id3d11videocontext_videoprocessorsetstreamframeformat
f1_keywords:
- d3d11/ID3D11VideoContext.VideoProcessorSetStreamFrameFormat
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
- ID3D11VideoContext.VideoProcessorSetStreamFrameFormat
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11VideoContext::VideoProcessorSetStreamFrameFormat


## -description


Specifies whether an input stream on the video processor contains interlaced or progressive frames.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorcaps">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.


### -param FrameFormat

A <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_frame_format">D3D11_VIDEO_FRAME_FORMAT</a> value that specifies the interlacing.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>
 

 

