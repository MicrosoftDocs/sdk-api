---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetStreamStereoFormat
title: ID3D11VideoContext::VideoProcessorSetStreamStereoFormat (d3d11.h)
description: Enables or disables stereo 3D video for an input stream on the video processor.
helpviewer_keywords: ["ID3D11VideoContext interface [Media Foundation]","VideoProcessorSetStreamStereoFormat method","ID3D11VideoContext.VideoProcessorSetStreamStereoFormat","ID3D11VideoContext::VideoProcessorSetStreamStereoFormat","VideoProcessorSetStreamStereoFormat","VideoProcessorSetStreamStereoFormat method [Media Foundation]","VideoProcessorSetStreamStereoFormat method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::VideoProcessorSetStreamStereoFormat","mf.id3d11videocontext_videoprocessorsetstreamstereoformat"]
old-location: mf\id3d11videocontext_videoprocessorsetstreamstereoformat.htm
tech.root: mf
ms.assetid: FAAE902A-622E-42D2-B332-CD4126A4182E
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorSetStreamStereoFormat method, ID3D11VideoContext.VideoProcessorSetStreamStereoFormat, ID3D11VideoContext::VideoProcessorSetStreamStereoFormat, VideoProcessorSetStreamStereoFormat, VideoProcessorSetStreamStereoFormat method [Media Foundation], VideoProcessorSetStreamStereoFormat method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetStreamStereoFormat, mf.id3d11videocontext_videoprocessorsetstreamstereoformat
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
 - ID3D11VideoContext::VideoProcessorSetStreamStereoFormat
 - d3d11/ID3D11VideoContext::VideoProcessorSetStreamStereoFormat
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
 - ID3D11VideoContext.VideoProcessorSetStreamStereoFormat
---

# ID3D11VideoContext::VideoProcessorSetStreamStereoFormat


## -description

Enables or disables stereo 3D video for an input stream on the video processor. In addition, this method specifies the layout of the video frames in memory.

## -parameters

### -param pVideoProcessor [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.

### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorcaps">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.

### -param Enable [in]

Specifies whether stereo 3D is enabled for this stream. If the value is <b>FALSE</b>, the remaining parameters of this method are ignored.

### -param Format [in]

Specifies the layout of the two stereo views in memory, as a <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_stereo_format">D3D11_VIDEO_PROCESSOR_STEREO_FORMAT</a> value.

### -param LeftViewFrame0 [in]

If <b>TRUE</b>, frame 0 contains the left view. Otherwise, frame 0 contains the right view. 

This parameter is ignored for the following stereo formats:

<ul>
<li><b>D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_MONO </b></li>
<li><b>D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_MONO_OFFSET</b></li>
</ul>

### -param BaseViewFrame0 [in]

If <b>TRUE</b>, frame 0 contains the base view. Otherwise, frame 1 contains the base view.

This parameter is ignored for the following stereo formats:

<ul>
<li><b>D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_MONO </b></li>
<li><b>D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_MONO_OFFSET</b></li>
<li>When <b>D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_SEPARATE</b> is used and the application wants to convert the stereo data to mono, it can either:<ul>
<li>Specify the base view as a mono input.</li>
<li>Specify both resources and allow the driver to do the conversion from the base view.  In this case, <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_processor_stream">D3D11_VIDEO_PROCESSOR_STREAM.hInputSurface</a> is considered frame 0 and <b>D3D11_VIDEO_PROCESSOR_STREAM.hInputSurfaceRight</b> is considered frame 1.</li>
</ul>
</li>
</ul>

### -param FlipMode [in]

A flag from the  <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_stereo_flip_mode">D3D11_VIDEO_PROCESSOR_STEREO_FLIP_MODE</a> enumeration, specifying whether one of the views is flipped.

### -param MonoOffset [in]

For <b>D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_MONO_OFFSET</b> format, this parameter specifies how to generate the left and right views:  

<ul>
<li>If <i>MonoOffset</i> is positive, the right view is shifted to the right by that many pixels, and the left view is shifted to the left by the same amount. </li>
<li>If <i>MonoOffset</i> is negative, the right view is shifted to the left by that many pixels, and the left view is shifted to right by the same amount.</li>
</ul>
If <i>Format</i> is not <b>D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_MONO_OFFSET</b>, this parameter must be zero.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>