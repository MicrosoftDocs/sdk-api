---
UID: NS:d3d12.D3D12_CACHED_PIPELINE_STATE
title: D3D12_CACHED_PIPELINE_STATE (d3d12.h)
description: Stores a pipeline state.
helpviewer_keywords: ["D3D12_CACHED_PIPELINE_STATE","D3D12_CACHED_PIPELINE_STATE structure","d3d12/D3D12_CACHED_PIPELINE_STATE","direct3d12.d3d12_cached_pipeline_state"]
old-location: direct3d12\d3d12_cached_pipeline_state.htm
tech.root: direct3d12
ms.assetid: 82A0CF70-7A16-45D5-A717-0BBB35DCC5A6
ms.date: 12/05/2018
ms.keywords: D3D12_CACHED_PIPELINE_STATE, D3D12_CACHED_PIPELINE_STATE structure, d3d12/D3D12_CACHED_PIPELINE_STATE, direct3d12.d3d12_cached_pipeline_state
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
req.typenames: D3D12_CACHED_PIPELINE_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_CACHED_PIPELINE_STATE
 - d3d12/D3D12_CACHED_PIPELINE_STATE
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
 - D3D12_CACHED_PIPELINE_STATE
---

# D3D12_CACHED_PIPELINE_STATE structure


## -description

Stores a pipeline state.

## -struct-fields

### -field pCachedBlob

Specifies pointer that references the memory location of the cache.

### -field CachedBlobSizeInBytes

Specifies the size of the cache in bytes.

## -remarks

This structure is used by the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc">D3D12_GRAPHICS_PIPELINE_STATE_DESC</a> structure, and the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc">D3D12_COMPUTE_PIPELINE_STATE_DESC</a> structure.

This structure is intended to be filled with the data retrieved from <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12pipelinestate-getcachedblob">ID3D12PipelineState::GetCachedBlob</a>. This cached PSO contains data specific to the hardware, driver, and machine that it was retrieved from. Compilation using this data should be faster than compilation without. The rest of the data in the PSO needs to still be valid, and needs to match the cached PSO, otherwise E_INVALIDARG might be returned.

If the driver has been upgraded to a D3D12 driver after the PSO was cached, you might see a D3D12_ERROR_DRIVER_VERSION_MISMATCH return code, or if you’re running on a different GPU, the D3D12_ERROR_ADAPTER_NOT_FOUND return code.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>