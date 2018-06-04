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

# _D3D12_SHADER_BUFFER_DESC structure


## -description



          Describes a shader constant-buffer.
        


## -struct-fields




### -field Name


            The name of the buffer.
          


### -field Type


            A <a href="https://msdn.microsoft.com/b21a460b-63cb-49c1-bd6c-a747df495efc">D3D_CBUFFER_TYPE</a>-typed value that indicates the intended use of the constant data.
          


### -field Variables


            The number of unique variables.
          


### -field Size


            The size of the buffer, in bytes.
          


### -field uFlags


            A combination of <a href="https://msdn.microsoft.com/f641b3ec-5492-4835-9cf6-e41447e4b6b6">D3D_SHADER_CBUFFER_FLAGS</a>-typed values that are combined by using a bitwise OR operation. The resulting value specifies properties for the shader constant-buffer.
          


## -remarks




        Constants are supplied to shaders in a shader-constant buffer. Get the description of a shader-constant-buffer by calling <a href="https://msdn.microsoft.com/33D6926F-BF1B-4424-BC28-83F8A4A30589">ID3D12ShaderReflectionConstantBuffer::GetDesc</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/b8ece5c3-5065-4711-b12c-6cf7ea0e1ba0">Shader Structures</a>
 

 

