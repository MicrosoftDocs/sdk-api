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
 

 

