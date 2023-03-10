---
UID: NE:d3d12.D3D12_DESCRIPTOR_RANGE_FLAGS
title: D3D12_DESCRIPTOR_RANGE_FLAGS (d3d12.h)
description: Specifies the volatility of both descriptors and the data they reference in a Root Signature 1.1 description, which can enable some driver optimizations.
helpviewer_keywords: ["D3D12_DESCRIPTOR_RANGE_FLAGS","D3D12_DESCRIPTOR_RANGE_FLAGS enumeration","D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC","D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC_WHILE_SET_AT_EXECUTE","D3D12_DESCRIPTOR_RANGE_FLAG_DATA_VOLATILE","D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE","D3D12_DESCRIPTOR_RANGE_FLAG_NONE","d3d12/D3D12_DESCRIPTOR_RANGE_FLAGS","d3d12/D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC","d3d12/D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC_WHILE_SET_AT_EXECUTE","d3d12/D3D12_DESCRIPTOR_RANGE_FLAG_DATA_VOLATILE","d3d12/D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE","d3d12/D3D12_DESCRIPTOR_RANGE_FLAG_NONE","direct3d12.d3d12_descriptor_range_flags"]
old-location: direct3d12\d3d12_descriptor_range_flags.htm
tech.root: direct3d12
ms.assetid: B22DBE80-A0BE-40F9-ADC2-5AFB35DDDDE8
ms.date: 12/05/2018
ms.keywords: D3D12_DESCRIPTOR_RANGE_FLAGS, D3D12_DESCRIPTOR_RANGE_FLAGS enumeration, D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC, D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC_WHILE_SET_AT_EXECUTE, D3D12_DESCRIPTOR_RANGE_FLAG_DATA_VOLATILE, D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE, D3D12_DESCRIPTOR_RANGE_FLAG_NONE, d3d12/D3D12_DESCRIPTOR_RANGE_FLAGS, d3d12/D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC, d3d12/D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC_WHILE_SET_AT_EXECUTE, d3d12/D3D12_DESCRIPTOR_RANGE_FLAG_DATA_VOLATILE, d3d12/D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE, d3d12/D3D12_DESCRIPTOR_RANGE_FLAG_NONE, direct3d12.d3d12_descriptor_range_flags
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: D3D12_DESCRIPTOR_RANGE_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_DESCRIPTOR_RANGE_FLAGS
 - d3d12/D3D12_DESCRIPTOR_RANGE_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_DESCRIPTOR_RANGE_FLAGS
---

# D3D12_DESCRIPTOR_RANGE_FLAGS enumeration


## -description

Specifies the volatility of both descriptors and the data they reference in a Root Signature 1.1 description, which can enable some driver optimizations.

## -enum-fields

### -field D3D12_DESCRIPTOR_RANGE_FLAG_NONE:0

Default behavior. Descriptors are static, and default assumptions are made for data (for SRV/CBV: DATA_STATIC_WHILE_SET_AT_EXECUTE, and for UAV: DATA_VOLATILE).

### -field D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE:0x1

If this is the only flag set, then descriptors are volatile and default assumptions are made about data (for SRV/CBV: DATA_STATIC_WHILE_SET_AT_EXECUTE, and for UAV: DATA_VOLATILE). 

If this flag is combined with DATA_VOLATILE, then both descriptors and data are volatile, which is equivalent to Root Signature Version 1.0.

If this flag is combined with DATA_STATIC_WHILE_SET_AT_EXECUTE, then descriptors are volatile. This still doesn’t allow them to change during command list execution so it is valid to combine the additional declaration that data is static while set via root descriptor table during execution – the underlying descriptors are effectively static for longer than the data is being promised to be static.

### -field D3D12_DESCRIPTOR_RANGE_FLAG_DATA_VOLATILE:0x2

Descriptors are static and the data is volatile.

### -field D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC_WHILE_SET_AT_EXECUTE:0x4

Descriptors are static and data is static while set at execute.

### -field D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC:0x8

Both descriptors and data are static. This maximizes the potential for driver optimization.

### -field D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_STATIC_KEEPING_BUFFER_BOUNDS_CHECKS:0x10000

Provides the same benefits as static descriptors (see **D3D12_DESCRIPTOR_RANGE_FLAG_NONE**), except that the driver is not allowed to promote buffers to root descriptors as an optimization, because they must maintain bounds checks and root descriptors do not have those.

## -remarks

This enum is used by the  <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1">D3D12_DESCRIPTOR_RANGE1</a> structure.

To specify the volatility of just the data referenced by descriptors, refer to <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags">D3D12_ROOT_DESCRIPTOR_FLAGS</a>.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>



<a href="/windows/desktop/direct3d12/root-signature-version-1-1">Root Signature Version 1.1</a>
