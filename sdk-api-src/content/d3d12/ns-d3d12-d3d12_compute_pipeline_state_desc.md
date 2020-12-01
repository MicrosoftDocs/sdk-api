---
UID: NS:d3d12.D3D12_COMPUTE_PIPELINE_STATE_DESC
title: D3D12_COMPUTE_PIPELINE_STATE_DESC (d3d12.h)
description: Describes a compute pipeline state object.
helpviewer_keywords: ["D3D12_COMPUTE_PIPELINE_STATE_DESC","D3D12_COMPUTE_PIPELINE_STATE_DESC structure","d3d12/D3D12_COMPUTE_PIPELINE_STATE_DESC","direct3d12.d3d12_compute_pipeline_state_desc"]
old-location: direct3d12\d3d12_compute_pipeline_state_desc.htm
tech.root: direct3d12
ms.assetid: 46C785C6-8294-410F-A8D5-7E5F85FA5C75
ms.date: 12/05/2018
ms.keywords: D3D12_COMPUTE_PIPELINE_STATE_DESC, D3D12_COMPUTE_PIPELINE_STATE_DESC structure, d3d12/D3D12_COMPUTE_PIPELINE_STATE_DESC, direct3d12.d3d12_compute_pipeline_state_desc
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
req.typenames: D3D12_COMPUTE_PIPELINE_STATE_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_COMPUTE_PIPELINE_STATE_DESC
 - d3d12/D3D12_COMPUTE_PIPELINE_STATE_DESC
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
 - D3D12_COMPUTE_PIPELINE_STATE_DESC
---

# D3D12_COMPUTE_PIPELINE_STATE_DESC structure


## -description

Describes a compute pipeline state object.

## -struct-fields

### -field pRootSignature

A pointer to the <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature">ID3D12RootSignature</a> object.

### -field CS

A <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_bytecode">D3D12_SHADER_BYTECODE</a> structure that describes the compute shader.

### -field NodeMask

For single GPU operation, set this to zero. If there are multiple GPU nodes, set bits to identify the nodes (the  device's physical adapters) for which the compute pipeline state is to apply.
            Each bit in the mask corresponds to a single node.
            Refer to <a href="/windows/win32/direct3d12/multi-engine">Multi-adapter systems</a>.

### -field CachedPSO

A cached pipeline state object, as a <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state">D3D12_CACHED_PIPELINE_STATE</a> structure. pCachedBlob and CachedBlobSizeInBytes may be set to NULL and 0 respectively.

### -field Flags

A <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags">D3D12_PIPELINE_STATE_FLAGS</a> enumeration constant such as for "tool debug".

## -remarks

This structure is used by <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate">CreateComputePipelineState</a>.

## -see-also

<a href="/windows/win32/direct3d12/direct3d-12-structures">Core Structures</a>

