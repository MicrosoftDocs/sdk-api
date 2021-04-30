---
UID: NS:d3d12.D3D12_ROOT_PARAMETER1
title: D3D12_ROOT_PARAMETER1 (d3d12.h)
description: Describes the slot of a root signature version 1.1.
helpviewer_keywords: ["D3D12_ROOT_PARAMETER1","D3D12_ROOT_PARAMETER1 structure","d3d12/D3D12_ROOT_PARAMETER1","direct3d12.d3d12_root_parameter1"]
old-location: direct3d12\d3d12_root_parameter1.htm
tech.root: direct3d12
ms.assetid: 615B8ABF-FD80-4254-976B-9E587CE9F12E
ms.date: 12/05/2018
ms.keywords: D3D12_ROOT_PARAMETER1, D3D12_ROOT_PARAMETER1 structure, d3d12/D3D12_ROOT_PARAMETER1, direct3d12.d3d12_root_parameter1
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
req.typenames: D3D12_ROOT_PARAMETER1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_ROOT_PARAMETER1
 - d3d12/D3D12_ROOT_PARAMETER1
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
 - D3D12_ROOT_PARAMETER1
---

# D3D12_ROOT_PARAMETER1 structure


## -description

Describes the slot of a root signature version 1.1.

## -struct-fields

### -field ParameterType

A <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_parameter_type">D3D12_ROOT_PARAMETER_TYPE</a>-typed value that  specifies the type of root signature slot. This member determines which type to use in the union below.

### -field DescriptorTable

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1">D3D12_ROOT_DESCRIPTOR_TABLE1</a> structure that describes the layout of a descriptor table as a collection of descriptor ranges that appear one after the other in a descriptor heap.

### -field Constants

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants">D3D12_ROOT_CONSTANTS</a> structure that describes constants inline in the root signature that appear in shaders as one constant buffer.

### -field Descriptor

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1">D3D12_ROOT_DESCRIPTOR1</a> structure that describes descriptors inline in the root signature that appear in shaders.

### -field ShaderVisibility

A <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility">D3D12_SHADER_VISIBILITY</a>-typed value that  specifies the shaders that can access the contents of the root signature slot.

## -remarks

Use this structure with the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1">D3D12_ROOT_SIGNATURE_DESC1</a> structure.

Refer to the helper structure <a href="/windows/desktop/direct3d12/cd3dx12-root-parameter1">CD3DX12_ROOT_PARAMETER1</a>.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>



<a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter">D3D12_ROOT_PARAMETER</a>



<a href="/windows/desktop/direct3d12/root-signature-version-1-1">Root Signature Version 1.1</a>