---
UID: NS:d3d12.D3D12_SHADER_BYTECODE
title: D3D12_SHADER_BYTECODE
author: windows-sdk-content
description: Describes shader data.
old-location: direct3d12\d3d12_shader_bytecode.htm
old-project: direct3d12
ms.assetid: E2195755-A0C2-4824-A2EB-553F7909847F
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: D3D12_SHADER_BYTECODE, D3D12_SHADER_BYTECODE structure, d3d12/D3D12_SHADER_BYTECODE, direct3d12.d3d12_shader_bytecode
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
tech.root: 
req.typenames: D3D12_SHADER_BYTECODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_SHADER_BYTECODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

