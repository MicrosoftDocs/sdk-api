---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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




        This structure is used by <a href="https://msdn.microsoft.com/FFA361B2-D8FA-4F5A-8D0C-022C2AA76B57">CreateComputePipelineState</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

