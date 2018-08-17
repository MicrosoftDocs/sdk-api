---
UID: NE:d3dcommon._D3D_SHADER_VARIABLE_CLASS
title: "_D3D_SHADER_VARIABLE_CLASS"
author: windows-sdk-content
description: These flags identify the shader-variable class.
old-location: direct3d10\d3d10_shader_variable_class.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_variable_class.htm
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: 4b5cfc29-21a8-7a79-2f99-3915047892cb, D3D10_SHADER_VARIABLE_CLASS, D3D10_SHADER_VARIABLE_CLASS enumeration [Direct3D 10], D3D10_SVC_FORCE_DWORD, D3D10_SVC_MATRIX_COLUMNS, D3D10_SVC_MATRIX_ROWS, D3D10_SVC_OBJECT, D3D10_SVC_SCALAR, D3D10_SVC_STRUCT, D3D10_SVC_VECTOR, D3D11_SVC_INTERFACE_CLASS, D3D11_SVC_INTERFACE_POINTER, D3D_SHADER_VARIABLE_CLASS, LPD3D10_SHADER_VARIABLE_CLASS, LPD3D10_SHADER_VARIABLE_CLASS enumeration pointer [Direct3D 10], _D3D_SHADER_VARIABLE_CLASS, d3d10shader/D3D10_SHADER_VARIABLE_CLASS, d3d10shader/D3D10_SVC_FORCE_DWORD, d3d10shader/D3D10_SVC_MATRIX_COLUMNS, d3d10shader/D3D10_SVC_MATRIX_ROWS, d3d10shader/D3D10_SVC_OBJECT, d3d10shader/D3D10_SVC_SCALAR, d3d10shader/D3D10_SVC_STRUCT, d3d10shader/D3D10_SVC_VECTOR, d3d10shader/D3D11_SVC_INTERFACE_CLASS, d3d10shader/D3D11_SVC_INTERFACE_POINTER, d3d10shader/LPD3D10_SHADER_VARIABLE_CLASS, d3dcommon/D3D10_SHADER_VARIABLE_CLASS, d3dcommon/D3D10_SVC_FORCE_DWORD, d3dcommon/D3D10_SVC_MATRIX_COLUMNS, d3dcommon/D3D10_SVC_MATRIX_ROWS, d3dcommon/D3D10_SVC_OBJECT, d3dcommon/D3D10_SVC_SCALAR, d3dcommon/D3D10_SVC_STRUCT, d3dcommon/D3D10_SVC_VECTOR, d3dcommon/D3D11_SVC_INTERFACE_CLASS, d3dcommon/D3D11_SVC_INTERFACE_POINTER, d3dcommon/LPD3D10_SHADER_VARIABLE_CLASS, direct3d10.d3d10_shader_variable_class
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3dcommon.h
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
req.typenames: D3D_SHADER_VARIABLE_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10Shader.h
 - d3dcommon.h
api_name:
 - D3D10_SHADER_VARIABLE_CLASS
product: Windows
targetos: Windows
req.lib: D3d9.lib
req.dll: 
req.irql: 
---

# _D3D_SHADER_VARIABLE_CLASS enumeration


## -description


These flags identify the shader-variable class.


## -enum-fields




### -field D3D_SVC_SCALAR


### -field D3D_SVC_VECTOR


### -field D3D_SVC_MATRIX_ROWS


### -field D3D_SVC_MATRIX_COLUMNS


### -field D3D_SVC_OBJECT


### -field D3D_SVC_STRUCT


### -field D3D_SVC_INTERFACE_CLASS


### -field D3D_SVC_INTERFACE_POINTER


### -field D3D10_SVC_SCALAR

The shader variable is a scalar.


### -field D3D10_SVC_VECTOR

The shader variable is a vector.


### -field D3D10_SVC_MATRIX_ROWS

The shader variable is a row-major matrix.


### -field D3D10_SVC_MATRIX_COLUMNS

The shader variable is a column-major matrix.


### -field D3D10_SVC_OBJECT

The shader variable is an object.


### -field D3D10_SVC_STRUCT

The shader variable is a structure.


### -field D3D11_SVC_INTERFACE_CLASS

The shader variable is a class.


### -field D3D11_SVC_INTERFACE_POINTER

The shader variable is an interface.


### -field D3D_SVC_FORCE_DWORD




#### - D3D10_SVC_FORCE_DWORD

This value is not used by a programmer; it exists to force the enumeration to compile to 32 bits.


## -remarks



These flags describe the class of a shader variable. This is not a programming class; the class identifies the variable class such as scalar, vector, object, and so on. The shader-variable class is used in a shader-variable-type description (see <a href="https://msdn.microsoft.com/en-us/library/Bb172439(v=VS.85).aspx">D3D10_SHADER_TYPE_DESC</a>).

The <b>D3D10_SHADER_VARIABLE_CLASS</b>     enumeration is type defined in the  D3D10shader.h header file as a <a href="https://msdn.microsoft.com/d367ba01-e357-468d-9417-7d5a282d5565">D3D_SHADER_VARIABLE_CLASS</a> enumeration, which is fully defined in the  D3DCommon.h header file.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
typedef D3D_SHADER_VARIABLE_CLASS D3D10_SHADER_VARIABLE_CLASS;</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205156(v=VS.85).aspx">Shader Enumerations</a>
 

 

