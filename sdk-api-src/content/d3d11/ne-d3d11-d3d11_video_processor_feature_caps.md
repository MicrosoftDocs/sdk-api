---
UID: NE:d3d11.D3D11_VIDEO_PROCESSOR_FEATURE_CAPS
title: D3D11_VIDEO_PROCESSOR_FEATURE_CAPS (d3d11.h)
description: Defines features that a Microsoft Direct3D 11 video processor can support.
helpviewer_keywords: ["D3D11_VIDEO_PROCESSOR_FEATURE_CAPS","D3D11_VIDEO_PROCESSOR_FEATURE_CAPS enumeration [Media Foundation]","D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_ALPHA_FILL","D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_ALPHA_PALETTE","D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_ALPHA_STREAM","D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_CONSTRICTION","D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_LEGACY","D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_LUMA_KEY","D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_PIXEL_ASPECT_RATIO","D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_ROTATION","D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_STEREO","d3d11/D3D11_VIDEO_PROCESSOR_FEATURE_CAPS","d3d11/D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_ALPHA_FILL","d3d11/D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_ALPHA_PALETTE","d3d11/D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_ALPHA_STREAM","d3d11/D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_CONSTRICTION","d3d11/D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_LEGACY","d3d11/D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_LUMA_KEY","d3d11/D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_PIXEL_ASPECT_RATIO","d3d11/D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_ROTATION","d3d11/D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_STEREO","mf.d3d11_video_processor_feature_caps"]
old-location: mf\d3d11_video_processor_feature_caps.htm
tech.root: mf
ms.assetid: A40E33D4-E8F3-4348-9135-DD56BABBFA85
ms.date: 12/05/2018
ms.keywords: D3D11_VIDEO_PROCESSOR_FEATURE_CAPS, D3D11_VIDEO_PROCESSOR_FEATURE_CAPS enumeration [Media Foundation], D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_ALPHA_FILL, D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_ALPHA_PALETTE, D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_ALPHA_STREAM, D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_CONSTRICTION, D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_LEGACY, D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_LUMA_KEY, D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_PIXEL_ASPECT_RATIO, D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_ROTATION, D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_STEREO, d3d11/D3D11_VIDEO_PROCESSOR_FEATURE_CAPS, d3d11/D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_ALPHA_FILL, d3d11/D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_ALPHA_PALETTE, d3d11/D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_ALPHA_STREAM, d3d11/D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_CONSTRICTION, d3d11/D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_LEGACY, d3d11/D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_LUMA_KEY, d3d11/D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_PIXEL_ASPECT_RATIO, d3d11/D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_ROTATION, d3d11/D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_STEREO, mf.d3d11_video_processor_feature_caps
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
req.typenames: D3D11_VIDEO_PROCESSOR_FEATURE_CAPS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_VIDEO_PROCESSOR_FEATURE_CAPS
 - d3d11/D3D11_VIDEO_PROCESSOR_FEATURE_CAPS
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
 - D3D11_VIDEO_PROCESSOR_FEATURE_CAPS
---

# D3D11_VIDEO_PROCESSOR_FEATURE_CAPS enumeration


## -description

Defines features that a Microsoft Direct3D 11 video processor can support.

## -enum-fields

### -field D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_ALPHA_FILL:0x1

The video processor can set alpha values on the output pixels. For more information, see <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputalphafillmode">ID3D11VideoContext::VideoProcessorSetOutputAlphaFillMode</a>.

### -field D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_CONSTRICTION:0x2

The video processor can downsample the video output. For more information, see <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputconstriction">ID3D11VideoContext::VideoProcessorSetOutputConstriction</a>.

### -field D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_LUMA_KEY:0x4

The video processor can perform luma keying. For more information, see <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamlumakey">ID3D11VideoContext::VideoProcessorSetStreamLumaKey</a>.

### -field D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_ALPHA_PALETTE:0x8

The video processor can apply alpha values from color palette entries.

### -field D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_LEGACY:0x10

The driver does not support full video processing capabilities. If this capability flag is set, the video processor has the following limitations:

<ul>
<li>A maximum of two streams are supported:<ul>
<li>The first stream must be either NV12 or YUY2.</li>
<li>The second stream must be AYUV, AI44, or IA44.</li>
</ul>
</li>
<li>Image adjustment (proc amp) controls are applied to the entire video processing blit, rather than per stream.</li>
<li>Support for per-stream planar alpha is not reliable. (Per-pixel alpha is supported, however.)</li>
</ul>

### -field D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_STEREO:0x20

The video processor can support 3D stereo video. For more information, see <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamstereoformat">ID3D11VideoContext::VideoProcessorSetStreamStereoFormat</a>.

All drivers setting this caps must support the following stereo formats: <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_stereo_format">D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_HORIZONTAL</a>, <b>D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_VERTICAL</b>, and <b>D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_SEPARATE</b>.

### -field D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_ROTATION:0x40

The driver can rotate the input data either 90, 180, or 270 degrees clockwise as part of the video processing operation.

### -field D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_ALPHA_STREAM:0x80

The driver supports the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamalpha">VideoProcessorSetStreamAlpha</a> call.

### -field D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_PIXEL_ASPECT_RATIO:0x100

The driver supports the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreampixelaspectratio">VideoProcessorSetStreamPixelAspectRatio</a> call.

### -field D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_MIRROR:0x200

### -field D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_SHADER_USAGE:0x400

### -field D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_METADATA_HDR10:0x800

## -see-also

<a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_processor_caps">D3D11_VIDEO_PROCESSOR_CAPS</a>



<a href="/windows/desktop/medfound/direct3d-11-video-enumerations">Direct3D 11 Video Enumerations</a>
