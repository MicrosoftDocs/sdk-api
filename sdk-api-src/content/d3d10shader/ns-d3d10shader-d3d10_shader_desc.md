---
UID: NS:d3d10shader._D3D10_SHADER_DESC
title: D3D10_SHADER_DESC (d3d10shader.h)
description: Describes a shader. (D3D10_SHADER_DESC)
helpviewer_keywords: ["4f0bd653-5cd1-26ff-b805-ecf9070b3990","D3D10_SHADER_DESC","D3D10_SHADER_DESC structure [Direct3D 10]","d3d10shader/D3D10_SHADER_DESC","direct3d10.d3d10_shader_desc"]
old-location: direct3d10\d3d10_shader_desc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_desc.htm
ms.date: 12/05/2018
ms.keywords: 4f0bd653-5cd1-26ff-b805-ecf9070b3990, D3D10_SHADER_DESC, D3D10_SHADER_DESC structure [Direct3D 10], d3d10shader/D3D10_SHADER_DESC, direct3d10.d3d10_shader_desc
req.header: d3d10shader.h
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
req.typenames: D3D10_SHADER_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D10_SHADER_DESC
 - d3d10shader/_D3D10_SHADER_DESC
 - D3D10_SHADER_DESC
 - d3d10shader/D3D10_SHADER_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10Shader.h
api_name:
 - D3D10_SHADER_DESC
---

## -description

Describes a shader.

## -struct-fields

### -field Version

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Shader version.

### -field Creator

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

The name of the originator of the shader.

### -field Flags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Shader compilation/parse flags.

### -field ConstantBuffers

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of shader-constant buffers.

### -field BoundResources

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of resource (textures and buffers) bound to a shader.

### -field InputParameters

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of parameters in the input signature.

### -field OutputParameters

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of parameters in the output signature.

### -field InstructionCount

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of intermediate-language instructions in the compiled shader.

### -field TempRegisterCount

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of temporary registers in the compiled shader.

### -field TempArrayCount

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of temporary arrays used.

### -field DefCount

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of constant defines.

### -field DclCount

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of declarations (input + output).

### -field TextureNormalInstructions

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of non-categorized texture instructions.

### -field TextureLoadInstructions

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of texture load instructions

### -field TextureCompInstructions

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of texture comparison instructions

### -field TextureBiasInstructions

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of texture bias instructions

### -field TextureGradientInstructions

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of texture gradient instructions.

### -field FloatInstructionCount

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of floating point arithmetic instructions used.

### -field IntInstructionCount

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of signed integer arithmetic instructions used.

### -field UintInstructionCount

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of unsigned integer arithmetic instructions used.

### -field StaticFlowControlCount

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of static flow control instructions used.

### -field DynamicFlowControlCount

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of dynamic flow control instructions used.

### -field MacroInstructionCount

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of macro instructions used.

### -field ArrayInstructionCount

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of array instructions used.

### -field CutInstructionCount

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of cut instructions used.

### -field EmitInstructionCount

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of emit instructions used.

### -field GSOutputTopology

Type: <b><a href="/previous-versions/windows/desktop/legacy/bb205334(v=vs.85)">D3D10_PRIMITIVE_TOPOLOGY</a></b>

Geometry shader output topology.

### -field GSMaxOutputVertexCount

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Geometry shader maximum output vertex count.

#### - BitwiseInstructionCount

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of bitwise operations.

#### - ConversionInstructionCount

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of conversion operations.

#### - MovInstructionCount

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of mov instructions.

#### - MovcInstructionCount

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of movc instructions.

## -remarks

A shader is written in HLSL and compiled into an intermediate language by the HLSL compiler. The shader description returns information about the compiled shader. Get a shader description by calling <a href="/windows/desktop/api/d3d10shader/nf-d3d10shader-id3d10shaderreflection-getdesc">ID3D10ShaderReflection::GetDesc</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-shader-structures">Shader Structures</a>
