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
 

 

