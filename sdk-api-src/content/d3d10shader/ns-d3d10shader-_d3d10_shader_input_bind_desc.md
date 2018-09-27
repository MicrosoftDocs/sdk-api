---
UID: NS:d3d10shader._D3D10_SHADER_INPUT_BIND_DESC
title: "_D3D10_SHADER_INPUT_BIND_DESC"
author: windows-sdk-content
description: Describes how a shader resource is bound to a shader input.
old-location: direct3d10\d3d10_shader_input_bind_desc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_input_bind_desc.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: 99c7399c-8b7c-2db1-c625-397e1a74f486, D3D10_SHADER_INPUT_BIND_DESC, D3D10_SHADER_INPUT_BIND_DESC structure [Direct3D 10], _D3D10_SHADER_INPUT_BIND_DESC, d3d10shader/D3D10_SHADER_INPUT_BIND_DESC, direct3d10.d3d10_shader_input_bind_desc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d10shader.h
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
 - D3D10Shader.h
api_name:
 - D3D10_SHADER_INPUT_BIND_DESC
product: Windows
targetos: Windows
req.typenames: D3D10_SHADER_INPUT_BIND_DESC
req.redist: 
---

# _D3D10_SHADER_INPUT_BIND_DESC structure


## -description


Describes how a shader resource is bound to a shader input.


## -struct-fields




### -field Name

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

Name of the shader resource.


### -field Type

Type: <b><a href="https://msdn.microsoft.com/67b8927a-e79a-42f5-845c-fe565ec7d8f8">D3D10_SHADER_INPUT_TYPE</a></b>

Identifies the type of data in the resource. See <a href="https://msdn.microsoft.com/67b8927a-e79a-42f5-845c-fe565ec7d8f8">D3D10_SHADER_INPUT_TYPE</a>.


### -field BindPoint

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Starting bind point.


### -field BindCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of contiguous bind points for arrays.


### -field uFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Shader input-parameter options. See <a href="https://msdn.microsoft.com/edde03b3-c952-40fc-ab3a-4e5a2edbfd3f">D3D10_SHADER_INPUT_FLAGS</a>.


### -field ReturnType

Type: <b><a href="https://msdn.microsoft.com/c53dd5fa-ced4-47f1-9842-78c81c305641">D3D10_RESOURCE_RETURN_TYPE</a></b>

If the input is a texture, the return type. See <a href="https://msdn.microsoft.com/c53dd5fa-ced4-47f1-9842-78c81c305641">D3D10_RESOURCE_RETURN_TYPE</a>.


### -field Dimension

Type: <b><a href="https://msdn.microsoft.com/2c2a6a68-179a-478b-bd86-c023a387601d">D3D10_SRV_DIMENSION</a></b>

Identifies the amount of data in the resource. See <a href="https://msdn.microsoft.com/2c2a6a68-179a-478b-bd86-c023a387601d">D3D10_SRV_DIMENSION</a>.


### -field NumSamples

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of samples for a multisampled texture; otherwise 0.


## -remarks



Get a shader-input-signature description by calling <a href="https://msdn.microsoft.com/e6e7717c-f4ca-4a65-bc52-d8a561a616e8">ID3D10ShaderReflection::GetResourceBindingDesc</a>.




## -see-also




<a href="https://msdn.microsoft.com/b36309e0-1c44-42d9-adcf-33acd753438c">Shader Structures</a>
 

 

