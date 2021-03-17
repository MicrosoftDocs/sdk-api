---
UID: NS:d3d12.D3D12_ROOT_PARAMETER
title: D3D12_ROOT_PARAMETER (d3d12.h)
description: Describes the slot of a root signature version 1.0.
helpviewer_keywords: ["D3D12_ROOT_PARAMETER","D3D12_ROOT_PARAMETER structure","d3d12/D3D12_ROOT_PARAMETER","direct3d12.d3d12_root_parameter"]
old-location: direct3d12\d3d12_root_parameter.htm
tech.root: direct3d12
ms.assetid: CC1DFE85-7F83-4551-86C6-1AFDF746FC92
ms.date: 12/05/2018
ms.keywords: D3D12_ROOT_PARAMETER, D3D12_ROOT_PARAMETER structure, d3d12/D3D12_ROOT_PARAMETER, direct3d12.d3d12_root_parameter
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
req.typenames: D3D12_ROOT_PARAMETER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_ROOT_PARAMETER
 - d3d12/D3D12_ROOT_PARAMETER
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
 - D3D12_ROOT_PARAMETER
---

# D3D12_ROOT_PARAMETER structure


## -description

Describes the slot of a root signature version 1.0.

## -struct-fields

### -field ParameterType

A <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_parameter_type">D3D12_ROOT_PARAMETER_TYPE</a>-typed value that  specifies the type of root signature slot. This member determines which type to use in the union below.

### -field DescriptorTable

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table">D3D12_ROOT_DESCRIPTOR_TABLE</a> structure that describes the layout of a descriptor table as a collection of descriptor ranges that appear one after the other in a descriptor heap.

### -field Constants

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants">D3D12_ROOT_CONSTANTS</a> structure that describes constants inline in the root signature that appear in shaders as one constant buffer.

### -field Descriptor

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor">D3D12_ROOT_DESCRIPTOR</a> structure that describes descriptors inline in the root signature that appear in shaders.

### -field ShaderVisibility

A <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility">D3D12_SHADER_VISIBILITY</a>-typed value that  specifies the shaders that can access the contents of the root signature slot.

## -remarks

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc">D3D12_ROOT_SIGNATURE_DESC</a> can contain descriptor tables and inline constants. More capable hardware could support inline descriptors in the root signature as well. The number of bind slots in the root signature are most efficient if kept below a certain size, and can have an upper bound as well.

## -see-also

<a href="/windows/desktop/direct3d12/cd3dx12-root-parameter">CD3DX12_ROOT_PARAMETER</a>



<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>



<a href="/windows/desktop/direct3d12/creating-a-root-signature">Creating a Root Signature</a>



<a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1">D3D12_ROOT_PARAMETER1</a>