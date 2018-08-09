---
UID: NE:d3dcommon._D3D_SHADER_INPUT_TYPE
title: "_D3D_SHADER_INPUT_TYPE"
author: windows-sdk-content
description: These flags identify resource types that can be bound to a shader and that are reflected as part of the resource description for the shader.
old-location: direct3d10\d3d10_shader_input_type.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_input_type.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 916808bd-9c2a-6f27-6001-74cdb922f16d, D3D10_SHADER_INPUT_TYPE, D3D10_SHADER_INPUT_TYPE enumeration [Direct3D 10], D3D10_SIT_CBUFFER, D3D10_SIT_SAMPLER, D3D10_SIT_TBUFFER, D3D10_SIT_TEXTURE, D3D11_SIT_BYTEADDRESS, D3D11_SIT_STRUCTURED, D3D11_SIT_UAV_APPEND_STRUCTURED, D3D11_SIT_UAV_CONSUME_STRUCTURED, D3D11_SIT_UAV_RWBYTEADDRESS, D3D11_SIT_UAV_RWSTRUCTURED, D3D11_SIT_UAV_RWSTRUCTURED_WITH_COUNTER, D3D11_SIT_UAV_RWTYPED, D3D_SHADER_INPUT_TYPE, LPD3D10_SHADER_INPUT_TYPE, LPD3D10_SHADER_INPUT_TYPE enumeration pointer [Direct3D 10], _D3D_SHADER_INPUT_TYPE, d3d10shader/D3D10_SHADER_INPUT_TYPE, d3d10shader/D3D10_SIT_CBUFFER, d3d10shader/D3D10_SIT_SAMPLER, d3d10shader/D3D10_SIT_TBUFFER, d3d10shader/D3D10_SIT_TEXTURE, d3d10shader/D3D11_SIT_BYTEADDRESS, d3d10shader/D3D11_SIT_STRUCTURED, d3d10shader/D3D11_SIT_UAV_APPEND_STRUCTURED, d3d10shader/D3D11_SIT_UAV_CONSUME_STRUCTURED, d3d10shader/D3D11_SIT_UAV_RWBYTEADDRESS, d3d10shader/D3D11_SIT_UAV_RWSTRUCTURED, d3d10shader/D3D11_SIT_UAV_RWSTRUCTURED_WITH_COUNTER, d3d10shader/D3D11_SIT_UAV_RWTYPED, d3d10shader/LPD3D10_SHADER_INPUT_TYPE, d3dcommon/D3D10_SHADER_INPUT_TYPE, d3dcommon/D3D10_SIT_CBUFFER, d3dcommon/D3D10_SIT_SAMPLER, d3dcommon/D3D10_SIT_TBUFFER, d3dcommon/D3D10_SIT_TEXTURE, d3dcommon/D3D11_SIT_BYTEADDRESS, d3dcommon/D3D11_SIT_STRUCTURED, d3dcommon/D3D11_SIT_UAV_APPEND_STRUCTURED, d3dcommon/D3D11_SIT_UAV_CONSUME_STRUCTURED, d3dcommon/D3D11_SIT_UAV_RWBYTEADDRESS, d3dcommon/D3D11_SIT_UAV_RWSTRUCTURED, d3dcommon/D3D11_SIT_UAV_RWSTRUCTURED_WITH_COUNTER, d3dcommon/D3D11_SIT_UAV_RWTYPED, d3dcommon/LPD3D10_SHADER_INPUT_TYPE, direct3d10.d3d10_shader_input_type
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3dcommon.h
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
req.typenames: D3D_SHADER_INPUT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10Shader.h
 - d3dcommon.h
api_name:
 - D3D10_SHADER_INPUT_TYPE
product: Windows
targetos: Windows
req.lib: D3d9.lib
req.dll: 
req.irql: 
---

# _D3D_SHADER_INPUT_TYPE enumeration


## -description


These flags identify resource types that can be bound to a shader and that are reflected as part of the resource description for the shader.


## -enum-fields




### -field D3D_SIT_CBUFFER


### -field D3D_SIT_TBUFFER


### -field D3D_SIT_TEXTURE


### -field D3D_SIT_SAMPLER


### -field D3D_SIT_UAV_RWTYPED


### -field D3D_SIT_STRUCTURED


### -field D3D_SIT_UAV_RWSTRUCTURED


### -field D3D_SIT_BYTEADDRESS


### -field D3D_SIT_UAV_RWBYTEADDRESS


### -field D3D_SIT_UAV_APPEND_STRUCTURED


### -field D3D_SIT_UAV_CONSUME_STRUCTURED


### -field D3D_SIT_UAV_RWSTRUCTURED_WITH_COUNTER


### -field D3D10_SIT_CBUFFER

The shader resource is a constant buffer.


### -field D3D10_SIT_TBUFFER

The shader resource is a texture buffer.


### -field D3D10_SIT_TEXTURE

The shader resource is a texture.


### -field D3D10_SIT_SAMPLER

The shader resource is a sampler.


### -field D3D11_SIT_UAV_RWTYPED

The shader resource is a read and write buffer.


### -field D3D11_SIT_STRUCTURED

The shader resource is a structured buffer.

For more information about structured buffers, see the <b>Remarks</b> section.


### -field D3D11_SIT_UAV_RWSTRUCTURED

The shader resource is a read-and-write structured buffer.


### -field D3D11_SIT_BYTEADDRESS

The shader resource is a byte-address buffer.


### -field D3D11_SIT_UAV_RWBYTEADDRESS

The shader resource is a read-and-write byte-address buffer.


### -field D3D11_SIT_UAV_APPEND_STRUCTURED

The shader resource is an append-structured buffer.


### -field D3D11_SIT_UAV_CONSUME_STRUCTURED

The shader resource is a consume-structured buffer.


### -field D3D11_SIT_UAV_RWSTRUCTURED_WITH_COUNTER

The shader resource is a read-and-write structured buffer that uses the built-in counter to append or consume.


## -remarks



These flags describe a shader resource that is used as an input in a shader-input-signature description (see <a href="https://msdn.microsoft.com/en-us/library/Bb172433(v=VS.85).aspx">D3D10_SHADER_INPUT_BIND_DESC</a>).

The types in a structured buffer describe the structure of the elements in the buffer. The layout of these types generally match their C++ struct counterparts, and are available through the type-reflection system. The following examples show structured buffers:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>struct mystruct {float4 val; uint ind;}; RWStructuredBuffer&lt;mystruct&gt; rwbuf;
RWStructuredBuffer&lt;float3&gt; rwbuf2;</pre>
</td>
</tr>
</table></span></div>
The <b>D3D10_SHADER_INPUT_TYPE</b>     enumeration is type defined in the  D3D10shader.h header file as a <a href="https://msdn.microsoft.com/c6106f9e-420d-43e1-92ba-bc3a6e544e7d">D3D_SHADER_INPUT_TYPE</a> enumeration, which is fully defined in the  D3DCommon.h header file.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
typedef D3D_SHADER_INPUT_TYPE D3D10_SHADER_INPUT_TYPE;</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205156(v=VS.85).aspx">Shader Enumerations</a>
 

 

