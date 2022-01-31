---
UID: NE:d3dcommon._D3D_SHADER_VARIABLE_CLASS
title: D3D_SHADER_VARIABLE_CLASS (d3dcommon.h)
description: Values that identify the class of a shader variable.
helpviewer_keywords: ["D3D10_SVC_MATRIX_COLUMNS","D3D10_SVC_MATRIX_ROWS","D3D10_SVC_OBJECT","D3D10_SVC_SCALAR","D3D10_SVC_STRUCT","D3D10_SVC_VECTOR","D3D11_SVC_INTERFACE_CLASS","D3D11_SVC_INTERFACE_POINTER","D3D_SHADER_VARIABLE_CLASS","D3D_SHADER_VARIABLE_CLASS enumeration [Direct3D 11]","D3D_SVC_FORCE_DWORD","D3D_SVC_INTERFACE_CLASS","D3D_SVC_INTERFACE_POINTER","D3D_SVC_MATRIX_COLUMNS","D3D_SVC_MATRIX_ROWS","D3D_SVC_OBJECT","D3D_SVC_SCALAR","D3D_SVC_STRUCT","D3D_SVC_VECTOR","d3dcommon/D3D10_SVC_MATRIX_COLUMNS","d3dcommon/D3D10_SVC_MATRIX_ROWS","d3dcommon/D3D10_SVC_OBJECT","d3dcommon/D3D10_SVC_SCALAR","d3dcommon/D3D10_SVC_STRUCT","d3dcommon/D3D10_SVC_VECTOR","d3dcommon/D3D11_SVC_INTERFACE_CLASS","d3dcommon/D3D11_SVC_INTERFACE_POINTER","d3dcommon/D3D_SHADER_VARIABLE_CLASS","d3dcommon/D3D_SVC_FORCE_DWORD","d3dcommon/D3D_SVC_INTERFACE_CLASS","d3dcommon/D3D_SVC_INTERFACE_POINTER","d3dcommon/D3D_SVC_MATRIX_COLUMNS","d3dcommon/D3D_SVC_MATRIX_ROWS","d3dcommon/D3D_SVC_OBJECT","d3dcommon/D3D_SVC_SCALAR","d3dcommon/D3D_SVC_STRUCT","d3dcommon/D3D_SVC_VECTOR","direct3d11.d3d_shader_variable_class"]
old-location: direct3d11\d3d_shader_variable_class.htm
tech.root: direct3d11
ms.assetid: d367ba01-e357-468d-9417-7d5a282d5565
ms.date: 12/05/2018
ms.keywords: D3D10_SVC_MATRIX_COLUMNS, D3D10_SVC_MATRIX_ROWS, D3D10_SVC_OBJECT, D3D10_SVC_SCALAR, D3D10_SVC_STRUCT, D3D10_SVC_VECTOR, D3D11_SVC_INTERFACE_CLASS, D3D11_SVC_INTERFACE_POINTER, D3D_SHADER_VARIABLE_CLASS, D3D_SHADER_VARIABLE_CLASS enumeration [Direct3D 11], D3D_SVC_FORCE_DWORD, D3D_SVC_INTERFACE_CLASS, D3D_SVC_INTERFACE_POINTER, D3D_SVC_MATRIX_COLUMNS, D3D_SVC_MATRIX_ROWS, D3D_SVC_OBJECT, D3D_SVC_SCALAR, D3D_SVC_STRUCT, D3D_SVC_VECTOR, d3dcommon/D3D10_SVC_MATRIX_COLUMNS, d3dcommon/D3D10_SVC_MATRIX_ROWS, d3dcommon/D3D10_SVC_OBJECT, d3dcommon/D3D10_SVC_SCALAR, d3dcommon/D3D10_SVC_STRUCT, d3dcommon/D3D10_SVC_VECTOR, d3dcommon/D3D11_SVC_INTERFACE_CLASS, d3dcommon/D3D11_SVC_INTERFACE_POINTER, d3dcommon/D3D_SHADER_VARIABLE_CLASS, d3dcommon/D3D_SVC_FORCE_DWORD, d3dcommon/D3D_SVC_INTERFACE_CLASS, d3dcommon/D3D_SVC_INTERFACE_POINTER, d3dcommon/D3D_SVC_MATRIX_COLUMNS, d3dcommon/D3D_SVC_MATRIX_ROWS, d3dcommon/D3D_SVC_OBJECT, d3dcommon/D3D_SVC_SCALAR, d3dcommon/D3D_SVC_STRUCT, d3dcommon/D3D_SVC_VECTOR, direct3d11.d3d_shader_variable_class
req.header: d3dcommon.h
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
targetos: Windows
req.typenames: D3D_SHADER_VARIABLE_CLASS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D_SHADER_VARIABLE_CLASS
 - d3dcommon/_D3D_SHADER_VARIABLE_CLASS
 - D3D_SHADER_VARIABLE_CLASS
 - d3dcommon/D3D_SHADER_VARIABLE_CLASS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3DCommon.h
api_name:
 - D3D_SHADER_VARIABLE_CLASS
---

# D3D_SHADER_VARIABLE_CLASS enumeration


## -description

Values that identify the class of a shader variable.

> [!NOTE]
> For programming with Direct3D 10, this API has a type alias that begins `D3D10_` instead of `D3D_`. These Direct3D 10 type aliases are defined in `d3d10.h`, `d3d10misc.h`, and `d3d10shader.h`.

## -enum-fields

### -field D3D_SVC_SCALAR:0

The shader variable is a scalar.

### -field D3D_SVC_VECTOR

The shader variable is a vector.

### -field D3D_SVC_MATRIX_ROWS

The shader variable is a row-major matrix.

### -field D3D_SVC_MATRIX_COLUMNS

The shader variable is a column-major matrix.

### -field D3D_SVC_OBJECT

The shader variable is an object.

### -field D3D_SVC_STRUCT

The shader variable is a structure.

### -field D3D_SVC_INTERFACE_CLASS

The shader variable is a class.

### -field D3D_SVC_INTERFACE_POINTER

The shader variable is an interface.

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

### -field D3D_SVC_FORCE_DWORD:0x7fffffff

This value is not used by a programmer; it exists to force the enumeration to compile to 32 bits.

## -remarks

The class of a shader variable is not a programming class; the class identifies the variable class such as scalar, vector, object, and so on. <b>D3D_SHADER_VARIABLE_CLASS</b>-typed values are specified in the <b>Class</b> member of the <a href="/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_type_desc">D3D11_SHADER_TYPE_DESC</a> structure.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-common-enumerations">Common Version Enumerations</a>
