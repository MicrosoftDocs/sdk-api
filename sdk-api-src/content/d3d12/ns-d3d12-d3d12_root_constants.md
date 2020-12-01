---
UID: NS:d3d12.D3D12_ROOT_CONSTANTS
title: D3D12_ROOT_CONSTANTS (d3d12.h)
description: Describes constants inline in the root signature that appear in shaders as one constant buffer.
helpviewer_keywords: ["D3D12_ROOT_CONSTANTS","D3D12_ROOT_CONSTANTS structure","d3d12/D3D12_ROOT_CONSTANTS","direct3d12.d3d12_root_constants"]
old-location: direct3d12\d3d12_root_constants.htm
tech.root: direct3d12
ms.assetid: B6630700-4F01-4D91-A8FF-3E9CB6505F51
ms.date: 12/05/2018
ms.keywords: D3D12_ROOT_CONSTANTS, D3D12_ROOT_CONSTANTS structure, d3d12/D3D12_ROOT_CONSTANTS, direct3d12.d3d12_root_constants
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
req.typenames: D3D12_ROOT_CONSTANTS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_ROOT_CONSTANTS
 - d3d12/D3D12_ROOT_CONSTANTS
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
 - D3D12_ROOT_CONSTANTS
---

# D3D12_ROOT_CONSTANTS structure


## -description

Describes constants inline in the root signature that appear in shaders as one constant buffer.

## -struct-fields

### -field ShaderRegister

The shader register.

### -field RegisterSpace

The register space.

### -field Num32BitValues

The number of constants that occupy a single shader slot (these constants appear like a single constant buffer). 
            All constants occupy a single root signature bind slot.

## -remarks

Refer to <a href="/windows/desktop/direct3d12/resource-binding-in-hlsl">Resource Binding in HLSL</a> for more information on shader registers and spaces. 

<b>D3D12_ROOT_CONSTANTS</b> is the data type of the <b>Constants</b> member of <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter">D3D12_ROOT_PARAMETER</a>. 
        Use a <b>D3D12_ROOT_CONSTANTS</b> when you set <b>D3D12_ROOT_PARAMETER</b>'s <b>SlotType</b> field to the D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS member of <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_parameter_type">D3D12_ROOT_PARAMETER_TYPE</a>.

## -see-also

<a href="/windows/desktop/direct3d12/cd3dx12-root-constants">CD3DX12_ROOT_CONSTANTS</a>



<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>



<a href="/windows/desktop/direct3d12/creating-a-root-signature">Creating a Root Signature</a>



<a href="/windows/desktop/direct3d12/using-constants-directly-in-the-root-signature">Using constants directly in the root signature</a>