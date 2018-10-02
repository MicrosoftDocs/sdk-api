---
UID: NS:d3d12shader._D3D12_SHADER_VARIABLE_DESC
title: "_D3D12_SHADER_VARIABLE_DESC"
author: windows-sdk-content
description: Describes a shader variable.
old-location: direct3d12\d3d12_shader_variable_desc.htm
tech.root: direct3d12
ms.assetid: 117181AB-16F4-41D7-974D-E2C04FEE4FB1
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: D3D12_SHADER_VARIABLE_DESC, D3D12_SHADER_VARIABLE_DESC structure, _D3D12_SHADER_VARIABLE_DESC, d3d12shader/D3D12_SHADER_VARIABLE_DESC, direct3d12.d3d12_shader_variable_desc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d12shader.h
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
 - d3d12shader.h
api_name:
 - D3D12_SHADER_VARIABLE_DESC
product: Windows
targetos: Windows
req.typenames: D3D12_SHADER_VARIABLE_DESC
req.redist: 
---

# _D3D12_SHADER_VARIABLE_DESC structure


## -description


Describes a shader variable.
        


## -struct-fields




### -field Name

The variable name.
          


### -field StartOffset

Offset from the start of the parent structure to the beginning of the variable.
          


### -field Size

Size of the variable (in bytes).
          


### -field uFlags

A combination of <a href="https://msdn.microsoft.com/b89dc001-c335-4994-a644-88bfbeb7d663">D3D_SHADER_VARIABLE_FLAGS</a>-typed values that are combined by using a bitwise-OR operation. 
            The resulting value identifies shader-variable properties.
          


### -field DefaultValue

The default value for initializing the variable.
            Emits default values for reflection.
          


### -field StartTexture

Offset from the start of the variable to the beginning of the texture.


### -field TextureSize

The size of the texture, in bytes.
          


### -field StartSampler

Offset from the start of the variable to the beginning of the sampler.


### -field SamplerSize

The size of the sampler, in bytes.
          


## -remarks



Get a shader-variable description using reflection by calling <a href="https://msdn.microsoft.com/21CF98AF-5645-4059-992A-FFF778576C93">ID3D12ShaderReflectionVariable::GetDesc</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/b8ece5c3-5065-4711-b12c-6cf7ea0e1ba0">Shader Structures</a>
 

 

