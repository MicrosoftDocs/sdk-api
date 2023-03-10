---
UID: NS:d3d12.D3D12_ROOT_DESCRIPTOR1
title: D3D12_ROOT_DESCRIPTOR1 (d3d12.h)
description: Describes descriptors inline in the root signature version 1.1 that appear in shaders.
helpviewer_keywords: ["D3D12_ROOT_DESCRIPTOR1","D3D12_ROOT_DESCRIPTOR1 structure","d3d12/D3D12_ROOT_DESCRIPTOR1","direct3d12.d3d12_root_descriptor1"]
old-location: direct3d12\d3d12_root_descriptor1.htm
tech.root: direct3d12
ms.assetid: 55627E99-6EED-442F-93B8-D869F0B4EAF4
ms.date: 12/05/2018
ms.keywords: D3D12_ROOT_DESCRIPTOR1, D3D12_ROOT_DESCRIPTOR1 structure, d3d12/D3D12_ROOT_DESCRIPTOR1, direct3d12.d3d12_root_descriptor1
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
req.typenames: D3D12_ROOT_DESCRIPTOR1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_ROOT_DESCRIPTOR1
 - d3d12/D3D12_ROOT_DESCRIPTOR1
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
 - D3D12_ROOT_DESCRIPTOR1
---

# D3D12_ROOT_DESCRIPTOR1 structure


## -description

Describes descriptors inline in the root signature version 1.1 that appear in shaders.

## -struct-fields

### -field ShaderRegister

The shader register.

### -field RegisterSpace

The register space.

### -field Flags

Specifies the <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags">D3D12_ROOT_DESCRIPTOR_FLAGS</a> that determine the volatility of descriptors and the data they reference.

## -remarks

<b>D3D12_ROOT_DESCRIPTOR1</b> is the data type of the <b>Descriptor</b> member of <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1">D3D12_ROOT_PARAMETER1</a>.
        Use a <b>D3D12_ROOT_DESCRIPTOR1</b> when you set <b>D3D12_ROOT_PARAMETER1</b>'s <b>ParameterType</b> field to the D3D12_ROOT_PARAMETER_TYPE_CBV, D3D12_ROOT_PARAMETER_TYPE_SRV, or D3D12_ROOT_PARAMETER_TYPE_UAV members of <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_parameter_type">D3D12_ROOT_PARAMETER_TYPE</a>.
      

Refer to the helper structure <a href="/windows/desktop/direct3d12/cd3dx12-root-descriptor1">CD3DX12_ROOT_DESCRIPTOR1</a>.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>



<a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor">D3D12_ROOT_DESCRIPTOR</a>



<a href="/windows/desktop/direct3d12/root-signature-version-1-1">Root Signature Version 1.1</a>
