---
UID: NE:d3d11.D3D11_VIDEO_PROCESSOR_STEREO_FLIP_MODE
title: D3D11_VIDEO_PROCESSOR_STEREO_FLIP_MODE (d3d11.h)
description: For stereo 3D video, specifies whether the data in frame 0 or frame 1 is flipped, either horizontally or vertically.
helpviewer_keywords: ["D3D11_VIDEO_PROCESSOR_STEREO_FLIP_FRAME0","D3D11_VIDEO_PROCESSOR_STEREO_FLIP_FRAME1","D3D11_VIDEO_PROCESSOR_STEREO_FLIP_MODE","D3D11_VIDEO_PROCESSOR_STEREO_FLIP_MODE enumeration [Media Foundation]","D3D11_VIDEO_PROCESSOR_STEREO_FLIP_NONE","d3d11/D3D11_VIDEO_PROCESSOR_STEREO_FLIP_FRAME0","d3d11/D3D11_VIDEO_PROCESSOR_STEREO_FLIP_FRAME1","d3d11/D3D11_VIDEO_PROCESSOR_STEREO_FLIP_MODE","d3d11/D3D11_VIDEO_PROCESSOR_STEREO_FLIP_NONE","mf.d3d11_video_processor_stereo_flip_mode"]
old-location: mf\d3d11_video_processor_stereo_flip_mode.htm
tech.root: mf
ms.assetid: 2BCC3190-BD27-465D-B9D6-346FAD5E01AF
ms.date: 12/05/2018
ms.keywords: D3D11_VIDEO_PROCESSOR_STEREO_FLIP_FRAME0, D3D11_VIDEO_PROCESSOR_STEREO_FLIP_FRAME1, D3D11_VIDEO_PROCESSOR_STEREO_FLIP_MODE, D3D11_VIDEO_PROCESSOR_STEREO_FLIP_MODE enumeration [Media Foundation], D3D11_VIDEO_PROCESSOR_STEREO_FLIP_NONE, d3d11/D3D11_VIDEO_PROCESSOR_STEREO_FLIP_FRAME0, d3d11/D3D11_VIDEO_PROCESSOR_STEREO_FLIP_FRAME1, d3d11/D3D11_VIDEO_PROCESSOR_STEREO_FLIP_MODE, d3d11/D3D11_VIDEO_PROCESSOR_STEREO_FLIP_NONE, mf.d3d11_video_processor_stereo_flip_mode
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
req.typenames: D3D11_VIDEO_PROCESSOR_STEREO_FLIP_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_VIDEO_PROCESSOR_STEREO_FLIP_MODE
 - d3d11/D3D11_VIDEO_PROCESSOR_STEREO_FLIP_MODE
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
 - D3D11_VIDEO_PROCESSOR_STEREO_FLIP_MODE
---

# D3D11_VIDEO_PROCESSOR_STEREO_FLIP_MODE enumeration


## -description

For stereo 3D video, specifies whether the data in frame 0 or frame 1 is flipped, either horizontally or vertically.

## -enum-fields

### -field D3D11_VIDEO_PROCESSOR_STEREO_FLIP_NONE:0

Neither frame is flipped.

### -field D3D11_VIDEO_PROCESSOR_STEREO_FLIP_FRAME0:1

The data in frame 0 is flipped.

### -field D3D11_VIDEO_PROCESSOR_STEREO_FLIP_FRAME1:2

The data in frame 1 is flipped.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-enumerations">Direct3D 11 Video Enumerations</a>



<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamstereoformat">ID3D11VideoContext::VideoProcessorSetStreamStereoFormat</a>
