---
UID: NS:d3d12shader._D3D12_SHADER_TYPE_DESC
title: "_D3D12_SHADER_TYPE_DESC"
author: windows-sdk-content
description: Describes a shader-variable type.
old-location: direct3d12\d3d12_shader_type_desc.htm
old-project: direct3d12
ms.assetid: B0AF7987-B25B-4496-9B8F-1D9C16DF5E50
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: D3D12_SHADER_TYPE_DESC, D3D12_SHADER_TYPE_DESC structure, _D3D12_SHADER_TYPE_DESC, d3d12shader/D3D12_SHADER_TYPE_DESC, direct3d12.d3d12_shader_type_desc
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
tech.root: 
req.typenames: D3D12_SHADER_TYPE_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12shader.h
api_name:
 - D3D12_SHADER_TYPE_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

