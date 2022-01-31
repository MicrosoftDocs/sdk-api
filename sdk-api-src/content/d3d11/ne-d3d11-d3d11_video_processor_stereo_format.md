---
UID: NE:d3d11.D3D11_VIDEO_PROCESSOR_STEREO_FORMAT
title: D3D11_VIDEO_PROCESSOR_STEREO_FORMAT (d3d11.h)
description: Specifies the layout in memory of a stereo 3D video frame.
helpviewer_keywords: ["D3D11_VIDEO_PROCESSOR_STEREO_FORMAT","D3D11_VIDEO_PROCESSOR_STEREO_FORMAT enumeration [Media Foundation]","D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_CHECKERBOARD","D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_COLUMN_INTERLEAVED","D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_HORIZONTAL","D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_MONO","D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_MONO_OFFSET","D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_ROW_INTERLEAVED","D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_SEPARATE","D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_VERTICAL","d3d11/D3D11_VIDEO_PROCESSOR_STEREO_FORMAT","d3d11/D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_CHECKERBOARD","d3d11/D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_COLUMN_INTERLEAVED","d3d11/D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_HORIZONTAL","d3d11/D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_MONO","d3d11/D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_MONO_OFFSET","d3d11/D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_ROW_INTERLEAVED","d3d11/D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_SEPARATE","d3d11/D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_VERTICAL","mf.d3d11_video_processor_stereo_format"]
old-location: mf\d3d11_video_processor_stereo_format.htm
tech.root: mf
ms.assetid: 77832DF2-821E-465C-80B6-46DDB2433791
ms.date: 12/05/2018
ms.keywords: D3D11_VIDEO_PROCESSOR_STEREO_FORMAT, D3D11_VIDEO_PROCESSOR_STEREO_FORMAT enumeration [Media Foundation], D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_CHECKERBOARD, D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_COLUMN_INTERLEAVED, D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_HORIZONTAL, D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_MONO, D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_MONO_OFFSET, D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_ROW_INTERLEAVED, D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_SEPARATE, D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_VERTICAL, d3d11/D3D11_VIDEO_PROCESSOR_STEREO_FORMAT, d3d11/D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_CHECKERBOARD, d3d11/D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_COLUMN_INTERLEAVED, d3d11/D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_HORIZONTAL, d3d11/D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_MONO, d3d11/D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_MONO_OFFSET, d3d11/D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_ROW_INTERLEAVED, d3d11/D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_SEPARATE, d3d11/D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_VERTICAL, mf.d3d11_video_processor_stereo_format
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
req.typenames: D3D11_VIDEO_PROCESSOR_STEREO_FORMAT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_VIDEO_PROCESSOR_STEREO_FORMAT
 - d3d11/D3D11_VIDEO_PROCESSOR_STEREO_FORMAT
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
 - D3D11_VIDEO_PROCESSOR_STEREO_FORMAT
---

# D3D11_VIDEO_PROCESSOR_STEREO_FORMAT enumeration


## -description

Specifies the layout in memory of a stereo 3D video frame.

## -enum-fields

### -field D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_MONO:0

The sample does not contain stereo data.  If the stereo format is not specified, this value is the default.

### -field D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_HORIZONTAL:1

Frame 0 and frame 1 are packed side-by-side, as shown in the following diagram.

<img alt="Side-by-side packing" src="./images/dxgistereo3d02.png"/>

All drivers that support stereo video must support this format.

### -field D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_VERTICAL:2

Frame 0 and frame 1 are packed top-to-bottom, as shown in the following diagram.

<img alt="Top-to-bottom packing" src="./images/dxgistereo3d01.png"/>

All drivers that support stereo video must support this format.

### -field D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_SEPARATE:3

Frame 0 and frame 1 are placed in separate resources or in separate texture array elements within the same resource.

All drivers that support stereo video must support this format.

### -field D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_MONO_OFFSET:4

The sample contains non-stereo data. However, the driver should create a left/right output of this sample using a specified offset.  The offset is specified in the <i>MonoOffset</i> parameter of the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamstereoformat">ID3D11VideoContext::VideoProcessorSetStreamStereoFormat</a> method. 

This format is primarily intended for subtitles and other subpicture data, where the entire sample is presented on the same plane.

Support for this stereo format is optional.

### -field D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_ROW_INTERLEAVED:5

Frame 0 and frame 1 are packed into interleaved rows, as shown in the following diagram.

<img alt="Interleaved rows" src="./images/dxgistereo3d03.png"/>

Support for this stereo format is optional.

### -field D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_COLUMN_INTERLEAVED:6

Frame 0 and frame 1 are packed into interleaved columns, as shown in the following diagram.

<img alt="Interleaved columns" src="./images/dxgistereo3d04.png"/>

Support for this stereo format is optional.

### -field D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_CHECKERBOARD:7

Frame 0 and frame 1 are packed in a checkerboard format, as shown in the following diagram.

<img alt="Checkerboard packing" src="./images/dxgistereo3d05.png"/>

Support for this stereo format is optional.

## -remarks

This enumeration designates the two stereo views as "frame 0" and "frame 1". The <i>LeftViewFrame0</i> parameter of the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamstereoformat">VideoProcessorSetStreamStereoFormat</a> method specifies which view is the left view, and which is the right view.

For packed formats, if the source rectangle clips part of the surface, the driver interprets the rectangle in logical coordinates relative to the stereo view,  rather than absolute pixel coordinates. The result is that frame 0 and frame 1 are clipped proportionately.

To query whether the device supports stereo 3D video, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorcaps">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check for the <b>D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_STEREO</b> flag in the <b>FeatureCaps</b> member of the <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_processor_caps">D3D11_VIDEO_PROCESSOR_CAPS</a> structure. If this capability flag is present, it means that the driver supports all of the stereo formats that are not  listed as optional. To find out which optional formats are supported, call <b>GetVideoProcessorCaps</b> and check the <b>StereoCaps</b> member of the structure.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-enumerations">Direct3D 11 Video Enumerations</a>



<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamstereoformat">ID3D11VideoContext::VideoProcessorSetStreamStereoFormat</a>
