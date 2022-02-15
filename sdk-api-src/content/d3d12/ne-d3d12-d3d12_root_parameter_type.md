---
UID: NE:d3d12.D3D12_ROOT_PARAMETER_TYPE
title: D3D12_ROOT_PARAMETER_TYPE (d3d12.h)
description: Specifies the type of root signature slot.
helpviewer_keywords: ["D3D12_ROOT_PARAMETER_TYPE","D3D12_ROOT_PARAMETER_TYPE enumeration","D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS","D3D12_ROOT_PARAMETER_TYPE_CBV","D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE","D3D12_ROOT_PARAMETER_TYPE_SRV","D3D12_ROOT_PARAMETER_TYPE_UAV","d3d12/D3D12_ROOT_PARAMETER_TYPE","d3d12/D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS","d3d12/D3D12_ROOT_PARAMETER_TYPE_CBV","d3d12/D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE","d3d12/D3D12_ROOT_PARAMETER_TYPE_SRV","d3d12/D3D12_ROOT_PARAMETER_TYPE_UAV","direct3d12.d3d12_root_parameter_type"]
old-location: direct3d12\d3d12_root_parameter_type.htm
tech.root: direct3d12
ms.assetid: 1AC2D29E-3F94-4362-83B8-E9BE2175E42F
ms.date: 12/05/2018
ms.keywords: D3D12_ROOT_PARAMETER_TYPE, D3D12_ROOT_PARAMETER_TYPE enumeration, D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS, D3D12_ROOT_PARAMETER_TYPE_CBV, D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE, D3D12_ROOT_PARAMETER_TYPE_SRV, D3D12_ROOT_PARAMETER_TYPE_UAV, d3d12/D3D12_ROOT_PARAMETER_TYPE, d3d12/D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS, d3d12/D3D12_ROOT_PARAMETER_TYPE_CBV, d3d12/D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE, d3d12/D3D12_ROOT_PARAMETER_TYPE_SRV, d3d12/D3D12_ROOT_PARAMETER_TYPE_UAV, direct3d12.d3d12_root_parameter_type
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
req.typenames: D3D12_ROOT_PARAMETER_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_ROOT_PARAMETER_TYPE
 - d3d12/D3D12_ROOT_PARAMETER_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_ROOT_PARAMETER_TYPE
---

# D3D12_ROOT_PARAMETER_TYPE enumeration


## -description

Specifies the type of root signature slot.

## -enum-fields

### -field D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE:0

The slot is for a descriptor table.

### -field D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS

The slot is for root constants.

### -field D3D12_ROOT_PARAMETER_TYPE_CBV

The slot is for a constant-buffer view (CBV).

### -field D3D12_ROOT_PARAMETER_TYPE_SRV

The slot is for a shader-resource view (SRV).

### -field D3D12_ROOT_PARAMETER_TYPE_UAV

The slot is for a unordered-access view (UAV).

## -remarks

This enum is used by the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter">D3D12_ROOT_PARAMETER</a> structure.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>



<a href="/windows/desktop/direct3d12/creating-a-root-signature">Creating a Root Signature</a>
