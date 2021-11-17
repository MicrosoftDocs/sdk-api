---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_OUTPUT_METADATA_STATISTICS
tech.root: mf
title: D3D12_VIDEO_ENCODER_OUTPUT_METADATA_STATISTICS
ms.date: 07/01/2021
targetos: Windows
description: Represents encoding statistics about a ID3D12VideoEncodeCommandList2::EncodeFrame operation.
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
req.typenames: D3D12_VIDEO_ENCODER_OUTPUT_METADATA_STATISTICS
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_OUTPUT_METADATA_STATISTICS
f1_keywords:
 - D3D12_VIDEO_ENCODER_OUTPUT_METADATA_STATISTICS
 - d3d12video/D3D12_VIDEO_ENCODER_OUTPUT_METADATA_STATISTICS
dev_langs:
 - c++
---

## -description

Represents encoding statistics about an [ID3D12VideoEncodeCommandList2::EncodeFrame](nf-d3d12video-id3d12videoencodecommandlist2-encodeframe.md) operation.

## -struct-fields

### -field AverageQP

Output field that receives the average QP value used for encoding this frame.

### -field IntraCodingUnitsCount

Output field that receives the number of intra-coded coding units used in this frame.

### -field InterCodingUnitsCount

Output field that receives the number of inter-coded coding units used in this frame.

### -field SkipCodingUnitsCount

Output field that receives the number of skip coding units used in this frame.

### -field AverageMotionEstimationXDirection

Output field that receives the average motion vector shift in X direction.

### -field AverageMotionEstimationYDirection

Output field that receives the average motion vector shift in Y direction.

## -remarks

## -see-also

