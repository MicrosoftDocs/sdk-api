---
UID: NS:d3d12shader._D3D12_SIGNATURE_PARAMETER_DESC
title: D3D12_SIGNATURE_PARAMETER_DESC (d3d12shader.h)
description: Describes a shader signature. (D3D12_SIGNATURE_PARAMETER_DESC)
helpviewer_keywords: ["D3D12_SIGNATURE_PARAMETER_DESC","D3D12_SIGNATURE_PARAMETER_DESC structure","d3d12shader/D3D12_SIGNATURE_PARAMETER_DESC","direct3d12.d3d12_signature_parameter_desc"]
old-location: direct3d12\d3d12_signature_parameter_desc.htm
tech.root: direct3d12
ms.assetid: FDD227A5-FFB9-46E3-B7F7-BECE785ECD7C
ms.date: 12/05/2018
ms.keywords: D3D12_SIGNATURE_PARAMETER_DESC, D3D12_SIGNATURE_PARAMETER_DESC structure, d3d12shader/D3D12_SIGNATURE_PARAMETER_DESC, direct3d12.d3d12_signature_parameter_desc
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
req.typenames: D3D12_SIGNATURE_PARAMETER_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D12_SIGNATURE_PARAMETER_DESC
 - d3d12shader/_D3D12_SIGNATURE_PARAMETER_DESC
 - D3D12_SIGNATURE_PARAMETER_DESC
 - d3d12shader/D3D12_SIGNATURE_PARAMETER_DESC
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
 - D3D12_SIGNATURE_PARAMETER_DESC
---

# D3D12_SIGNATURE_PARAMETER_DESC structure


## -description

Describes a shader signature.

## -struct-fields

### -field SemanticName

A per-parameter string that identifies how the data will be used. For more info, see <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics">Semantics</a>.

### -field SemanticIndex

Semantic index that modifies the semantic. Used to differentiate different parameters that use the same semantic.

### -field Register

The register that will contain this variable's data.

### -field SystemValueType

A <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_name">D3D_NAME</a>-typed value that identifies a predefined string that determines the functionality of certain pipeline stages.

### -field ComponentType

A <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_register_component_type">D3D_REGISTER_COMPONENT_TYPE</a>-typed value that identifies the per-component-data type that is stored in a register.  Each register can store up to four-components of data.

### -field Mask

Mask which indicates which components of a register are used.

### -field ReadWriteMask

Mask which indicates whether a given component is never written (if the signature is an output signature) or always read (if the signature is an input signature).

### -field Stream

Indicates which stream the geometry shader is using for the signature parameter.

### -field MinPrecision

A <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_min_precision">D3D_MIN_PRECISION</a>-typed value that indicates the minimum desired interpolation precision. For more info, see <a href="/windows/desktop/direct3dhlsl/using-hlsl-minimum-precision">Using HLSL minimum precision</a>.

## -remarks

A shader can take n inputs and can produce m outputs. The order of the input (or output) parameters, their associated types, and any attached semantics make up the shader signature. Each shader has an input and an output signature.
        

When compiling a shader or an effect, some API calls validate shader signatures  That is, they compare the output signature of one shader (like a vertex shader) with the input signature of another shader (like a pixel shader). This ensures that a shader outputs data that is compatible with a downstream shader that is consuming that data. Compatible means that a shader signature is a exact-match subset of the preceding shader stage. Exact match means parameter types and semantics must exactly match. Subset means that a parameter that is not required by a downstream stage, does not need to include that parameter in its shader signature.
        

Get a shader-signature from a shader or an effect by calling APIs such as <a href="/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflection-getinputparameterdesc">ID3D12ShaderReflection::GetInputParameterDesc</a>.

## -see-also

<a href="/windows/desktop/direct3d12/d3d12-graphics-reference-shader-structures">Shader Structures</a>
