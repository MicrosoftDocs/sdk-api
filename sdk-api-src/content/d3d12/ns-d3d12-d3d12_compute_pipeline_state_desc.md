---
UID: NS:d3d12.D3D12_COMPUTE_PIPELINE_STATE_DESC
title: D3D12_COMPUTE_PIPELINE_STATE_DESC
author: windows-sdk-content
description: Describes a compute pipeline state object.
old-location: direct3d12\d3d12_compute_pipeline_state_desc.htm
tech.root: direct3d12
ms.assetid: 46C785C6-8294-410F-A8D5-7E5F85FA5C75
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: D3D12_COMPUTE_PIPELINE_STATE_DESC, D3D12_COMPUTE_PIPELINE_STATE_DESC structure, d3d12/D3D12_COMPUTE_PIPELINE_STATE_DESC, direct3d12.d3d12_compute_pipeline_state_desc
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
 - D3D12.h
api_name:
 - D3D12_COMPUTE_PIPELINE_STATE_DESC
product: Windows
targetos: Windows
req.typenames: D3D12_COMPUTE_PIPELINE_STATE_DESC
req.redist: 
---

# D3D12_COMPUTE_PIPELINE_STATE_DESC structure


## -description


Describes a compute pipeline state object.


## -struct-fields




### -field pRootSignature

A pointer to the <a href="https://msdn.microsoft.com/BEE01381-12C2-4DD9-9121-22BB5840ECD5">ID3D12RootSignature</a> object.
          


### -field CS

A <a href="https://msdn.microsoft.com/E2195755-A0C2-4824-A2EB-553F7909847F">D3D12_SHADER_BYTECODE</a> structure that describes the compute shader.
          


### -field NodeMask

For single GPU operation, set this to zero. If there are multiple GPU nodes, set bits to identify the nodes (the  device's physical adapters) for which the compute pipeline state is to apply.
            Each bit in the mask corresponds to a single node.
            Refer to <a href="https://msdn.microsoft.com/CC4C6594-D48F-40C1-93EE-9F98532BC038">Multi-Adapter</a>.


### -field CachedPSO

A cached pipeline state object, as a <a href="https://msdn.microsoft.com/82A0CF70-7A16-45D5-A717-0BBB35DCC5A6">D3D12_CACHED_PIPELINE_STATE</a> structure.
          


### -field Flags

A <a href="https://msdn.microsoft.com/DAE5C06B-ED1F-4B35-812E-31E26B51704C">D3D12_PIPELINE_STATE_FLAGS</a> enumeration constant such as for "tool debug".
          


## -remarks



This structure is used by <a href="https://msdn.microsoft.com/en-us/library/Dn788658(v=VS.85).aspx">CreateComputePipelineState</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn770459(v=VS.85).aspx">Core Structures</a>
 

 

