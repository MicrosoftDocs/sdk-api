---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_FRAME_SUBREGION_METADATA
tech.root: mf
title: D3D12_VIDEO_ENCODER_FRAME_SUBREGION_METADATA
ms.date: 07/01/2021
targetos: Windows
description: Represents video encoder frame subregion metadata.
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
req.typenames: D3D12_VIDEO_ENCODER_FRAME_SUBREGION_METADATA
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_FRAME_SUBREGION_METADATA
f1_keywords:
 - D3D12_VIDEO_ENCODER_FRAME_SUBREGION_METADATA
 - d3d12video/D3D12_VIDEO_ENCODER_FRAME_SUBREGION_METADATA
dev_langs:
 - c++
---

## -description

Represents video encoder frame subregion metadata.

## -struct-fields

### -field bSize

Output field that receives the sizes in bytes of each subregion. Subregions sizes must include both the subregion initial padding, the subregion header and the subregion payload.

### -field bStartOffset

Output field that receives the padding size in bytes that needs to be skipped at the beginning of every subregion. This padding size is included in the size reported above.

For example, let *pFrameSubregionsSizes* be an array of *bSize* for each slice. With this information, along with *pFrameSubregionsSizes*, the user can extract individual subregions from the output bitstream buffer by calculating i-th subregion start offset as `pBuffer + FrameStartOffset + sum j = (0, (i-1)){ pFrameSubregionsSizes[j] } + pFrameSubregionsStartOffsets[i]` and reading `pFrameSubregionsSizes[i]` bytes.


### -field bHeaderSize

Output parameter that receives the sizes in bits of each subregion header.
With this information, in addition to extracting the full subregion from the bitstream as explained above, the user can extract the subregions payload/headers directly without needing to parse the full subregion bitstream.

## -remarks

## -see-also

