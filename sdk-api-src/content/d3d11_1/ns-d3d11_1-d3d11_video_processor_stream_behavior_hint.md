---
UID: NS:d3d11_1.D3D11_VIDEO_PROCESSOR_STREAM_BEHAVIOR_HINT
title: D3D11_VIDEO_PROCESSOR_STREAM_BEHAVIOR_HINT (d3d11_1.h)
description: Provides information about the input streams passed into the ID3DVideoContext1::VideoProcessorGetBehaviorHints method.
helpviewer_keywords: ["D3D11_VIDEO_PROCESSOR_STREAM_BEHAVIOR_HINT","D3D11_VIDEO_PROCESSOR_STREAM_BEHAVIOR_HINT structure [Media Foundation]","d3d11_1/D3D11_VIDEO_PROCESSOR_STREAM_BEHAVIOR_HINT","mf.d3d11_video_processor_stream_behavior_hint"]
old-location: mf\d3d11_video_processor_stream_behavior_hint.htm
tech.root: mf
ms.assetid: 0B90AB2C-3F62-49FF-A1DB-FCB07A33F482
ms.date: 12/05/2018
ms.keywords: D3D11_VIDEO_PROCESSOR_STREAM_BEHAVIOR_HINT, D3D11_VIDEO_PROCESSOR_STREAM_BEHAVIOR_HINT structure [Media Foundation], d3d11_1/D3D11_VIDEO_PROCESSOR_STREAM_BEHAVIOR_HINT, mf.d3d11_video_processor_stream_behavior_hint
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: D3D11_VIDEO_PROCESSOR_STREAM_BEHAVIOR_HINT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_VIDEO_PROCESSOR_STREAM_BEHAVIOR_HINT
 - d3d11_1/D3D11_VIDEO_PROCESSOR_STREAM_BEHAVIOR_HINT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11_1.h
api_name:
 - D3D11_VIDEO_PROCESSOR_STREAM_BEHAVIOR_HINT
---

# D3D11_VIDEO_PROCESSOR_STREAM_BEHAVIOR_HINT structure


## -description

Provides information about the input streams passed into the <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorgetbehaviorhints">ID3DVideoContext1::VideoProcessorGetBehaviorHints</a> method.

## -struct-fields

### -field Enable

A value indicating whether this input stream should be used to compute behavior hints. Set to true if the stream should be used to compute behavior hints; otherwise, set to false.

### -field Width

The width of the input stream.

### -field Height

The height of the input stream.

### -field Format

The format of the input stream.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-structures">Direct3D 11 Video Structures</a>