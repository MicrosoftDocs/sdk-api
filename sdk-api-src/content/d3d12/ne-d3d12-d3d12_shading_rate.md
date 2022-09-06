---
UID: NE:d3d12.D3D12_SHADING_RATE
title: D3D12_SHADING_RATE
description: Defines constants that specify the shading rate (for variable-rate shading, or VRS).
tech.root: direct3d12
helpviewer_keywords: ["D3D12_SHADING_RATE"]
ms.date: 05/20/2019
ms.keywords: D3D12_SHADING_RATE
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
 - D3D12_SHADING_RATE
 - d3d12/D3D12_SHADING_RATE
dev_langs:
 - c++
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

### -field D3D12_SHADING_RATE_1X1:0

Specifies no change to the shading rate.

### -field D3D12_SHADING_RATE_1X2:0x1

Specifies that the shading rate should reduce vertical resolution 2x.

### -field D3D12_SHADING_RATE_2X1:0x4

Specifies that the shading rate should reduce horizontal resolution 2x.

### -field D3D12_SHADING_RATE_2X2:0x5

Specifies that the shading rate should reduce the resolution of both axes 2x.

### -field D3D12_SHADING_RATE_2X4:0x6

Specifies that the shading rate should reduce horizontal resolution 2x, and reduce vertical resolution 4x.

### -field D3D12_SHADING_RATE_4X2:0x9

Specifies that the shading rate should reduce horizontal resolution 4x, and reduce vertical resolution 2x.

### -field D3D12_SHADING_RATE_4X4:0xa

Specifies that the shading rate should reduce the resolution of both axes 4x.

## -remarks

## -see-also

[Variable-rate shading (VRS)](/windows/desktop/direct3d12/vrs)

