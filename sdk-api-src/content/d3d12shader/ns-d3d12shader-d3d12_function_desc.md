---
UID: NS:d3d12shader._D3D12_FUNCTION_DESC
title: D3D12_FUNCTION_DESC (d3d12shader.h)
description: Describes a function. (D3D12_FUNCTION_DESC)
helpviewer_keywords: ["D3D12_FUNCTION_DESC","D3D12_FUNCTION_DESC structure","d3d12shader/D3D12_FUNCTION_DESC","direct3d12.d3d12_function_desc"]
old-location: direct3d12\d3d12_function_desc.htm
tech.root: direct3d12
ms.assetid: 6FF99C49-B5B1-4969-86E2-828D584D1EA9
ms.date: 12/05/2018
ms.keywords: D3D12_FUNCTION_DESC, D3D12_FUNCTION_DESC structure, d3d12shader/D3D12_FUNCTION_DESC, direct3d12.d3d12_function_desc
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
req.typenames: D3D12_FUNCTION_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D12_FUNCTION_DESC
 - d3d12shader/_D3D12_FUNCTION_DESC
 - D3D12_FUNCTION_DESC
 - d3d12shader/D3D12_FUNCTION_DESC
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
 - D3D12_FUNCTION_DESC
---

# D3D12_FUNCTION_DESC structure


## -description

Describes a function.

## -struct-fields

### -field Version

The shader version.
            See also <a href="/windows/desktop/api/d3d12shader/ne-d3d12shader-d3d12_shader_version_type">D3D12_SHADER_VERSION_TYPE</a>.

### -field Creator

The name of the originator of the function.

### -field Flags

A combination of <a href="/windows/desktop/direct3dhlsl/d3dcompile-constants">D3DCOMPILE Constants</a> that are combined by using a bitwise OR operation. The resulting value specifies shader compilation and parsing.

### -field ConstantBuffers

The number of constant buffers for the function.

### -field BoundResources

The number of bound resources for the function.

### -field InstructionCount

The number of emitted instructions for the function.

### -field TempRegisterCount

The number of temporary registers used by the function.

### -field TempArrayCount

The number of temporary arrays used by the function.

### -field DefCount

The number of constant defines for the function.

### -field DclCount

The number of declarations (input + output) for the function.

### -field TextureNormalInstructions

The number of non-categorized texture instructions for the function.

### -field TextureLoadInstructions

The number of texture load instructions for the function.

### -field TextureCompInstructions

The number of texture comparison instructions for the function.

### -field TextureBiasInstructions

The number of texture bias instructions for the function.

### -field TextureGradientInstructions

The number of texture gradient instructions for the function.

### -field FloatInstructionCount

The number of floating point arithmetic instructions used by the function.

### -field IntInstructionCount

The number of signed integer arithmetic instructions used by the function.

### -field UintInstructionCount

The number of unsigned integer arithmetic instructions used by the function.

### -field StaticFlowControlCount

The number of static flow control instructions used by the function.

### -field DynamicFlowControlCount

The number of dynamic flow control instructions used by the function.

### -field MacroInstructionCount

The number of macro instructions used by the function.

### -field ArrayInstructionCount

The number of array instructions used by the function.

### -field MovInstructionCount

The number of mov instructions used by the function.

### -field MovcInstructionCount

The number of movc instructions used by the function.

### -field ConversionInstructionCount

The number of type conversion instructions used by the function.

### -field BitwiseInstructionCount

The number of bitwise arithmetic instructions used by the function.

### -field MinFeatureLevel

A <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level">D3D_FEATURE_LEVEL</a>-typed value that specifies the minimum Direct3D feature level target of the function byte code.

### -field RequiredFeatureFlags

A value that contains a combination of one or more shader requirements flags; each flag specifies a requirement of the shader. A default value of 0 means there are no requirements. For a list of values, see <a href="/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflection-getrequiresflags">ID3D12ShaderReflection::GetRequiresFlags</a>.

### -field Name

The name of the function.

### -field FunctionParameterCount

The number of logical parameters in the function signature, not including the return value.

### -field HasReturn

Indicates whether the function returns a value. <b>TRUE</b> indicates it returns a value; otherwise, <b>FALSE</b> (it is a subroutine).

### -field Has10Level9VertexShader

Indicates whether there is a Direct3D 10Level9 vertex shader blob. <b>TRUE</b> indicates there is a 10Level9 vertex shader blob; otherwise, <b>FALSE</b>.

### -field Has10Level9PixelShader

Indicates whether there is a Direct3D 10Level9 pixel shader blob. <b>TRUE</b> indicates there is a 10Level9 pixel shader blob; otherwise, <b>FALSE</b>.

## -remarks

This structure is returned by <a href="/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12functionreflection-getdesc">ID3D12FunctionReflection::GetDesc</a>.

## -see-also

<a href="/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12functionreflection-getdesc">ID3D12FunctionReflection::GetDesc</a>



<a href="/windows/desktop/direct3d12/d3d12-graphics-reference-shader-structures">Shader Structures</a>
