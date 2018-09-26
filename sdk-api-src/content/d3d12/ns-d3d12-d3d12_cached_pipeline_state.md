---
UID: NS:d3d12.D3D12_CACHED_PIPELINE_STATE
title: D3D12_CACHED_PIPELINE_STATE
author: windows-sdk-content
description: Stores a pipeline state.
old-location: direct3d12\d3d12_cached_pipeline_state.htm
tech.root: direct3d12
ms.assetid: 82A0CF70-7A16-45D5-A717-0BBB35DCC5A6
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: D3D12_CACHED_PIPELINE_STATE, D3D12_CACHED_PIPELINE_STATE structure, d3d12/D3D12_CACHED_PIPELINE_STATE, direct3d12.d3d12_cached_pipeline_state
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_CACHED_PIPELINE_STATE
product: Windows
targetos: Windows
req.typenames: D3D12_CACHED_PIPELINE_STATE
req.redist: 
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



This structure is used by the <a href="https://msdn.microsoft.com/35D10150-A633-4D38-B684-3E2DF357FFC0">D3D12_GRAPHICS_PIPELINE_STATE_DESC</a>structure, and the <a href="https://msdn.microsoft.com/46C785C6-8294-410F-A8D5-7E5F85FA5C75">D3D12_COMPUTE_PIPELINE_STATE_DESC</a> structure.

This structure is intended to be filled with the data retrieved from <a href="https://msdn.microsoft.com/318FCFEE-74A7-4546-989E-9AF674D2B853">ID3D12PipelineState::GetCachedBlob</a>. This cached PSO contains data specific to the hardware, driver, and machine that it was retrieved from. Compilation using this data should be faster than compilation without. The rest of the data in the PSO needs to still be valid, and needs to match the cached PSO, otherwise E_INVALIDARG might be returned.

If the driver has been upgraded to a D3D12 driver after the PSO was cached, you might see a D3D12_ERROR_DRIVER_VERSION_MISMATCH return code, or if you’re running on a different GPU, the D3D12_ERROR_ADAPTER_NOT_FOUND return code.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

