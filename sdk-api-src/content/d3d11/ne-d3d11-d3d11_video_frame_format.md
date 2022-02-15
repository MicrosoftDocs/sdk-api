---
UID: NE:d3d11.D3D11_VIDEO_FRAME_FORMAT
title: D3D11_VIDEO_FRAME_FORMAT (d3d11.h)
description: Describes how a video stream is interlaced.
helpviewer_keywords: ["D3D11_VIDEO_FRAME_FORMAT","D3D11_VIDEO_FRAME_FORMAT enumeration [Media Foundation]","D3D11_VIDEO_FRAME_FORMAT_INTERLACED_BOTTOM_FIELD_FIRST","D3D11_VIDEO_FRAME_FORMAT_INTERLACED_TOP_FIELD_FIRST","D3D11_VIDEO_FRAME_FORMAT_PROGRESSIVE","d3d11/D3D11_VIDEO_FRAME_FORMAT","d3d11/D3D11_VIDEO_FRAME_FORMAT_INTERLACED_BOTTOM_FIELD_FIRST","d3d11/D3D11_VIDEO_FRAME_FORMAT_INTERLACED_TOP_FIELD_FIRST","d3d11/D3D11_VIDEO_FRAME_FORMAT_PROGRESSIVE","mf.d3d11_video_frame_format"]
old-location: mf\d3d11_video_frame_format.htm
tech.root: mf
ms.assetid: D0C0C58C-8BBC-4C2C-BD0B-4244211E7E06
ms.date: 12/05/2018
ms.keywords: D3D11_VIDEO_FRAME_FORMAT, D3D11_VIDEO_FRAME_FORMAT enumeration [Media Foundation], D3D11_VIDEO_FRAME_FORMAT_INTERLACED_BOTTOM_FIELD_FIRST, D3D11_VIDEO_FRAME_FORMAT_INTERLACED_TOP_FIELD_FIRST, D3D11_VIDEO_FRAME_FORMAT_PROGRESSIVE, d3d11/D3D11_VIDEO_FRAME_FORMAT, d3d11/D3D11_VIDEO_FRAME_FORMAT_INTERLACED_BOTTOM_FIELD_FIRST, d3d11/D3D11_VIDEO_FRAME_FORMAT_INTERLACED_TOP_FIELD_FIRST, d3d11/D3D11_VIDEO_FRAME_FORMAT_PROGRESSIVE, mf.d3d11_video_frame_format
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
req.typenames: D3D11_VIDEO_FRAME_FORMAT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_VIDEO_FRAME_FORMAT
 - d3d11/D3D11_VIDEO_FRAME_FORMAT
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
 - D3D11_VIDEO_FRAME_FORMAT
---

# D3D11_VIDEO_FRAME_FORMAT enumeration


## -description

Describes how a video stream is interlaced.

## -enum-fields

### -field D3D11_VIDEO_FRAME_FORMAT_PROGRESSIVE:0

Frames are progressive.

### -field D3D11_VIDEO_FRAME_FORMAT_INTERLACED_TOP_FIELD_FIRST:1

Frames are interlaced. The top field of each frame is displayed first.

### -field D3D11_VIDEO_FRAME_FORMAT_INTERLACED_BOTTOM_FIELD_FIRST:2

Frame are interlaced. The bottom field of each frame is displayed first.

## -see-also

<a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_processor_content_desc">D3D11_VIDEO_PROCESSOR_CONTENT_DESC</a>



<a href="/windows/desktop/medfound/direct3d-11-video-enumerations">Direct3D 11 Video Enumerations</a>
