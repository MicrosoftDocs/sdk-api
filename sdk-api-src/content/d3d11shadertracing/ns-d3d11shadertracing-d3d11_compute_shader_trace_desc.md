---
UID: NS:d3d11shadertracing.D3D11_COMPUTE_SHADER_TRACE_DESC
title: D3D11_COMPUTE_SHADER_TRACE_DESC
author: windows-sdk-content
description: Describes an instance of a compute shader to trace.
old-location: direct3d11\d3d11_compute_shader_trace_desc.htm
tech.root: direct3d11
ms.assetid: C047CA31-22D4-4512-B90C-3C77BA6AADA9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D11_COMPUTE_SHADER_TRACE_DESC, D3D11_COMPUTE_SHADER_TRACE_DESC structure [Direct3D 11], d3d11shadertracing/D3D11_COMPUTE_SHADER_TRACE_DESC, direct3d11.d3d11_compute_shader_trace_desc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d11shadertracing.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - D3D11ShaderTracing.h
api_name:
 - D3D11_COMPUTE_SHADER_TRACE_DESC
product: Windows
targetos: Windows
req.typenames: D3D11_COMPUTE_SHADER_TRACE_DESC
req.redist: 
---

# D3D11_COMPUTE_SHADER_TRACE_DESC structure


## -description


Describes an instance of a compute shader to trace.


## -struct-fields




### -field Invocation

The invocation number of the instance of the compute shader.


### -field ThreadIDInGroup

The <a href="https://msdn.microsoft.com/be944592-c4ea-43c9-88bc-98a9a190a437">SV_GroupThreadID</a> to trace. This value identifies indexes of individual threads within a thread group that a compute shader executes in.
          


### -field ThreadGroupID

The <a href="https://msdn.microsoft.com/1b90ca74-a2b6-4a5f-aa4a-1ec879360593">SV_GroupID</a> to trace. This value identifies indexes of a thread group that the compute shader executes in.
          


## -remarks



This API requires the Windows Software Development Kit (SDK) for Windows 8.
      




## -see-also




<a href="https://msdn.microsoft.com/3b8ece5c-5065-4711-b12c-06cf7ea0e1ba">Shader Structures</a>
 

 

