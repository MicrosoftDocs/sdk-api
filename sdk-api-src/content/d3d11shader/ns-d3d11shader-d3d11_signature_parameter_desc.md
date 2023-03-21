---
UID: NS:d3d11shader._D3D11_SIGNATURE_PARAMETER_DESC
title: D3D11_SIGNATURE_PARAMETER_DESC (d3d11shader.h)
description: Describes a shader signature. (D3D11_SIGNATURE_PARAMETER_DESC)
helpviewer_keywords: ["D3D11_SIGNATURE_PARAMETER_DESC","D3D11_SIGNATURE_PARAMETER_DESC structure [Direct3D 11]","d3d11shader/D3D11_SIGNATURE_PARAMETER_DESC","direct3d11.d3d11_signature_parameter_desc","e870121a-ce22-1699-8203-c018e7d5db8e"]
old-location: direct3d11\d3d11_signature_parameter_desc.htm
tech.root: direct3d11
ms.assetid: 3aed2f5f-1cfa-4224-bfcc-7d015e6a2cc0
ms.date: 12/05/2018
ms.keywords: D3D11_SIGNATURE_PARAMETER_DESC, D3D11_SIGNATURE_PARAMETER_DESC structure [Direct3D 11], d3d11shader/D3D11_SIGNATURE_PARAMETER_DESC, direct3d11.d3d11_signature_parameter_desc, e870121a-ce22-1699-8203-c018e7d5db8e
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
targetos: Windows
req.typenames: D3D11_SIGNATURE_PARAMETER_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D11_SIGNATURE_PARAMETER_DESC
 - d3d11shader/_D3D11_SIGNATURE_PARAMETER_DESC
 - D3D11_SIGNATURE_PARAMETER_DESC
 - d3d11shader/D3D11_SIGNATURE_PARAMETER_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11Shader.h
api_name:
 - D3D11_SIGNATURE_PARAMETER_DESC
---

# D3D11_SIGNATURE_PARAMETER_DESC structure


## -description

Describes a shader signature.

## -struct-fields

### -field SemanticName

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

A per-parameter string that identifies how the data will be used. For more info, see <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics">Semantics</a>.

### -field SemanticIndex

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Semantic index that modifies the semantic. Used to differentiate different parameters that use the same semantic.

### -field Register

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The register that will contain this variable's data.

### -field SystemValueType

Type: <b><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_name">D3D_NAME</a></b>

A <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_name">D3D_NAME</a>-typed value that identifies a predefined string that determines the functionality of certain pipeline stages.

### -field ComponentType

Type: <b><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_register_component_type">D3D_REGISTER_COMPONENT_TYPE</a></b>

A <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_register_component_type">D3D_REGISTER_COMPONENT_TYPE</a>-typed value that identifies the per-component-data type that is stored in a register.  Each register can store up to four-components of data.

### -field Mask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

Mask which indicates which components of a register are used.

### -field ReadWriteMask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

Mask which indicates whether a given component is never written (if the signature is an output signature) or always read (if the signature is an input signature).

### -field Stream

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Indicates which stream the geometry shader is using for the signature parameter.

### -field MinPrecision

Type: <b><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_min_precision">D3D_MIN_PRECISION</a></b>

A <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_min_precision">D3D_MIN_PRECISION</a>-typed value that indicates the minimum desired interpolation precision. For more info, see <a href="/windows/desktop/direct3dhlsl/using-hlsl-minimum-precision">Using HLSL minimum precision</a>.

## -remarks

A shader can take n inputs and can produce m outputs. The order of the input (or output) parameters, their associated types, and any attached semantics make up the shader signature. Each shader has an input and an output signature.

When compiling a shader or an effect, some API calls validate shader signatures  That is, they compare the output signature of one shader (like a vertex shader) with the input signature of another shader (like a pixel shader). This ensures that a shader outputs data that is compatible with a downstream shader that is consuming that data. Compatible means that a shader signature is a exact-match subset of the preceding shader stage. Exact match means parameter types and semantics must exactly match. Subset means that a parameter that is not required by a downstream stage, does not need to include that parameter in its shader signature.

Get a shader-signature from a shader or an effect by calling APIs such as <a href="/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getinputparameterdesc">ID3D11ShaderReflection::GetInputParameterDesc</a>.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-shader-structures">Shader Structures</a>
