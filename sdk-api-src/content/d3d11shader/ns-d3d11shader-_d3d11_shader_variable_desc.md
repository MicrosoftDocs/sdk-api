---
UID: NS:d3d11shader._D3D11_SHADER_VARIABLE_DESC
title: "_D3D11_SHADER_VARIABLE_DESC"
author: windows-sdk-content
description: Describes a shader variable.
old-location: direct3d11\d3d11_shader_variable_desc.htm
tech.root: direct3d11
ms.assetid: b5620fea-c7d1-4db1-9bd1-991a2efa3b4c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: D3D11_SHADER_VARIABLE_DESC, D3D11_SHADER_VARIABLE_DESC structure [Direct3D 11], _D3D11_SHADER_VARIABLE_DESC, cfce73ab-af25-fa7f-0d0a-e49af39dc5d8, d3d11shader/D3D11_SHADER_VARIABLE_DESC, direct3d11.d3d11_shader_variable_desc
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
 - D3D11_SHADER_VARIABLE_DESC
product: Windows
targetos: Windows
req.typenames: D3D11_SHADER_VARIABLE_DESC
req.redist: 
---

# _D3D11_SHADER_VARIABLE_DESC structure


## -description


Describes a shader variable.


## -struct-fields




### -field Name

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The variable name.


### -field StartOffset

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Offset from the start of the parent structure to the beginning of the variable.


### -field Size

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Size of the variable (in bytes).


### -field uFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A combination of <a href="https://msdn.microsoft.com/b89dc001-c335-4994-a644-88bfbeb7d663">D3D_SHADER_VARIABLE_FLAGS</a>-typed values that are combined by using a bitwise OR operation. The resulting value identifies shader-variable properties.
          


### -field DefaultValue

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPVOID</a></b>

The default value for initializing the variable.


### -field StartTexture

Type: <b>UINT</b>

Offset from the start of the variable to the beginning of the texture.




### -field TextureSize

Type: <b>UINT</b>

The size of the texture, in bytes. 




### -field StartSampler

Type: <b>UINT</b>

Offset from the start of the variable to the beginning of the sampler.




### -field SamplerSize

Type: <b>UINT</b>

The size of the sampler, in bytes. 


## -remarks



Get a shader-variable description using reflection by calling <a href="https://msdn.microsoft.com/a384e172-763f-4f4c-b6fb-f657fa31e5ee">ID3D11ShaderReflectionVariable::GetDesc</a>.
        

As of the June 2010 update, <b>DefaultValue</b> emits default values for reflection.
        




## -see-also




<a href="https://msdn.microsoft.com/3b8ece5c-5065-4711-b12c-06cf7ea0e1ba">Shader Structures</a>
 

 

