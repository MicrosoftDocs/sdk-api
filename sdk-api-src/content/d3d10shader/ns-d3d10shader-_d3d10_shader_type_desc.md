---
UID: NS:d3d10shader._D3D10_SHADER_TYPE_DESC
title: "_D3D10_SHADER_TYPE_DESC"
author: windows-sdk-content
description: Describes a shader-variable type.
old-location: direct3d10\d3d10_shader_type_desc.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_type_desc.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: D3D10_SHADER_TYPE_DESC, D3D10_SHADER_TYPE_DESC structure [Direct3D 10], _D3D10_SHADER_TYPE_DESC, b18f1523-7db4-ff5b-d9ab-04f0e773c99b, d3d10shader/D3D10_SHADER_TYPE_DESC, direct3d10.d3d10_shader_type_desc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d10shader.h
req.include-header: 
req.redist: 
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
req.typenames: D3D10_SHADER_TYPE_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10Shader.h
api_name:
 - D3D10_SHADER_TYPE_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3D10_SHADER_TYPE_DESC structure


## -description


Describes a shader-variable type.


## -struct-fields




### -field Class

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172440(v=VS.85).aspx">D3D10_SHADER_VARIABLE_CLASS</a></b>

Identifies the variable class as one of scalar, vector, matrix or object. See <a href="https://msdn.microsoft.com/en-us/library/Bb172440(v=VS.85).aspx">D3D10_SHADER_VARIABLE_CLASS</a>.


### -field Type

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172443(v=VS.85).aspx">D3D10_SHADER_VARIABLE_TYPE</a></b>

The variable type. See <a href="https://msdn.microsoft.com/en-us/library/Bb172443(v=VS.85).aspx">D3D10_SHADER_VARIABLE_TYPE</a>.


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

Offset, in bytes, between the start of the parent structure and this variable.


## -remarks



Get a shader-variable-type description by calling <a href="https://msdn.microsoft.com/en-us/library/Bb173841(v=VS.85).aspx">ID3D10ShaderReflectionType::GetDesc</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205159(v=VS.85).aspx">Shader Structures</a>
 

 

