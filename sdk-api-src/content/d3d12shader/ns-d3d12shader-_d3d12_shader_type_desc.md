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

# _D3D12_SHADER_TYPE_DESC structure


## -description



          Describes a shader-variable type.
        


## -struct-fields




### -field Class


            A <a href="https://msdn.microsoft.com/d367ba01-e357-468d-9417-7d5a282d5565">D3D_SHADER_VARIABLE_CLASS</a>-typed value that identifies the variable class as one of scalar, vector, matrix, object, and so on.
          


### -field Type


            A <a href="https://msdn.microsoft.com/ef07a68c-d944-4dbb-8cb1-c50403c6c8e8">D3D_SHADER_VARIABLE_TYPE</a>-typed value that identifies the variable type.
          


### -field Rows


            Number of rows in a matrix. Otherwise a numeric type returns 1, any other type returns 0.
          


### -field Columns


            Number of columns in a matrix. Otherwise a numeric type returns 1, any other type returns 0.
          


### -field Elements


            Number of elements in an array; otherwise 0.
          


### -field Members


            Number of members in the structure; otherwise 0.
          


### -field Offset


            Offset, in bytes, between the start of the parent structure and this variable. Can be 0 if not a structure member.
          


### -field Name


            Name of the shader-variable type. This member can be <b>NULL</b> if it isn't used. This member supports dynamic shader linkage interface types, which have names. For more info about dynamic shader linkage, see <a href="https://msdn.microsoft.com/2f5f7852-0f0a-4fad-a412-9a0d634c73b6">Dynamic Linking</a>.
          


## -remarks




        Get a shader-variable-type description by calling <a href="https://msdn.microsoft.com/E5C28FFE-5BA4-436F-9CDB-215B5B9918F9">ID3D12ShaderReflectionType::GetDesc</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/b8ece5c3-5065-4711-b12c-6cf7ea0e1ba0">Shader Structures</a>
 

 

