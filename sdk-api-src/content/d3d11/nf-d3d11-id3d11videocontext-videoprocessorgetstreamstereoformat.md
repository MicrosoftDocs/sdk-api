---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetStreamStereoFormat
title: ID3D11VideoContext::VideoProcessorGetStreamStereoFormat (d3d11.h)
description: Gets the stereo 3D format for an input stream on the video processor.
helpviewer_keywords: ["FALSE","ID3D11VideoContext interface [Media Foundation]","VideoProcessorGetStreamStereoFormat method","ID3D11VideoContext.VideoProcessorGetStreamStereoFormat","ID3D11VideoContext::VideoProcessorGetStreamStereoFormat","TRUE","VideoProcessorGetStreamStereoFormat","VideoProcessorGetStreamStereoFormat method [Media Foundation]","VideoProcessorGetStreamStereoFormat method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::VideoProcessorGetStreamStereoFormat","mf.id3d11videocontext_videoprocessorgetstreamstereoformat"]
old-location: mf\id3d11videocontext_videoprocessorgetstreamstereoformat.htm
tech.root: mf
ms.assetid: FCEE6C95-C631-4268-9B06-686B8AC7D80C
ms.date: 12/05/2018
ms.keywords: FALSE, ID3D11VideoContext interface [Media Foundation],VideoProcessorGetStreamStereoFormat method, ID3D11VideoContext.VideoProcessorGetStreamStereoFormat, ID3D11VideoContext::VideoProcessorGetStreamStereoFormat, TRUE, VideoProcessorGetStreamStereoFormat, VideoProcessorGetStreamStereoFormat method [Media Foundation], VideoProcessorGetStreamStereoFormat method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorGetStreamStereoFormat, mf.id3d11videocontext_videoprocessorgetstreamstereoformat
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
 - ID3D11VideoContext::VideoProcessorGetStreamStereoFormat
 - d3d11/ID3D11VideoContext::VideoProcessorGetStreamStereoFormat
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
 - ID3D11VideoContext.VideoProcessorGetStreamStereoFormat
---

# ID3D11VideoContext::VideoProcessorGetStreamStereoFormat


## -description

Gets the stereo 3D format for an input stream on the video processor

## -parameters

### -param pVideoProcessor [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.

### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorcaps">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.

### -param pEnable [out]

Receives the value <b>TRUE</b> if stereo 3D is enabled for this stream, or <b>FALSE</b> otherwise. If the value is <b>FALSE</b>, ignore the remaining parameters.

### -param pFormat [out]

Receives a <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_stereo_format">D3D11_VIDEO_PROCESSOR_STEREO_FORMAT</a> value that specifies the layout of the two stereo views in memory.

### -param pLeftViewFrame0 [out]

Receives a Boolean value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
Frame 0 contains the left view.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Frame 0 contains the right view.

</td>
</tr>
</table>

### -param pBaseViewFrame0 [out]

Receives a Boolean value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
Frame 0 contains the base view.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Frame 1 contains the base view.

</td>
</tr>
</table>

### -param pFlipMode [out]

Receives a <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_stereo_flip_mode">D3D11_VIDEO_PROCESSOR_STEREO_FLIP_MODE</a> value. This value specifies whether one of the views is flipped.

### -param MonoOffset [out]

Receives the pixel offset used for <b>D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_MONO_OFFSET</b> format. This parameter is ignored for other stereo formats.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>