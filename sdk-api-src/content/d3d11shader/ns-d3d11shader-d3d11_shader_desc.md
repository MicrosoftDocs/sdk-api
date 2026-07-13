---
UID: NS:d3d11shader._D3D11_SHADER_DESC
title: D3D11_SHADER_DESC (d3d11shader.h)
description: Describes a shader. (D3D11_SHADER_DESC)
helpviewer_keywords: ["60a58f35-71f5-ec69-15ed-a355dd62d5f7","D3D11_SHADER_DESC","D3D11_SHADER_DESC structure [Direct3D 11]","d3d11shader/D3D11_SHADER_DESC","direct3d11.d3d11_shader_desc"]
old-location: direct3d11\d3d11_shader_desc.htm
tech.root: direct3d11
ms.assetid: 25c8f773-e319-4ba1-b332-d45b8323e8c8
ms.date: 12/05/2018
ms.keywords: 60a58f35-71f5-ec69-15ed-a355dd62d5f7, D3D11_SHADER_DESC, D3D11_SHADER_DESC structure [Direct3D 11], d3d11shader/D3D11_SHADER_DESC, direct3d11.d3d11_shader_desc
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
req.typenames: D3D11_SHADER_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D11_SHADER_DESC
 - d3d11shader/_D3D11_SHADER_DESC
 - D3D11_SHADER_DESC
 - d3d11shader/D3D11_SHADER_DESC
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
 - D3D11_SHADER_DESC
---

# D3D11_SHADER_DESC structure


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

Type: <b><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology">D3D_PRIMITIVE_TOPOLOGY</a></b>

The <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology">D3D_PRIMITIVE_TOPOLOGY</a>-typed value that represents the geometry shader output topology.

### -field GSMaxOutputVertexCount

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Geometry shader maximum output vertex count.

### -field InputPrimitive

Type: <b><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive">D3D_PRIMITIVE</a></b>

The <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive">D3D_PRIMITIVE</a>-typed value that represents the input primitive for a  geometry shader or hull shader.

### -field PatchConstantParameters

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of parameters in the patch-constant signature.

### -field cGSInstanceCount

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of geometry shader instances.

### -field cControlPoints

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of control points in the hull shader and domain shader.

### -field HSOutputPrimitive

Type: <b><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_tessellator_output_primitive">D3D_TESSELLATOR_OUTPUT_PRIMITIVE</a></b>

The <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_tessellator_output_primitive">D3D_TESSELLATOR_OUTPUT_PRIMITIVE</a>-typed value that represents the tessellator output-primitive type.

### -field HSPartitioning

Type: <b><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_tessellator_partitioning">D3D_TESSELLATOR_PARTITIONING</a></b>

The <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_tessellator_partitioning">D3D_TESSELLATOR_PARTITIONING</a>-typed value that represents the tessellator partitioning mode.

### -field TessellatorDomain

Type: <b><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_tessellator_domain">D3D_TESSELLATOR_DOMAIN</a></b>

The <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_tessellator_domain">D3D_TESSELLATOR_DOMAIN</a>-typed value that represents the tessellator domain.

### -field cBarrierInstructions

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of barrier instructions in a compute shader.

### -field cInterlockedInstructions

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of interlocked instructions in a compute shader.

### -field cTextureStoreInstructions

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of texture writes in a compute shader.

## -remarks

A shader is written in HLSL and compiled into an intermediate language by the HLSL compiler. The shader description returns information about the compiled shader. Get a shader description by calling <a href="/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getdesc">ID3D11ShaderReflection::GetDesc</a>.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-shader-structures">Shader Structures</a>
