---
UID: NE:d3d12.D3D12_SHADING_RATE
title: D3D12_SHADING_RATE
description: Defines constants that specify the shading rate (for variable-rate shading, or VRS).
ms.date: 05/20/2019
ms.keywords: D3D12_SHADING_RATE
ms.topic: language-reference
f1_keywords: ["d3d12/D3D12_SHADING_RATE"]
targetos: Windows
product: Windows
req.construct-type: enumeration
req.ddi-compliance: 
req.header: d3d12.h
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
 - d3d12.h
api_name:
 - D3D12_SHADING_RATE
---

## -description

Defines constants that specify the shading rate (for variable-rate shading, or VRS). For more info, see [Variable-rate shading (VRS)](/windows/desktop/direct3d12/vrs).

## -enum-fields

### -field D3D12_SHADING_RATE_1X1

Specifies no change to the shading rate.

### -field D3D12_SHADING_RATE_1X2

Specifies that the shading rate should reduce vertical resolution 2x.

### -field D3D12_SHADING_RATE_2X1

Specifies that the shading rate should reduce horizontal resolution 2x.

### -field D3D12_SHADING_RATE_2X2

Specifies that the shading rate should reduce the resolution of both axes 2x.

### -field D3D12_SHADING_RATE_2X4

Specifies that the shading rate should reduce horizontal resolution 2x, and reduce vertical resolution 4x.

### -field D3D12_SHADING_RATE_4X2

Specifies that the shading rate should reduce horizontal resolution 4x, and reduce vertical resolution 2x.

### -field D3D12_SHADING_RATE_4X4

Specifies that the shading rate should reduce the resolution of both axes 4x.

## -remarks

## -see-also

[Variable-rate shading (VRS)](/windows/desktop/direct3d12/vrs)
