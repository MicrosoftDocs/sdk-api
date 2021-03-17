---
UID: NS:d3d11.D3D11_VIDEO_PROCESSOR_CONTENT_DESC
title: D3D11_VIDEO_PROCESSOR_CONTENT_DESC (d3d11.h)
description: Describes a video stream for a video processor.
helpviewer_keywords: ["D3D11_VIDEO_PROCESSOR_CONTENT_DESC","D3D11_VIDEO_PROCESSOR_CONTENT_DESC structure [Media Foundation]","d3d11/D3D11_VIDEO_PROCESSOR_CONTENT_DESC","mf.d3d11_video_processor_content_desc"]
old-location: mf\d3d11_video_processor_content_desc.htm
tech.root: mf
ms.assetid: A1649897-B368-4D03-9A08-630C8C59E44A
ms.date: 12/05/2018
ms.keywords: D3D11_VIDEO_PROCESSOR_CONTENT_DESC, D3D11_VIDEO_PROCESSOR_CONTENT_DESC structure [Media Foundation], d3d11/D3D11_VIDEO_PROCESSOR_CONTENT_DESC, mf.d3d11_video_processor_content_desc
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
req.typenames: D3D11_VIDEO_PROCESSOR_CONTENT_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_VIDEO_PROCESSOR_CONTENT_DESC
 - d3d11/D3D11_VIDEO_PROCESSOR_CONTENT_DESC
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
 - D3D11_VIDEO_PROCESSOR_CONTENT_DESC
---

# D3D11_VIDEO_PROCESSOR_CONTENT_DESC structure


## -description

Describes a video stream for a video processor.

## -struct-fields

### -field InputFrameFormat

A member of the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_frame_format">D3D11_VIDEO_FRAME_FORMAT</a> enumeration that describes how the video stream is interlaced.

### -field InputFrameRate

The frame rate of the input video stream, specified as a <a href="/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_rational">DXGI_RATIONAL</a> structure.

### -field InputWidth

The width of the input frames, in pixels.

### -field InputHeight

The height of the input frames, in pixels.

### -field OutputFrameRate

The frame rate of the output video stream, specified as a <a href="/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_rational">DXGI_RATIONAL</a> structure.

### -field OutputWidth

The width of the output frames, in pixels.

### -field OutputHeight

The height of the output frames, in pixels.

### -field Usage

A member of the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_usage">D3D11_VIDEO_USAGE</a> enumeration that describes how the video processor will be used. The value indicates the desired trade-off between speed and video quality. The driver uses this flag as a hint when it creates the video processor.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-structures">Direct3D 11 Video Structures</a>



<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessorenumerator">ID3D11VideoDevice::CreateVideoProcessorEnumerator</a>