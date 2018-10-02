---
UID: NS:d3d10shader._D3D10_SHADER_DESC
title: "_D3D10_SHADER_DESC"
author: windows-sdk-content
description: Describes a shader.
old-location: direct3d10\d3d10_shader_desc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_desc.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 4f0bd653-5cd1-26ff-b805-ecf9070b3990, D3D10_SHADER_DESC, D3D10_SHADER_DESC structure [Direct3D 10], _D3D10_SHADER_DESC, d3d10shader/D3D10_SHADER_DESC, direct3d10.d3d10_shader_desc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10Shader.h
api_name:
 - D3D10_SHADER_DESC
product: Windows
targetos: Windows
req.typenames: D3D10_SHADER_DESC
req.redist: 
---

# _D3D10_SHADER_DESC structure


## -description


Describes a shader.


## -struct-fields




### -field Version

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Shader version.


### -field Creator

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The name of the originator of the shader.


### -field Flags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Shader compilation/parse flags.


### -field ConstantBuffers

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of shader-constant buffers.


### -field BoundResources

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of resource (textures and buffers) bound to a shader.


### -field InputParameters

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of parameters in the input signature.


### -field OutputParameters

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of parameters in the output signature.


### -field InstructionCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of intermediate-language instructions in the compiled shader.


### -field TempRegisterCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of temporary registers in the compiled shader.


### -field TempArrayCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of temporary arrays used.


### -field DefCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of constant defines.


### -field DclCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of declarations (input + output).


### -field TextureNormalInstructions

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of non-categorized texture instructions.


### -field TextureLoadInstructions

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of texture load instructions


### -field TextureCompInstructions

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of texture comparison instructions


### -field TextureBiasInstructions

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of texture bias instructions


### -field TextureGradientInstructions

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of texture gradient instructions.


### -field FloatInstructionCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of floating point arithmetic instructions used.


### -field IntInstructionCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of signed integer arithmetic instructions used.


### -field UintInstructionCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of unsigned integer arithmetic instructions used.


### -field StaticFlowControlCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of static flow control instructions used.


### -field DynamicFlowControlCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of dynamic flow control instructions used.


### -field MacroInstructionCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of macro instructions used.


### -field ArrayInstructionCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of array instructions used.


### -field CutInstructionCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of cut instructions used.


### -field EmitInstructionCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of emit instructions used.


### -field GSOutputTopology

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb205334(v=VS.85).aspx">D3D10_PRIMITIVE_TOPOLOGY</a></b>

Geometry shader output topology.


### -field GSMaxOutputVertexCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Geometry shader maximum output vertex count.


#### - BitwiseInstructionCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of bitwise operations.


#### - ConversionInstructionCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of conversion operations.


#### - MovInstructionCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of mov instructions.


#### - MovcInstructionCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of movc instructions.


## -remarks



A shader is written in HLSL and compiled into an intermediate language by the HLSL compiler. The shader description returns information about the compiled shader. Get a shader description by calling <a href="https://msdn.microsoft.com/en-us/library/Bb173850(v=VS.85).aspx">ID3D10ShaderReflection::GetDesc</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205159(v=VS.85).aspx">Shader Structures</a>
 

 

