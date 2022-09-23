---
UID: NS:d3d12shader._D3D12_PARAMETER_DESC
title: D3D12_PARAMETER_DESC (d3d12shader.h)
description: Describes a function parameter. (D3D12_PARAMETER_DESC)
helpviewer_keywords: ["D3D12_PARAMETER_DESC","D3D12_PARAMETER_DESC structure","d3d12shader/D3D12_PARAMETER_DESC","direct3d12.d3d12_parameter_desc"]
old-location: direct3d12\d3d12_parameter_desc.htm
tech.root: direct3d12
ms.assetid: CE32EC5C-2B12-44CA-A2B0-C9ED3E64849F
ms.date: 12/05/2018
ms.keywords: D3D12_PARAMETER_DESC, D3D12_PARAMETER_DESC structure, d3d12shader/D3D12_PARAMETER_DESC, direct3d12.d3d12_parameter_desc
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
targetos: Windows
req.typenames: D3D12_PARAMETER_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D12_PARAMETER_DESC
 - d3d12shader/_D3D12_PARAMETER_DESC
 - D3D12_PARAMETER_DESC
 - d3d12shader/D3D12_PARAMETER_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12shader.h
api_name:
 - D3D12_PARAMETER_DESC
---

# D3D12_PARAMETER_DESC structure


## -description

Describes a function parameter.

## -struct-fields

### -field Name

The name of the function parameter.

### -field SemanticName

The HLSL <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics">semantic</a> that is associated with this function parameter. This name includes the index, for example, SV_Target[n].

### -field Type

A <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type">D3D_SHADER_VARIABLE_TYPE</a>-typed value that identifies the variable type for the parameter.

### -field Class

A <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class">D3D_SHADER_VARIABLE_CLASS</a>-typed value that identifies the variable class for the parameter as one of scalar, vector, matrix, object, and so on.

### -field Rows

The number of rows for a matrix parameter.

### -field Columns

The number of columns for a matrix parameter.

### -field InterpolationMode

A <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_interpolation_mode">D3D_INTERPOLATION_MODE</a>-typed value that identifies the interpolation mode for the parameter.

### -field Flags

A combination of <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_parameter_flags">D3D_PARAMETER_FLAGS</a>-typed values that are combined by using a bitwise OR operation. The resulting value specifies semantic flags for the parameter.

### -field FirstInRegister

The first input register for this parameter.

### -field FirstInComponent

The first input register component for this parameter.

### -field FirstOutRegister

The first output register for this parameter.

### -field FirstOutComponent

The first output register component for this parameter.

## -remarks

Get a function-parameter description by calling <a href="/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12functionparameterreflection-getdesc">ID3D12FunctionParameterReflection::GetDesc</a>.

## -see-also

<a href="/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12functionparameterreflection-getdesc">ID3D12FunctionParameterReflection::GetDesc</a>



<a href="/windows/desktop/direct3d12/d3d12-graphics-reference-shader-structures">Shader Structures</a>
