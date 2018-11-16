---
UID: NS:d3d11shader._D3D11_SHADER_DESC
title: "_D3D11_SHADER_DESC"
author: windows-sdk-content
description: Describes a shader.
old-location: direct3d11\d3d11_shader_desc.htm
tech.root: direct3d11
ms.assetid: 25c8f773-e319-4ba1-b332-d45b8323e8c8
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 60a58f35-71f5-ec69-15ed-a355dd62d5f7, D3D11_SHADER_DESC, D3D11_SHADER_DESC structure [Direct3D 11], _D3D11_SHADER_DESC, d3d11shader/D3D11_SHADER_DESC, direct3d11.d3d11_shader_desc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11Shader.h
api_name:
 - D3D11_SHADER_DESC
product: Windows
targetos: Windows
req.typenames: D3D11_SHADER_DESC
req.redist: 
---

# _D3D11_SHADER_DESC structure


## -description


Describes a shader.


## -struct-fields




### -field Version

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Shader version.


### -field Creator

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">LPCSTR</a></b>

The name of the originator of the shader.


### -field Flags

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Shader compilation/parse flags.


### -field ConstantBuffers

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The number of shader-constant buffers.


### -field BoundResources

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The number of resource (textures and buffers) bound to a shader.


### -field InputParameters

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The number of parameters in the input signature.


### -field OutputParameters

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The number of parameters in the output signature.


### -field InstructionCount

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The number of intermediate-language instructions in the compiled shader.


### -field TempRegisterCount

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The number of temporary registers in the compiled shader.


### -field TempArrayCount

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of temporary arrays used.


### -field DefCount

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of constant defines.


### -field DclCount

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of declarations (input + output).


### -field TextureNormalInstructions

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of non-categorized texture instructions.


### -field TextureLoadInstructions

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of texture load instructions


### -field TextureCompInstructions

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of texture comparison instructions


### -field TextureBiasInstructions

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of texture bias instructions


### -field TextureGradientInstructions

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of texture gradient instructions.


### -field FloatInstructionCount

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of floating point arithmetic instructions used.


### -field IntInstructionCount

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of signed integer arithmetic instructions used.


### -field UintInstructionCount

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of unsigned integer arithmetic instructions used.


### -field StaticFlowControlCount

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of static flow control instructions used.


### -field DynamicFlowControlCount

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of dynamic flow control instructions used.


### -field MacroInstructionCount

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of macro instructions used.


### -field ArrayInstructionCount

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of array instructions used.


### -field CutInstructionCount

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of cut instructions used.


### -field EmitInstructionCount

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of emit instructions used.


### -field GSOutputTopology

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff728726(v=VS.85).aspx">D3D_PRIMITIVE_TOPOLOGY</a></b>

The <a href="https://msdn.microsoft.com/en-us/library/Ff728726(v=VS.85).aspx">D3D_PRIMITIVE_TOPOLOGY</a>-typed value that represents the geometry shader output topology.


### -field GSMaxOutputVertexCount

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Geometry shader maximum output vertex count.


### -field InputPrimitive

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff728725(v=VS.85).aspx">D3D_PRIMITIVE</a></b>

The <a href="https://msdn.microsoft.com/en-us/library/Ff728725(v=VS.85).aspx">D3D_PRIMITIVE</a>-typed value that represents the input primitive for a  geometry shader or hull shader.


### -field PatchConstantParameters

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of parameters in the patch-constant signature.


### -field cGSInstanceCount

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of geometry shader instances.


### -field cControlPoints

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of control points in the hull shader and domain shader.


### -field HSOutputPrimitive

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff728738(v=VS.85).aspx">D3D_TESSELLATOR_OUTPUT_PRIMITIVE</a></b>

The <a href="https://msdn.microsoft.com/en-us/library/Ff728738(v=VS.85).aspx">D3D_TESSELLATOR_OUTPUT_PRIMITIVE</a>-typed value that represents the tessellator output-primitive type.


### -field HSPartitioning

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff728739(v=VS.85).aspx">D3D_TESSELLATOR_PARTITIONING</a></b>

The <a href="https://msdn.microsoft.com/en-us/library/Ff728739(v=VS.85).aspx">D3D_TESSELLATOR_PARTITIONING</a>-typed value that represents the tessellator partitioning mode.


### -field TessellatorDomain

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff728737(v=VS.85).aspx">D3D_TESSELLATOR_DOMAIN</a></b>

The <a href="https://msdn.microsoft.com/en-us/library/Ff728737(v=VS.85).aspx">D3D_TESSELLATOR_DOMAIN</a>-typed value that represents the tessellator domain.


### -field cBarrierInstructions

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of barrier instructions in a compute shader.


### -field cInterlockedInstructions

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of interlocked instructions in a compute shader.


### -field cTextureStoreInstructions

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of texture writes in a compute shader.


## -remarks



A shader is written in HLSL and compiled into an intermediate language by the HLSL compiler. The shader description returns information about the compiled shader. Get a shader description by calling <a href="https://msdn.microsoft.com/en-us/library/Ff476615(v=VS.85).aspx">ID3D11ShaderReflection::GetDesc</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476176(v=VS.85).aspx">Shader Structures</a>
 

 

