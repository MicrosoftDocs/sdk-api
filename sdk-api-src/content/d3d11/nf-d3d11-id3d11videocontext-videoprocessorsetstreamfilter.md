---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetStreamFilter
title: ID3D11VideoContext::VideoProcessorSetStreamFilter (d3d11.h)
description: Enables or disables an image filter for an input stream on the video processor.
helpviewer_keywords: ["ID3D11VideoContext interface [Media Foundation]","VideoProcessorSetStreamFilter method","ID3D11VideoContext.VideoProcessorSetStreamFilter","ID3D11VideoContext::VideoProcessorSetStreamFilter","VideoProcessorSetStreamFilter","VideoProcessorSetStreamFilter method [Media Foundation]","VideoProcessorSetStreamFilter method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::VideoProcessorSetStreamFilter","mf.id3d11videocontext_videoprocessorsetstreamfilter"]
old-location: mf\id3d11videocontext_videoprocessorsetstreamfilter.htm
tech.root: mf
ms.assetid: 49258E8F-50BC-4F51-A492-78B44A73CC13
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorSetStreamFilter method, ID3D11VideoContext.VideoProcessorSetStreamFilter, ID3D11VideoContext::VideoProcessorSetStreamFilter, VideoProcessorSetStreamFilter, VideoProcessorSetStreamFilter method [Media Foundation], VideoProcessorSetStreamFilter method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetStreamFilter, mf.id3d11videocontext_videoprocessorsetstreamfilter
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
 - ID3D11VideoContext::VideoProcessorSetStreamFilter
 - d3d11/ID3D11VideoContext::VideoProcessorSetStreamFilter
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
 - ID3D11VideoContext.VideoProcessorSetStreamFilter
---

# ID3D11VideoContext::VideoProcessorSetStreamFilter


## -description

Enables or disables an image filter for an input stream on the video processor.

## -parameters

### -param pVideoProcessor [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.

### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorcaps">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.

### -param Filter [in]

The filter, specified as a <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_filter">D3D11_VIDEO_PROCESSOR_FILTER</a> value.

To query which filters the driver supports, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorcaps">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a>.

### -param Enable [in]

Specifies whether to enable the filter.

### -param Level [in]

The filter level. If <i>Enable</i> is <b>FALSE</b>, this parameter is ignored. 

To find the valid range of levels for a specified filter, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorfilterrange">ID3D11VideoProcessorEnumerator::GetVideoProcessorFilterRange</a>.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>