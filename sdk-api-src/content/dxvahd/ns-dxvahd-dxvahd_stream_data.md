---
UID: NS:dxvahd._DXVAHD_STREAM_DATA
title: DXVAHD_STREAM_DATA (dxvahd.h)
description: Contains per-stream data for the IDXVAHD_VideoProcessor::VideoProcessBltHD method.
helpviewer_keywords: ["DXVAHD_STREAM_DATA","DXVAHD_STREAM_DATA structure [Media Foundation]","dxvahd/DXVAHD_STREAM_DATA","mf.dxvahd_stream_data"]
old-location: mf\dxvahd_stream_data.htm
tech.root: mf
ms.assetid: 95d74c87-5884-4004-926f-108e9bbb012d
ms.date: 12/05/2018
ms.keywords: DXVAHD_STREAM_DATA, DXVAHD_STREAM_DATA structure [Media Foundation], dxvahd/DXVAHD_STREAM_DATA, mf.dxvahd_stream_data
req.header: dxvahd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: DXVAHD_STREAM_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAHD_STREAM_DATA
 - dxvahd/_DXVAHD_STREAM_DATA
 - DXVAHD_STREAM_DATA
 - dxvahd/DXVAHD_STREAM_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxvahd.h
api_name:
 - DXVAHD_STREAM_DATA
---

# DXVAHD_STREAM_DATA structure


## -description

Contains per-stream data for the <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-videoprocessblthd">IDXVAHD_VideoProcessor::VideoProcessBltHD</a> method.

## -struct-fields

### -field Enable

Specifies whether this input stream is enabled. If the value is <b>TRUE</b>, the <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-videoprocessblthd">VideoProcessBltHD</a> method blits this stream to the output surface<b></b>. Otherwise, the stream is not blitted. The maximum number of streams that can be enabled at one time is given in the <b>MaxInputStreams</b> member of the <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps">DXVAHD_VPDEVCAPS</a> structure.

### -field OutputIndex

The zero-based index number of the output frame. See Remarks.

### -field InputFrameOrField

The zero-based index number of the input frame or field. See Remarks.

### -field PastFrames

The number of past reference frames. This value must be less than or equal to the value of the <b>PastFrames</b> member of the <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps">DXVAHD_VPCAPS</a> structure.

### -field FutureFrames

The number of future reference frames. This value must be less than or equal to the value of the <b>FutureFrames</b> member of the <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps">DXVAHD_VPCAPS</a> structure.

### -field ppPastSurfaces

A pointer to an array of <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a> pointers, allocated by the caller. This array contains the past reference frames for the video processing operation. The number of elements in the array is equal to the value of the <b>PastFrames</b> member.

### -field pInputSurface

A pointer to the <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a> interface of a Microsoft Direct3D surface that contains the current input frame.

### -field ppFutureSurfaces

A pointer to an array of <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a> pointers, allocated by the caller. This array contains the future reference frames for the video processing operation. The number of elements in the array is equal to the value of the <b>FutureFrames</b> member.

## -remarks

<h3><a id="Input_Surfaces"></a><a id="input_surfaces"></a><a id="INPUT_SURFACES"></a>Input Surfaces</h3>
The Direct3D surfaces must be allocated in the memory pool specified by the <b>InputPool</b> member of the <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps">DXVAHD_VPDEVCAPS</a> structure. The following surface types can be used:


<ul>
<li>A video surface of type <b>DXVAHD_SURFACE_TYPE_VIDEO_INPUT</b> or <b>DXVAHD_SURFACE_TYPE_VIDEO_INPUT_PRIVATE</b>. See <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface">IDXVAHD_Device::CreateVideoSurface</a>.</li>
<li>A decoder render-target surface of type <b>DXVA2_VideoDecoderRenderTarget</b>. See <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface">IDirectXVideoAccelerationService::CreateSurface</a>.</li>
<li>An off-screen plain surface.</li>
</ul>
The past and future reference frames must be placed in the arrays in temporal order, from oldest to newest. For example, if <i>T</i> is the current input frame, the arrays would be ordered as follows:

<ul>
<li><b>ppPastSurfaces</b>: { …, <i>T</i>-3, <i>T</i>-2, <i>T</i>-1 }</li>
<li><b>ppInputSurface</b>: <i>T</i></li>
<li><b>ppFutureSurfaces</b>: { <i>T</i>+1, <i>T</i>+2, <i>T</i>+3, … }</li>
</ul>
The <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps">DXVAHD_VPCAPS</a> structure specifies the number of reference frames required to get the best deinterlacing quality. If the application provides fewer reference frames, the device will fall back to simpler deinterlacing algorithms. If no reference frames are provided, the device can use bob deinterlacing. Here are some cases where an application might provide fewer reference frames:

<ul>
<li>At the beginning or end of the video sequence</li>
<li>With progressive input</li>
<li>During a transition between progressive and interlaced input</li>
<li>For a substream that does not require high deinterlacing quality</li>
<li>While dropping frames</li>
</ul>
<h3><a id="Input_and_Output_Indexes"></a><a id="input_and_output_indexes"></a><a id="INPUT_AND_OUTPUT_INDEXES"></a>Input and Output Indexes</h3>
The <b>OutputIndex</b> and <b>InputFrameOrField</b> members are used to correlate input frames or fields with output frames. The value of the <b>OutputIndex</b> member is cyclic and resets to zero after each cycle.

Here are some example patterns:

<ul>
<li>Progressive video at normal rate. Each input frame produces one output frame.<ul>
<li>Output index: 0, 0, 0, 0, …</li>
<li>Input index: 0, 1, 2, 3, …</li>
</ul>
</li>
<li>Interlaced video at normal rate. Each interlaced frame (two fields) produces two output frames.<ul>
<li>Output index: 0, 1, 0, 1, …</li>
<li>Input index: 0, 1, 2, 3, …</li>
</ul>
</li>
<li>Progressive video at 2/1 output rate. Each input frame produces one output frame.<ul>
<li>Output index: 0, 1, 0, 1, …</li>
<li>Input index: 0, 1, 2, 3, …</li>
</ul>
</li>
<li>Interlaced video at 1/2 output rate. Each interlaced frame produces one output frame. (The two fields are blended to create one frame.)<ul>
<li>Output index: 0, 0, 0, 0, …</li>
<li>Input index: 0, 2, 4, 6, …</li>
</ul>
</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/medfound/direct3d-video-structures">Direct3D Video Structures</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>