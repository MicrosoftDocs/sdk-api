---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_ENCODE_OPERATION_METADATA_BUFFER
tech.root: mf
title: D3D12_VIDEO_ENCODER_ENCODE_OPERATION_METADATA_BUFFER
ms.date: 07/02/2021
targetos: Windows
description: Represents a buffer containing metadata about an ID3D12VideoEncodeCommandList2::EncodeFrame operation.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: d3d12video.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.typenames: D3D12_VIDEO_ENCODER_ENCODE_OPERATION_METADATA_BUFFER
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_ENCODE_OPERATION_METADATA_BUFFER
f1_keywords:
 - D3D12_VIDEO_ENCODER_ENCODE_OPERATION_METADATA_BUFFER
 - d3d12video/D3D12_VIDEO_ENCODER_ENCODE_OPERATION_METADATA_BUFFER
dev_langs:
 - c++
---

## -description

Represents a buffer containing metadata about an [ID3D12VideoEncodeCommandList2::EncodeFrame](nf-d3d12video-id3d12videoencodecommandlist2-encodeframe.md) operation.

## -struct-fields

### -field pBuffer

A pointer to an [ID3D12Resource](..//d3d12/nn-d3d12-id3d12resource.md) representing the metadata buffer.

### -field Offset

The offset into the associated buffer.

## -remarks

## -see-also

