---
UID: NE:d3d12video.D3D12_VIDEO_ENCODER_MOVEREGION_INFO_FLAGS
tech.root: mf
title: D3D12_VIDEO_ENCODER_MOVEREGION_INFO_FLAGS
ms.date: 04/07/2026
targetos: Windows
description: Specifies flags for move region info in video encoding.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: d3d12video.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_MOVEREGION_INFO_FLAGS
f1_keywords:
 - D3D12_VIDEO_ENCODER_MOVEREGION_INFO_FLAGS
 - d3d12video/D3D12_VIDEO_ENCODER_MOVEREGION_INFO_FLAGS
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_VIDEO_ENCODER_MOVEREGION_INFO_FLAGS
---

## -description

Specifies flags for move region info in video encoding.

## -enum-fields

### -field D3D12_VIDEO_ENCODER_MOVEREGION_INFO_FLAG_NONE : 0x0

No flags.

### -field D3D12_VIDEO_ENCODER_MOVEREGION_INFO_FLAG_MULTIPLE_HINTS : 0x1

Indicates that pMoveRegions contains overlapped rects, producing multiple hints for positions where the overlap occurs. Check support with D3D12_VIDEO_ENCODER_MOTION_SEARCH_SUPPORT_FLAG_MULTIPLE_HINTS before using this flag.

## -remarks

## -see-also
