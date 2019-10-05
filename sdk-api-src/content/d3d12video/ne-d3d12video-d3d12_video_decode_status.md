---
UID: NE:d3d12video.D3D12_VIDEO_DECODE_STATUS
title: D3D12_VIDEO_DECODE_STATUS
author: windows-sdk-content
description: Specifes the status of a video decode operation.
tech.root: mf
ms.assetid: 4ed97807-90ca-4709-a635-004ecf8f235d
ms.author: windowssdkdev
ms.date: 05/28/2019 
ms.topic: enum
f1_keywords:
 - D3D12_VIDEO_DECODE_STATUS
dev_langs:
 - c++
ms.keywords: D3D12_VIDEO_DECODE_STATUS, D3D12_VIDEO_DECODE_STATUS, 
req.header: d3d12video.h
req.include-header:
req.redist:
req.target-type:
req.target-min-winverclnt:
req.target-min-winversvr:
req.kmdf-ver:
req.umdf-ver:
req.ddi-compliance:
req.max-support:
req.typenames: D3D12_VIDEO_DECODE_STATUS
topic_type: 
 - apiref
api_type: 
 - HeaderDef
api_location: 
 - d3d12video.h
api_name: 
 - D3D12_VIDEO_DECODE_STATUS
targetos: Windows
---

# D3D12_VIDEO_DECODE_STATUS enumeration

## -description

Specifes the status of a video decode operation. This enumeration is used in the status field of a [D3D12_VIDEO_DECODE_STATUS](ne-d3d12video-d3d12_video_decode_status) structure.


## -enum-fields

### -field D3D12_VIDEO_DECODE_STATUS_OK 

The operation succeeded.

### -field D3D12_VIDEO_DECODE_STATUS_CONTINUE 

There was a minor problem in the data format, but the host decoder should continue processing.

### -field D3D12_VIDEO_DECODE_STATUS_CONTINUE_SKIP_DISPLAY 

There was a significant problem in the data format. The host decoder should continue processing, but should skip display.

### -field D3D12_VIDEO_DECODE_STATUS_RESTART 

There was a severe problem in the data format. The host decoder should restart the entire decoding process, starting at a sequence or random-access entry point.


## -remarks

## -see-also
