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
 

 

