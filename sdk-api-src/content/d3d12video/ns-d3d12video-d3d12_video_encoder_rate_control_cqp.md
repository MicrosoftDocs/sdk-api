---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_RATE_CONTROL_CQP
tech.root: mf
title: D3D12_VIDEO_ENCODER_RATE_CONTROL_CQP
ms.date: 06/15/2021
targetos: Windows
description: Represents a rate control structure definition for constant quantization parameter mode.
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
req.typenames: D3D12_VIDEO_ENCODER_RATE_CONTROL_CQP
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_RATE_CONTROL_CQP
f1_keywords:
 - D3D12_VIDEO_ENCODER_RATE_CONTROL_CQP
 - d3d12video/D3D12_VIDEO_ENCODER_RATE_CONTROL_CQP
dev_langs:
 - c++
---

## -description

Represents a rate control structure definition for constant quantization parameter mode.

## -struct-fields

### -field ConstantQP_FullIntracodedFrame

A UINT64 specifying the quantization parameter that should be used for each fully intra-encoded frame.

### -field ConstantQP_InterPredictedFrame_PrevRefOnly

A UINT64 specifying the quantization parameter that should be used for each encoded frame that has inter-picture references to pictures (in display order) before the current one.

### -field ConstantQP_InterPredictedFrame_BiDirectionalRef

A UINT64 specifying the quantization parameter that should be used for each encoded frame that has inter-picture references to pictures (in display order) both from previous and next frames.

## -remarks




## -see-also

