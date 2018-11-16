---
UID: NS:d3d11shader._D3D11_SHADER_TYPE_DESC
title: "_D3D11_SHADER_TYPE_DESC"
author: windows-sdk-content
description: Describes a shader-variable type.
old-location: direct3d11\d3d11_shader_type_desc.htm
tech.root: direct3d11
ms.assetid: 8d2067a3-17f8-4496-a613-581f5e35fe93
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 071e4c6b-35a1-909a-b08c-bb43e4a73d5a, D3D11_SHADER_TYPE_DESC, D3D11_SHADER_TYPE_DESC structure [Direct3D 11], _D3D11_SHADER_TYPE_DESC, d3d11shader/D3D11_SHADER_TYPE_DESC, direct3d11.d3d11_shader_type_desc
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
 - D3D11_SHADER_TYPE_DESC
product: Windows
targetos: Windows
req.typenames: D3D11_SHADER_TYPE_DESC
req.redist: 
---

# _D3D11_SHADER_TYPE_DESC structure


## -description


Describes a shader-variable type.


## -struct-fields




### -field Class

Type: <b><a href="https://msdn.microsoft.com/d367ba01-e357-468d-9417-7d5a282d5565">D3D_SHADER_VARIABLE_CLASS</a></b>

A <a href="https://msdn.microsoft.com/d367ba01-e357-468d-9417-7d5a282d5565">D3D_SHADER_VARIABLE_CLASS</a>-typed value that identifies the variable class as one of scalar, vector, matrix, object, and so on.


### -field Type

Type: <b><a href="https://msdn.microsoft.com/ef07a68c-d944-4dbb-8cb1-c50403c6c8e8">D3D_SHADER_VARIABLE_TYPE</a></b>

A <a href="https://msdn.microsoft.com/ef07a68c-d944-4dbb-8cb1-c50403c6c8e8">D3D_SHADER_VARIABLE_TYPE</a>-typed value that identifies the variable type.


### -field Rows

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of rows in a matrix. Otherwise a numeric type returns 1, any other type returns 0.


### -field Columns

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of columns in a matrix. Otherwise a numeric type returns 1, any other type returns 0.


### -field Elements

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of elements in an array; otherwise 0.


### -field Members

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of members in the structure; otherwise 0.


### -field Offset

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Offset, in bytes, between the start of the parent structure and this variable. Can be 0 if not a structure member.


### -field Name

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

Name of the shader-variable type. This member can be <b>NULL</b> if it isn't used. This member supports dynamic shader linkage interface types, which have names. For more info about dynamic shader linkage, see <a href="https://msdn.microsoft.com/2f5f7852-0f0a-4fad-a412-9a0d634c73b6">Dynamic Linking</a>.


## -remarks



Get a shader-variable-type description by calling <a href="https://msdn.microsoft.com/96296270-fcca-4843-bd0a-78c7f87136e5">ID3D11ShaderReflectionType::GetDesc</a>.




## -see-also




<a href="https://msdn.microsoft.com/3b8ece5c-5065-4711-b12c-06cf7ea0e1ba">Shader Structures</a>
 

 

