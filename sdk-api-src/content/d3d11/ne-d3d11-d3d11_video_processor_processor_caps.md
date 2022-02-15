---
UID: NE:d3d11.D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS
title: D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS (d3d11.h)
description: Specifies video processing capabilities that relate to deinterlacing, inverse telecine (IVTC), and frame-rate conversion.
helpviewer_keywords: ["D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS","D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS enumeration [Media Foundation]","D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS_DEINTERLACE_ADAPTIVE","D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS_DEINTERLACE_BLEND","D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS_DEINTERLACE_BOB","D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS_DEINTERLACE_MOTION_COMPENSATION","D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS_FRAME_RATE_CONVERSION","D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS_INVERSE_TELECINE","d3d11/D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS","d3d11/D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS_DEINTERLACE_ADAPTIVE","d3d11/D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS_DEINTERLACE_BLEND","d3d11/D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS_DEINTERLACE_BOB","d3d11/D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS_DEINTERLACE_MOTION_COMPENSATION","d3d11/D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS_FRAME_RATE_CONVERSION","d3d11/D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS_INVERSE_TELECINE","mf.d3d11_video_processor_processor_caps"]
old-location: mf\d3d11_video_processor_processor_caps.htm
tech.root: mf
ms.assetid: 9AD4ED7B-B12E-4DFD-BB85-BC19FC6C755A
ms.date: 12/05/2018
ms.keywords: D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS, D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS enumeration [Media Foundation], D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS_DEINTERLACE_ADAPTIVE, D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS_DEINTERLACE_BLEND, D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS_DEINTERLACE_BOB, D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS_DEINTERLACE_MOTION_COMPENSATION, D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS_FRAME_RATE_CONVERSION, D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS_INVERSE_TELECINE, d3d11/D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS, d3d11/D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS_DEINTERLACE_ADAPTIVE, d3d11/D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS_DEINTERLACE_BLEND, d3d11/D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS_DEINTERLACE_BOB, d3d11/D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS_DEINTERLACE_MOTION_COMPENSATION, d3d11/D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS_FRAME_RATE_CONVERSION, d3d11/D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS_INVERSE_TELECINE, mf.d3d11_video_processor_processor_caps
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
req.typenames: D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS
 - d3d11/D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS
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
 - D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS
---

# D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS enumeration


## -description

Specifies video processing capabilities that relate to deinterlacing, inverse telecine (IVTC), and frame-rate conversion.

## -enum-fields

### -field D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS_DEINTERLACE_BLEND:0x1

The video processor can perform blend deinterlacing.



In blend deinterlacing, the two fields from an interlaced frame are blended into a single progressive frame. A video processor uses blend deinterlacing when it deinterlaces at half rate, as when converting 60i to 30p. Blend deinterlacing does not require reference frames.

### -field D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS_DEINTERLACE_BOB:0x2

The video processor can perform bob deinterlacing.

In bob deinterlacing, missing field lines are interpolated from the lines above and below. Bob deinterlacing does not require reference frames.

### -field D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS_DEINTERLACE_ADAPTIVE:0x4

The video processor can perform adaptive deinterlacing.

Adaptive deinterlacing uses spatial or temporal interpolation, and switches between the two on a field-by-field basis, depending on the amount of motion. If the video processor does not receive enough reference frames to perform adaptive deinterlacing, it falls back to bob deinterlacing.

### -field D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS_DEINTERLACE_MOTION_COMPENSATION:0x8

The video processor can perform motion-compensated deinterlacing.



Motion-compensated deinterlacing uses motion vectors to recreate missing lines. If the video processor does not receive enough reference frames to perform motion-compensated deinterlacing, it falls back to bob deinterlacing.

### -field D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS_INVERSE_TELECINE:0x10

The video processor can perform inverse telecine (IVTC).



If the video processor supports this capability, the <b>ITelecineCaps</b> member of the <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_processor_rate_conversion_caps">D3D11_VIDEO_PROCESSOR_RATE_CONVERSION_CAPS</a> structure specifies which IVTC modes are supported.

### -field D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS_FRAME_RATE_CONVERSION:0x20

The video processor can convert the frame rate by interpolating frames.

## -see-also

<a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_processor_rate_conversion_caps">D3D11_VIDEO_PROCESSOR_RATE_CONVERSION_CAPS</a>



<a href="/windows/desktop/medfound/direct3d-11-video-enumerations">Direct3D 11 Video Enumerations</a>
