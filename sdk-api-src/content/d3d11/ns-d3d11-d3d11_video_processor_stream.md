---
UID: NS:d3d11.D3D11_VIDEO_PROCESSOR_STREAM
title: D3D11_VIDEO_PROCESSOR_STREAM (d3d11.h)
description: Contains stream-level data for the ID3D11VideoContext::VideoProcessorBlt method.
helpviewer_keywords: ["D3D11_VIDEO_PROCESSOR_STREAM","D3D11_VIDEO_PROCESSOR_STREAM structure [Media Foundation]","d3d11/D3D11_VIDEO_PROCESSOR_STREAM","mf.d3d11_video_processor_stream"]
old-location: mf\d3d11_video_processor_stream.htm
tech.root: mf
ms.assetid: B861D00B-2FF2-4F8F-AD40-0EE6A9706A0C
ms.date: 12/05/2018
ms.keywords: D3D11_VIDEO_PROCESSOR_STREAM, D3D11_VIDEO_PROCESSOR_STREAM structure [Media Foundation], d3d11/D3D11_VIDEO_PROCESSOR_STREAM, mf.d3d11_video_processor_stream
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
req.typenames: D3D11_VIDEO_PROCESSOR_STREAM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_VIDEO_PROCESSOR_STREAM
 - d3d11/D3D11_VIDEO_PROCESSOR_STREAM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_VIDEO_PROCESSOR_STREAM
---

# D3D11_VIDEO_PROCESSOR_STREAM structure


## -description

Contains stream-level data for the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorblt">ID3D11VideoContext::VideoProcessorBlt</a> method.

## -struct-fields

### -field Enable

Specifies whether this input stream is enabled. If the value is <b>TRUE</b>, the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorblt">VideoProcessorBlt</a> method blits this stream to the output surface. Otherwise, this stream is not blitted. 

The maximum number of streams that can be enabled at one time is given in the <b>MaxInputStreams</b> member of the <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_processor_caps">D3D11_VIDEO_PROCESSOR_CAPS</a> structure.

### -field OutputIndex

The zero-based index number of the output frame.

### -field InputFrameOrField

The zero-based index number of the input frame or field.

### -field PastFrames

The number of past reference frames.

### -field FutureFrames

The number of future reference frames.

### -field ppPastSurfaces

A pointer to an array of <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessorinputview">ID3D11VideoProcessorInputView</a> pointers, allocated by the caller. This array contains the past reference frames for the video processing operation. The number of elements in the array is equal to <b>PastFrames</b>.

### -field pInputSurface

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessorinputview">ID3D11VideoProcessorInputView</a> interface of the surface that contains the current input frame.

### -field ppFutureSurfaces

A pointer to an array of <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessorinputview">ID3D11VideoProcessorInputView</a> pointers, allocated by the caller. This array contains the future reference frames for the video processing operation. The number of elements in the array is equal to <b>FutureFrames</b>.

### -field ppPastSurfacesRight

If the stereo 3D format is <b>D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_SEPARATE</b>, this member points to an array that contains the past reference frames for the right view. The number of elements in the array is equal to <b>PastFrames</b>.

For any other stereo 3D format, set this member to <b>NULL</b>. For more information, see <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamstereoformat">ID3D11VideoContext::VideoProcessorSetStreamStereoFormat</a>.

### -field pInputSurfaceRight

If the stereo 3D format is <b>D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_SEPARATE</b>, this member contains a pointer to the current input frame for the right view. 

For any other stereo 3D format, set this member to <b>NULL</b>.

### -field ppFutureSurfacesRight

If the stereo 3D format is <b>D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_SEPARATE</b>, this member points to an array that contains the future reference frames for the right view. The number of elements in the array is equal to <b>FutureFrames</b>.

For any other stereo 3D format, set this member to <b>NULL</b>.

## -remarks

If the stereo 3D format is <b>D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_SEPARATE</b>, the <b>ppPastSurfaces</b>, <b>pInputSurface</b>, and <b>ppFutureSurfaces</b> members contain the left view.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-structures">Direct3D 11 Video Structures</a>



<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorblt">ID3D11VideoContext::VideoProcessorBlt</a>