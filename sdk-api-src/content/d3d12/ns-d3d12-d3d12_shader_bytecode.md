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

# D3D12_SHADER_BYTECODE structure


## -description


Describes shader data.


## -struct-fields




### -field pShaderBytecode


            A pointer to a memory block that contains the shader data.
          


### -field BytecodeLength


            The size, in bytes, of the shader data that the <b>pShaderBytecode</b> member points to.
          


## -remarks




        The <a href="https://msdn.microsoft.com/35D10150-A633-4D38-B684-3E2DF357FFC0">D3D12_GRAPHICS_PIPELINE_STATE_DESC</a> and <a href="https://msdn.microsoft.com/46C785C6-8294-410F-A8D5-7E5F85FA5C75">D3D12_COMPUTE_PIPELINE_STATE_DESC</a> objects contain <b>D3D12_SHADER_BYTECODE</b> structures that describe various shader types.
      




## -see-also




<a href="https://msdn.microsoft.com/63719AA1-2119-456C-9D23-13933D38AFA9">CD3DX12_SHADER_BYTECODE</a>



<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

