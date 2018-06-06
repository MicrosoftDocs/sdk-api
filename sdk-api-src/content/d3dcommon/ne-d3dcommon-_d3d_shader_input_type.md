---
UID: NE:d3dcommon._D3D_SHADER_INPUT_TYPE
title: "_D3D_SHADER_INPUT_TYPE"
author: windows-sdk-content
description: Values that identify resource types that can be bound to a shader and that are reflected as part of the resource description for the shader.
old-location: direct3d11\d3d_shader_input_type.htm
old-project: direct3d11
ms.assetid: c6106f9e-420d-43e1-92ba-bc3a6e544e7d
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: D3D10_SIT_CBUFFER, D3D10_SIT_SAMPLER, D3D10_SIT_TBUFFER, D3D10_SIT_TEXTURE, D3D11_SIT_BYTEADDRESS, D3D11_SIT_STRUCTURED, D3D11_SIT_UAV_APPEND_STRUCTURED, D3D11_SIT_UAV_CONSUME_STRUCTURED, D3D11_SIT_UAV_RWBYTEADDRESS, D3D11_SIT_UAV_RWSTRUCTURED, D3D11_SIT_UAV_RWSTRUCTURED_WITH_COUNTER, D3D11_SIT_UAV_RWTYPED, D3D_SHADER_INPUT_TYPE, D3D_SHADER_INPUT_TYPE enumeration [Direct3D 11], D3D_SIT_BYTEADDRESS, D3D_SIT_CBUFFER, D3D_SIT_SAMPLER, D3D_SIT_STRUCTURED, D3D_SIT_TBUFFER, D3D_SIT_TEXTURE, D3D_SIT_UAV_APPEND_STRUCTURED, D3D_SIT_UAV_CONSUME_STRUCTURED, D3D_SIT_UAV_RWBYTEADDRESS, D3D_SIT_UAV_RWSTRUCTURED, D3D_SIT_UAV_RWSTRUCTURED_WITH_COUNTER, D3D_SIT_UAV_RWTYPED, _D3D_SHADER_INPUT_TYPE, d3dcommon/D3D10_SIT_CBUFFER, d3dcommon/D3D10_SIT_SAMPLER, d3dcommon/D3D10_SIT_TBUFFER, d3dcommon/D3D10_SIT_TEXTURE, d3dcommon/D3D11_SIT_BYTEADDRESS, d3dcommon/D3D11_SIT_STRUCTURED, d3dcommon/D3D11_SIT_UAV_APPEND_STRUCTURED, d3dcommon/D3D11_SIT_UAV_CONSUME_STRUCTURED, d3dcommon/D3D11_SIT_UAV_RWBYTEADDRESS, d3dcommon/D3D11_SIT_UAV_RWSTRUCTURED, d3dcommon/D3D11_SIT_UAV_RWSTRUCTURED_WITH_COUNTER, d3dcommon/D3D11_SIT_UAV_RWTYPED, d3dcommon/D3D_SHADER_INPUT_TYPE, d3dcommon/D3D_SIT_BYTEADDRESS, d3dcommon/D3D_SIT_CBUFFER, d3dcommon/D3D_SIT_SAMPLER, d3dcommon/D3D_SIT_STRUCTURED, d3dcommon/D3D_SIT_TBUFFER, d3dcommon/D3D_SIT_TEXTURE, d3dcommon/D3D_SIT_UAV_APPEND_STRUCTURED, d3dcommon/D3D_SIT_UAV_CONSUME_STRUCTURED, d3dcommon/D3D_SIT_UAV_RWBYTEADDRESS, d3dcommon/D3D_SIT_UAV_RWSTRUCTURED, d3dcommon/D3D_SIT_UAV_RWSTRUCTURED_WITH_COUNTER, d3dcommon/D3D_SIT_UAV_RWTYPED, direct3d11.d3d_shader_input_type
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
 - D3DCommon.h
api_name:
 - D3D_SHADER_INPUT_TYPE
product: Windows
targetos: Windows
req.lib: D3d9.lib
req.dll: 
req.irql: 
---

# _D3D_SHADER_INPUT_TYPE enumeration


## -description


Values that identify resource types that can be bound to a shader and that are reflected as part of the resource description for the shader.


## -enum-fields




### -field D3D_SIT_CBUFFER

The shader resource is a constant buffer.


### -field D3D_SIT_TBUFFER

The shader resource is a texture buffer.


### -field D3D_SIT_TEXTURE

The shader resource is a texture.


### -field D3D_SIT_SAMPLER

The shader resource is a sampler.


### -field D3D_SIT_UAV_RWTYPED

The shader resource is a read-and-write buffer.


### -field D3D_SIT_STRUCTURED

The shader resource is a structured buffer.

For more information about structured buffer, see the <b>Remarks</b> section.


### -field D3D_SIT_UAV_RWSTRUCTURED

The shader resource is a read-and-write structured buffer.


### -field D3D_SIT_BYTEADDRESS

The shader resource is a byte-address buffer.


### -field D3D_SIT_UAV_RWBYTEADDRESS

The shader resource is a read-and-write byte-address buffer.


### -field D3D_SIT_UAV_APPEND_STRUCTURED

The shader resource is an append-structured buffer.


### -field D3D_SIT_UAV_CONSUME_STRUCTURED

The shader resource is a consume-structured buffer.


### -field D3D_SIT_UAV_RWSTRUCTURED_WITH_COUNTER

The shader resource is a read-and-write structured buffer that uses the built-in counter to append or consume.


### -field D3D10_SIT_CBUFFER

The shader resource is a constant buffer.


### -field D3D10_SIT_TBUFFER

The shader resource is a texture buffer.


### -field D3D10_SIT_TEXTURE

The shader resource is a texture.


### -field D3D10_SIT_SAMPLER

The shader resource is a sampler.


### -field D3D11_SIT_UAV_RWTYPED

The shader resource is a read-and-write buffer.


### -field D3D11_SIT_STRUCTURED

The shader resource is a structured buffer.

For more information about structured buffer, see the <b>Remarks</b> section.


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



<b>D3D_SHADER_INPUT_TYPE</b>-typed values are specified in the <b>Type</b> member of the <a href="https://msdn.microsoft.com/384ad8f8-0991-4cd2-bb3d-76b8338686da">D3D11_SHADER_INPUT_BIND_DESC</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/002154d5-74a6-48fb-b55f-8687e4505fc7">Common Version Enumerations</a>
 

 

