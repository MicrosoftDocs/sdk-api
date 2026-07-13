---
UID: NE:d3d12.D3D12_ROOT_DESCRIPTOR_FLAGS
title: D3D12_ROOT_DESCRIPTOR_FLAGS (d3d12.h)
description: Specifies the volatility of the data referenced by descriptors in a Root Signature 1.1 description, which can enable some driver optimizations.
helpviewer_keywords: ["D3D12_ROOT_DESCRIPTOR_FLAGS","D3D12_ROOT_DESCRIPTOR_FLAGS enumeration","D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC","D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC_WHILE_SET_AT_EXECUTE","D3D12_ROOT_DESCRIPTOR_FLAG_DATA_VOLATILE","D3D12_ROOT_DESCRIPTOR_FLAG_NONE","d3d12/D3D12_ROOT_DESCRIPTOR_FLAGS","d3d12/D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC","d3d12/D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC_WHILE_SET_AT_EXECUTE","d3d12/D3D12_ROOT_DESCRIPTOR_FLAG_DATA_VOLATILE","d3d12/D3D12_ROOT_DESCRIPTOR_FLAG_NONE","direct3d12.d3d12_root_descriptor_flags"]
old-location: direct3d12\d3d12_root_descriptor_flags.htm
tech.root: direct3d12
ms.assetid: 1BF4D1FA-C938-4704-8D82-CFCA6FE954CB
ms.date: 12/05/2018
ms.keywords: D3D12_ROOT_DESCRIPTOR_FLAGS, D3D12_ROOT_DESCRIPTOR_FLAGS enumeration, D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC, D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC_WHILE_SET_AT_EXECUTE, D3D12_ROOT_DESCRIPTOR_FLAG_DATA_VOLATILE, D3D12_ROOT_DESCRIPTOR_FLAG_NONE, d3d12/D3D12_ROOT_DESCRIPTOR_FLAGS, d3d12/D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC, d3d12/D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC_WHILE_SET_AT_EXECUTE, d3d12/D3D12_ROOT_DESCRIPTOR_FLAG_DATA_VOLATILE, d3d12/D3D12_ROOT_DESCRIPTOR_FLAG_NONE, direct3d12.d3d12_root_descriptor_flags
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
req.typenames: D3D12_ROOT_DESCRIPTOR_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_ROOT_DESCRIPTOR_FLAGS
 - d3d12/D3D12_ROOT_DESCRIPTOR_FLAGS
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
 - D3D12_ROOT_DESCRIPTOR_FLAGS
---

# D3D12_ROOT_DESCRIPTOR_FLAGS enumeration


## -description

Specifies the volatility of the data referenced by descriptors in a Root Signature 1.1 description, which can enable some driver optimizations.

## -enum-fields

### -field D3D12_ROOT_DESCRIPTOR_FLAG_NONE:0

Default assumptions are made for data (for SRV/CBV: DATA_STATIC_WHILE_SET_AT_EXECUTE, and for UAV: DATA_VOLATILE).

### -field D3D12_ROOT_DESCRIPTOR_FLAG_DATA_VOLATILE:0x2

Data is volatile. Equivalent to Root Signature Version 1.0.

### -field D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC_WHILE_SET_AT_EXECUTE:0x4

Data is static while set at execute.

### -field D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC:0x8

Data is static. The best potential for driver optimization.

## -remarks

This enum is used by the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1">D3D12_ROOT_DESCRIPTOR1</a> structure.

To specify the volatility of both descriptors and data, refer to <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags">D3D12_DESCRIPTOR_RANGE_FLAGS</a>.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>



<a href="/windows/desktop/direct3d12/root-signature-version-1-1">Root Signature Version 1.1</a>
