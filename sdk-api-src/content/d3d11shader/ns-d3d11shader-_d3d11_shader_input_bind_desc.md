---
UID: NS:d3d11shader._D3D11_SHADER_INPUT_BIND_DESC
title: "_D3D11_SHADER_INPUT_BIND_DESC"
author: windows-sdk-content
description: Describes how a shader resource is bound to a shader input.
old-location: direct3d11\d3d11_shader_input_bind_desc.htm
tech.root: direct3d11
ms.assetid: 384ad8f8-0991-4cd2-bb3d-76b8338686da
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: D3D11_SHADER_INPUT_BIND_DESC, D3D11_SHADER_INPUT_BIND_DESC structure [Direct3D 11], _D3D11_SHADER_INPUT_BIND_DESC, b6214f45-418b-2509-b9d9-f7513efc5ba6, d3d11shader/D3D11_SHADER_INPUT_BIND_DESC, direct3d11.d3d11_shader_input_bind_desc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d11shader.h
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
 - D3D11Shader.h
api_name:
 - D3D11_SHADER_INPUT_BIND_DESC
product: Windows
targetos: Windows
req.typenames: D3D11_SHADER_INPUT_BIND_DESC
req.redist: 
---

# _D3D11_SHADER_INPUT_BIND_DESC structure


## -description


Describes how a shader resource is bound to a shader input.


## -struct-fields




### -field Name

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

Name of the shader resource.


### -field Type

Type: <b><a href="https://msdn.microsoft.com/c6106f9e-420d-43e1-92ba-bc3a6e544e7d">D3D_SHADER_INPUT_TYPE</a></b>

A <a href="https://msdn.microsoft.com/c6106f9e-420d-43e1-92ba-bc3a6e544e7d">D3D_SHADER_INPUT_TYPE</a>-typed value that identifies the type of data in the resource.


### -field BindPoint

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Starting bind point.


### -field BindCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of contiguous bind points for arrays.


### -field uFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A combination of <a href="https://msdn.microsoft.com/3c79331e-73c0-42d7-9948-6ac2671a4ab5">D3D_SHADER_INPUT_FLAGS</a>-typed values for shader input-parameter options.  


### -field ReturnType

Type: <b><a href="https://msdn.microsoft.com/3da3f315-9f92-4557-93b8-94aff42a91fe">D3D_RESOURCE_RETURN_TYPE</a></b>

If the input is a texture, the <a href="https://msdn.microsoft.com/3da3f315-9f92-4557-93b8-94aff42a91fe">D3D_RESOURCE_RETURN_TYPE</a>-typed value that identifies the return type.


### -field Dimension

Type: <b><a href="https://msdn.microsoft.com/6f3c2429-83be-44cd-89bb-b074bfa084e3">D3D_SRV_DIMENSION</a></b>

A <a href="https://msdn.microsoft.com/6f3c2429-83be-44cd-89bb-b074bfa084e3">D3D_SRV_DIMENSION</a>-typed value that identifies the dimensions of the bound resource.


### -field NumSamples

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of samples for a multisampled texture; when a texture isn't multisampled, the value is set to -1 (0xFFFFFFFF). 


## -remarks



Get a shader-input-signature description by calling <a href="https://msdn.microsoft.com/2bd540f5-513d-4dd5-ab28-b0e8083231eb">ID3D11ShaderReflection::GetResourceBindingDesc</a> or <a href="https://msdn.microsoft.com/b4bddcc0-c2fd-4dac-b999-cfbe1d318777">ID3D11ShaderReflection::GetResourceBindingDescByName</a>.




## -see-also




<a href="https://msdn.microsoft.com/3b8ece5c-5065-4711-b12c-06cf7ea0e1ba">Shader Structures</a>
 

 

