---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorBlt
title: ID3D11VideoContext::VideoProcessorBlt (d3d11.h)
description: Performs a video processing operation on one or more input samples and writes the result to a Direct3D surface.
helpviewer_keywords: ["ID3D11VideoContext interface [Media Foundation]","VideoProcessorBlt method","ID3D11VideoContext.VideoProcessorBlt","ID3D11VideoContext::VideoProcessorBlt","VideoProcessorBlt","VideoProcessorBlt method [Media Foundation]","VideoProcessorBlt method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::VideoProcessorBlt","mf.id3d11videocontext_videoprocessorblt"]
old-location: mf\id3d11videocontext_videoprocessorblt.htm
tech.root: mf
ms.assetid: D526BB31-A4B9-4BBD-BAE3-43FDFF58A32A
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorBlt method, ID3D11VideoContext.VideoProcessorBlt, ID3D11VideoContext::VideoProcessorBlt, VideoProcessorBlt, VideoProcessorBlt method [Media Foundation], VideoProcessorBlt method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorBlt, mf.id3d11videocontext_videoprocessorblt
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
 - ID3D11VideoContext::VideoProcessorBlt
 - d3d11/ID3D11VideoContext::VideoProcessorBlt
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
 - ID3D11VideoContext.VideoProcessorBlt
---

## -description

Performs a video processing operation on one or more input samples, and writes the result to a Direct3D surface.

## -parameters

### -param pVideoProcessor [in]

A pointer to the <a href="/windows/win32/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call the <a href="/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a> method.

### -param pView [in]

A pointer to the <a href="/windows/win32/api/d3d11/nn-d3d11-id3d11videoprocessoroutputview">ID3D11VideoProcessorOutputView</a> interface for the output surface. The output of the video processing operation will be written to this surface.

### -param OutputFrame [in]

The frame number of the output video frame, indexed from zero.

### -param StreamCount [in]

The number of input streams to process.

### -param pStreams [in]

A pointer to an array of <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_video_processor_stream">D3D11_VIDEO_PROCESSOR_STREAM</a> structures that contain information about the input streams. The caller allocates the array and fills in each structure. The number of elements in the array is given in the *StreamCount* parameter.

## -returns

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -remarks

The maximum value of <i>StreamCount</i> is given in the <b>MaxStreamStates</b> member of the <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_video_processor_caps">D3D11_VIDEO_PROCESSOR_CAPS</a> structure. The maximum number of streams that can be enabled at one time is given in the <b>MaxInputStreams</b> member of that structure.

If the output stereo mode is <b>TRUE</b>:

<ul>
<li>The output view must contain a texture array of two elements.</li>
<li>At least one stereo stream must be specified.</li>
<li>If multiple input streams are enabled, it is possible that one or more of the input streams may contain mono data.</li>
</ul>
Otherwise:

<ul>
<li>The output view must contain a single element.</li>
<li>The stereo format cannot be <a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_video_processor_stereo_format">D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_MONO</a> .</li>
</ul>
This function does not honor a D3D11 predicate that may have been set.

If the application uses <a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_query">D3D11 queries</a>, this function may not be accounted for with <b>D3D11_QUERY_EVENT</b> and <b>D3D11_QUERY_TIMESTAMP</b> when using feature levels lower than 11. <b>D3D11_QUERY_PIPELINE_STATISTICS</b> will not include this function for any feature level.

## -see-also

[ID3D11VideoContext interface](./nn-d3d11-id3d11videocontext.md)