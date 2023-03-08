---
UID: NE:d3d12.D3D12_SHADING_RATE_COMBINER
title: D3D12_SHADING_RATE_COMBINER
description: Defines constants that specify a shading rate combiner (for variable-rate shading, or VRS).
tech.root: direct3d12
helpviewer_keywords: ["D3D12_SHADING_RATE_COMBINER"]
ms.date: 05/20/2019
ms.keywords: D3D12_SHADING_RATE_COMBINER
targetos: Windows
req.construct-type: enumeration
req.ddi-compliance: 
req.header: d3d12.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: 
req.umdf-ver: 
f1_keywords:
 - D3D12_SHADING_RATE_COMBINER
 - d3d12/D3D12_SHADING_RATE_COMBINER
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_SHADING_RATE_COMBINER
---

## -description

Defines constants that specify a shading rate combiner (for variable-rate shading, or VRS). For more info, see [Variable-rate shading (VRS)](/windows/desktop/direct3d12/vrs).

## -enum-fields

### -field D3D12_SHADING_RATE_COMBINER_PASSTHROUGH:0

Specifies the combiner `C.xy = A.xy`, for combiner (C) and inputs (A and B).

### -field D3D12_SHADING_RATE_COMBINER_OVERRIDE:1

Specifies the combiner `C.xy = B.xy`, for combiner (C) and inputs (A and B).

### -field D3D12_SHADING_RATE_COMBINER_MIN:2

Specifies the combiner `C.xy = max(A.xy, B.xy)`, for combiner (C) and inputs (A and B).

### -field D3D12_SHADING_RATE_COMBINER_MAX:3

Specifies the combiner `C.xy = min(A.xy, B.xy)`, for combiner (C) and inputs (A and B).

### -field D3D12_SHADING_RATE_COMBINER_SUM:4

Specifies the combiner C.xy = min(maxRate, A.xy + B.xy)`, for combiner (C) and inputs (A and B).

## -remarks

## -see-also

[Variable-rate shading (VRS)](/windows/desktop/direct3d12/vrs)

