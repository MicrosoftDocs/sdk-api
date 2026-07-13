---
UID: NS:d3d12shader._D3D12_SHADER_DESC
title: D3D12_SHADER_DESC (d3d12shader.h)
description: Describes a shader. (D3D12_SHADER_DESC)
helpviewer_keywords: ["D3D12_SHADER_DESC","D3D12_SHADER_DESC structure","d3d12shader/D3D12_SHADER_DESC","direct3d12.d3d12_shader_desc"]
old-location: direct3d12\d3d12_shader_desc.htm
tech.root: direct3d12
ms.assetid: FE989434-B1B6-48F3-8F95-64B1E7C988F5
ms.date: 12/05/2018
ms.keywords: D3D12_SHADER_DESC, D3D12_SHADER_DESC structure, d3d12shader/D3D12_SHADER_DESC, direct3d12.d3d12_shader_desc
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
req.typenames: D3D12_SHADER_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D12_SHADER_DESC
 - d3d12shader/_D3D12_SHADER_DESC
 - D3D12_SHADER_DESC
 - d3d12shader/D3D12_SHADER_DESC
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
 - D3D12_SHADER_DESC
---

# D3D12_SHADER_DESC structure


## -description

Describes a shader.

## -struct-fields

### -field Version

The Shader version, as an encoded UINT that corresponds to a shader model, such as "ps_5_0".
            <b>Version</b> describes the program type, a major version number, and a minor version number.
            The program type is a <a href="/windows/desktop/api/d3d12shader/ne-d3d12shader-d3d12_shader_version_type">D3D12_SHADER_VERSION_TYPE</a> enumeration constant.
            <b>Version</b> is decoded in the following way:
            

<ul>
<li>Program type = (Version &amp; 0xFFFF0000) &gt;&gt; 16</li>
<li>Major version = (Version &amp; 0x000000F0) &gt;&gt; 4</li>
<li>Minor version = (Version &amp; 0x0000000F)</li>
</ul>

### -field Creator

The name of the originator of the shader.

### -field Flags

Shader compilation/parse flags.

### -field ConstantBuffers

The number of shader-constant buffers.

### -field BoundResources

The number of resource (textures and buffers) bound to a shader.

### -field InputParameters

The number of parameters in the input signature.

### -field OutputParameters

The number of parameters in the output signature.

### -field InstructionCount

The number of intermediate-language instructions in the compiled shader.

### -field TempRegisterCount

The number of temporary registers in the compiled shader.

### -field TempArrayCount

Number of temporary arrays used.

### -field DefCount

Number of constant defines.

### -field DclCount

Number of declarations (input + output).

### -field TextureNormalInstructions

Number of non-categorized texture instructions.

### -field TextureLoadInstructions

Number of texture load instructions

### -field TextureCompInstructions

Number of texture comparison instructions

### -field TextureBiasInstructions

Number of texture bias instructions

### -field TextureGradientInstructions

Number of texture gradient instructions.

### -field FloatInstructionCount

Number of floating point arithmetic instructions used.

### -field IntInstructionCount

Number of signed integer arithmetic instructions used.

### -field UintInstructionCount

Number of unsigned integer arithmetic instructions used.

### -field StaticFlowControlCount

Number of static flow control instructions used.

### -field DynamicFlowControlCount

Number of dynamic flow control instructions used.

### -field MacroInstructionCount

Number of macro instructions used.

### -field ArrayInstructionCount

Number of array instructions used.

### -field CutInstructionCount

Number of cut instructions used.

### -field EmitInstructionCount

Number of emit instructions used.

### -field GSOutputTopology

The <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology">D3D_PRIMITIVE_TOPOLOGY</a>-typed value that represents the geometry shader output topology.

### -field GSMaxOutputVertexCount

Geometry shader maximum output vertex count.

### -field InputPrimitive

The <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive">D3D_PRIMITIVE</a>-typed value that represents the input primitive for a  geometry shader or hull shader.

### -field PatchConstantParameters

Number of parameters in the patch-constant signature.

### -field cGSInstanceCount

Number of geometry shader instances.

### -field cControlPoints

Number of control points in the hull shader and domain shader.

### -field HSOutputPrimitive

The <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_tessellator_output_primitive">D3D_TESSELLATOR_OUTPUT_PRIMITIVE</a>-typed value that represents the tessellator output-primitive type.

### -field HSPartitioning

The <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_tessellator_partitioning">D3D_TESSELLATOR_PARTITIONING</a>-typed value that represents the tessellator partitioning mode.

### -field TessellatorDomain

The <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_tessellator_domain">D3D_TESSELLATOR_DOMAIN</a>-typed value that represents the tessellator domain.

### -field cBarrierInstructions

Number of barrier instructions in a compute shader.

### -field cInterlockedInstructions

Number of interlocked instructions in a compute shader.

### -field cTextureStoreInstructions

Number of texture writes in a compute shader.

## -remarks

A shader is written in HLSL and compiled into an intermediate language by the HLSL compiler.
        The shader description returns information about the compiled shader.
        To get a shader description, call <a href="/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflection-getdesc">ID3D12ShaderReflection::GetDesc</a>.

## -see-also

<a href="/windows/desktop/direct3d12/d3d12-graphics-reference-shader-structures">Shader Structures</a>
