---
UID: NE:d3d11.D3D11_VIDEO_PROCESSOR_STEREO_CAPS
title: D3D11_VIDEO_PROCESSOR_STEREO_CAPS (d3d11.h)
description: Defines stereo 3D capabilities for a Microsoft Direct3D 11 video processor.
helpviewer_keywords: ["D3D11_VIDEO_PROCESSOR_STEREO_CAPS","D3D11_VIDEO_PROCESSOR_STEREO_CAPS enumeration [Media Foundation]","D3D11_VIDEO_PROCESSOR_STEREO_CAPS_CHECKERBOARD","D3D11_VIDEO_PROCESSOR_STEREO_CAPS_COLUMN_INTERLEAVED","D3D11_VIDEO_PROCESSOR_STEREO_CAPS_FLIP_MODE","D3D11_VIDEO_PROCESSOR_STEREO_CAPS_MONO_OFFSET","D3D11_VIDEO_PROCESSOR_STEREO_CAPS_ROW_INTERLEAVED","d3d11/D3D11_VIDEO_PROCESSOR_STEREO_CAPS","d3d11/D3D11_VIDEO_PROCESSOR_STEREO_CAPS_CHECKERBOARD","d3d11/D3D11_VIDEO_PROCESSOR_STEREO_CAPS_COLUMN_INTERLEAVED","d3d11/D3D11_VIDEO_PROCESSOR_STEREO_CAPS_FLIP_MODE","d3d11/D3D11_VIDEO_PROCESSOR_STEREO_CAPS_MONO_OFFSET","d3d11/D3D11_VIDEO_PROCESSOR_STEREO_CAPS_ROW_INTERLEAVED","mf.d3d11_video_processor_stereo_caps"]
old-location: mf\d3d11_video_processor_stereo_caps.htm
tech.root: mf
ms.assetid: 352B982A-E950-4593-973E-ECDAFCF2A5F4
ms.date: 12/05/2018
ms.keywords: D3D11_VIDEO_PROCESSOR_STEREO_CAPS, D3D11_VIDEO_PROCESSOR_STEREO_CAPS enumeration [Media Foundation], D3D11_VIDEO_PROCESSOR_STEREO_CAPS_CHECKERBOARD, D3D11_VIDEO_PROCESSOR_STEREO_CAPS_COLUMN_INTERLEAVED, D3D11_VIDEO_PROCESSOR_STEREO_CAPS_FLIP_MODE, D3D11_VIDEO_PROCESSOR_STEREO_CAPS_MONO_OFFSET, D3D11_VIDEO_PROCESSOR_STEREO_CAPS_ROW_INTERLEAVED, d3d11/D3D11_VIDEO_PROCESSOR_STEREO_CAPS, d3d11/D3D11_VIDEO_PROCESSOR_STEREO_CAPS_CHECKERBOARD, d3d11/D3D11_VIDEO_PROCESSOR_STEREO_CAPS_COLUMN_INTERLEAVED, d3d11/D3D11_VIDEO_PROCESSOR_STEREO_CAPS_FLIP_MODE, d3d11/D3D11_VIDEO_PROCESSOR_STEREO_CAPS_MONO_OFFSET, d3d11/D3D11_VIDEO_PROCESSOR_STEREO_CAPS_ROW_INTERLEAVED, mf.d3d11_video_processor_stereo_caps
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
req.typenames: D3D11_VIDEO_PROCESSOR_STEREO_CAPS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_VIDEO_PROCESSOR_STEREO_CAPS
 - d3d11/D3D11_VIDEO_PROCESSOR_STEREO_CAPS
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
 - D3D11_VIDEO_PROCESSOR_STEREO_CAPS
---

# D3D11_VIDEO_PROCESSOR_STEREO_CAPS enumeration


## -description

Defines stereo 3D capabilities for a Microsoft Direct3D 11 video processor.

## -enum-fields

### -field D3D11_VIDEO_PROCESSOR_STEREO_CAPS_MONO_OFFSET:0x1

The video processor supports the <b>D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_MONO_OFFSET</b> 
 format.

### -field D3D11_VIDEO_PROCESSOR_STEREO_CAPS_ROW_INTERLEAVED:0x2

The video processor supports the <b>D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_ROW_INTERLEAVED</b> 
 format.

### -field D3D11_VIDEO_PROCESSOR_STEREO_CAPS_COLUMN_INTERLEAVED:0x4

The video processor supports the <b>D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_COLUMN_INTERLEAVED</b> 
 format.

### -field D3D11_VIDEO_PROCESSOR_STEREO_CAPS_CHECKERBOARD:0x8

The video processor supports the <b>D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_CHECKERBOARD</b> 
 format.

### -field D3D11_VIDEO_PROCESSOR_STEREO_CAPS_FLIP_MODE:0x10

The video processor can flip one or both views. For more information, see <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_stereo_flip_mode">D3D11_VIDEO_PROCESSOR_STEREO_FLIP_MODE</a>.

## -see-also

<a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_processor_caps">D3D11_VIDEO_PROCESSOR_CAPS</a>



<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_stereo_format">D3D11_VIDEO_PROCESSOR_STEREO_FORMAT</a>



<a href="/windows/desktop/medfound/direct3d-11-video-enumerations">Direct3D 11 Video Enumerations</a>
