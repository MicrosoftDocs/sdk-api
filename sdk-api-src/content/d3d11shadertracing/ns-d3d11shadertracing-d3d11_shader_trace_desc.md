---
UID: NS:d3d11shadertracing.D3D11_SHADER_TRACE_DESC
title: D3D11_SHADER_TRACE_DESC
author: windows-sdk-content
description: Describes a shader-trace object.
old-location: direct3d11\d3d11_shader_trace_desc.htm
tech.root: direct3d11
ms.assetid: 0BF5D48F-EBC5-445B-B315-496C50411C72
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: D3D11_SHADER_TRACE_DESC, D3D11_SHADER_TRACE_DESC structure [Direct3D 11], d3d11shadertracing/D3D11_SHADER_TRACE_DESC, direct3d11.d3d11_shader_trace_desc
ms.prod: windows
ms.technology: windows-sdk
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
 - D3D11_SHADER_TRACE_DESC
product: Windows
targetos: Windows
req.typenames: D3D11_SHADER_TRACE_DESC
req.redist: 
---

# D3D11_SHADER_TRACE_DESC structure


## -description


Describes a shader-trace object.


## -struct-fields




### -field Type

A <a href="https://msdn.microsoft.com/4F7C8BF5-3C6E-470E-AFAA-34F4F78DAC15">D3D11_SHADER_TYPE</a>-typed value that identifies the type of shader that the shader-trace object describes. This member also determines which shader-trace type to use in the following union.
          


### -field Flags

A combination of the following flags that are combined by using a bitwise <b>OR</b> operation. The resulting value specifies how <a href="https://msdn.microsoft.com/8F63E8B3-0E36-49D5-AB3B-1B1C7A9B841A">ID3D11ShaderTraceFactory::CreateShaderTrace</a> creates the shader-trace object.

<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td>D3D11_SHADER_TRACE_FLAG_RECORD_REGISTER_WRITES (0x1)</td>
<td>The shader trace object records register-writes.</td>
</tr>
<tr>
<td>D3D11_SHADER_TRACE_FLAG_RECORD_REGISTER_READS (0x2)</td>
<td>The shader trace object records register-reads.</td>
</tr>
</table>
 


### -field VertexShaderTraceDesc

A <a href="https://msdn.microsoft.com/6D69DCE7-74BE-4FFE-8044-B16CB5EC1C07">D3D11_VERTEX_SHADER_TRACE_DESC</a> structure that describes an instance of a vertex shader to trace.
            


### -field HullShaderTraceDesc

A <a href="https://msdn.microsoft.com/E91FE826-C1BC-4583-83B0-FF2869AF86F2">D3D11_HULL_SHADER_TRACE_DESC</a> structure that describes an instance of a hull shader to trace.
            


### -field DomainShaderTraceDesc

A <a href="https://msdn.microsoft.com/A513A751-06BB-4298-82A5-BBBF6DCEBD1F">D3D11_DOMAIN_SHADER_TRACE_DESC</a> structure that describes an instance of a domain shader to trace.
            


### -field GeometryShaderTraceDesc

A <a href="https://msdn.microsoft.com/1E7E5BA5-C0CE-49ED-8AD3-A13300D867E0">D3D11_GEOMETRY_SHADER_TRACE_DESC</a> structure that describes an instance of a geometry shader to trace.
            


### -field PixelShaderTraceDesc

A <a href="https://msdn.microsoft.com/4A44DA4F-81FC-47BE-90CA-06355C363795">D3D11_PIXEL_SHADER_TRACE_DESC</a> structure that describes an instance of a pixel shader to trace.
            


### -field ComputeShaderTraceDesc

A <a href="https://msdn.microsoft.com/C047CA31-22D4-4512-B90C-3C77BA6AADA9">D3D11_COMPUTE_SHADER_TRACE_DESC</a> structure that describes an instance of a compute shader to trace.
            


## -remarks



This API requires the Windows Software Development Kit (SDK) for Windows 8.
      




## -see-also




<a href="https://msdn.microsoft.com/8F63E8B3-0E36-49D5-AB3B-1B1C7A9B841A">ID3D11ShaderTraceFactory::CreateShaderTrace</a>



<a href="https://msdn.microsoft.com/3b8ece5c-5065-4711-b12c-06cf7ea0e1ba">Shader Structures</a>
 

 

