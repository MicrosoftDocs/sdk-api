---
UID: NE:d3dcommon._D3D_SHADER_INPUT_FLAGS
title: "_D3D_SHADER_INPUT_FLAGS"
author: windows-sdk-content
description: These flags identify shader-input options.
old-location: direct3d10\d3d10_shader_input_flags.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_input_flags.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: D3D10_SHADER_INPUT_FLAGS, D3D10_SHADER_INPUT_FLAGS enumeration [Direct3D 10], D3D10_SIF_COMPARISON_SAMPLER, D3D10_SIF_FORCE_DWORD, D3D10_SIF_TEXTURE_COMPONENTS, D3D10_SIF_TEXTURE_COMPONENT_0, D3D10_SIF_TEXTURE_COMPONENT_1, D3D10_SIF_USERPACKED, D3D_SHADER_INPUT_FLAGS, LPD3D10_SHADER_INPUT_FLAGS, LPD3D10_SHADER_INPUT_FLAGS enumeration pointer [Direct3D 10], _D3D_SHADER_INPUT_FLAGS, d3d10shader/D3D10_SHADER_INPUT_FLAGS, d3d10shader/D3D10_SIF_COMPARISON_SAMPLER, d3d10shader/D3D10_SIF_FORCE_DWORD, d3d10shader/D3D10_SIF_TEXTURE_COMPONENTS, d3d10shader/D3D10_SIF_TEXTURE_COMPONENT_0, d3d10shader/D3D10_SIF_TEXTURE_COMPONENT_1, d3d10shader/D3D10_SIF_USERPACKED, d3d10shader/LPD3D10_SHADER_INPUT_FLAGS, d3dcommon/D3D10_SHADER_INPUT_FLAGS, d3dcommon/D3D10_SIF_COMPARISON_SAMPLER, d3dcommon/D3D10_SIF_FORCE_DWORD, d3dcommon/D3D10_SIF_TEXTURE_COMPONENTS, d3dcommon/D3D10_SIF_TEXTURE_COMPONENT_0, d3dcommon/D3D10_SIF_TEXTURE_COMPONENT_1, d3dcommon/D3D10_SIF_USERPACKED, d3dcommon/LPD3D10_SHADER_INPUT_FLAGS, direct3d10.d3d10_shader_input_flags, e5dc4758-0c9e-7c03-15ed-8af919236b2f
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: D3D_SHADER_INPUT_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10Shader.h
 - d3dcommon.h
api_name:
 - D3D10_SHADER_INPUT_FLAGS
product: Windows
targetos: Windows
req.lib: D3d9.lib
req.dll: 
req.irql: 
---

# _D3D_SHADER_INPUT_FLAGS enumeration


## -description


These flags identify shader-input options.


## -enum-fields




### -field D3D_SIF_USERPACKED


### -field D3D_SIF_COMPARISON_SAMPLER


### -field D3D_SIF_TEXTURE_COMPONENT_0


### -field D3D_SIF_TEXTURE_COMPONENT_1


### -field D3D_SIF_TEXTURE_COMPONENTS


### -field D3D_SIF_UNUSED


### -field D3D10_SIF_USERPACKED

Assign a shader input to a register based on the register assignment in the HLSL code (instead of letting the compiler choose the register).


### -field D3D10_SIF_COMPARISON_SAMPLER

Use a comparison sampler, which uses the <a href="https://msdn.microsoft.com/e21894c4-e8c5-4c3d-92c1-727964f8fd94">SampleCmp (DirectX HLSL Texture Object)</a> and <a href="https://msdn.microsoft.com/cecfc5e8-d293-4e0e-a3f4-b23f84843b7d">SampleCmpLevelZero (DirectX HLSL Texture Object)</a> sampling functions.


### -field D3D10_SIF_TEXTURE_COMPONENT_0

A 2-bit value for encoding texture components.


### -field D3D10_SIF_TEXTURE_COMPONENT_1

A 2-bit value for encoding texture components.


### -field D3D10_SIF_TEXTURE_COMPONENTS

A 2-bit value for encoding texture components.


### -field D3D_SIF_FORCE_DWORD




#### - D3D10_SIF_FORCE_DWORD

This value is not used by a programmer; it exists to force the enumeration to compile to 32 bits.


## -remarks



These flags are used in a shader-input-signature description (see <a href="https://msdn.microsoft.com/8929f7d4-6fd0-4b48-b1d8-0b089d4c730d">D3D10_SHADER_INPUT_BIND_DESC</a>).

The <b>D3D10_SHADER_INPUT_FLAGS</b>     enumeration is type defined in the  D3D10shader.h header file as a <a href="https://msdn.microsoft.com/3c79331e-73c0-42d7-9948-6ac2671a4ab5">D3D_SHADER_INPUT_FLAGS</a> enumeration, which is fully defined in the  D3DCommon.h header file.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
typedef D3D_SHADER_INPUT_FLAGS D3D10_SHADER_INPUT_FLAGS;</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/8d2b758b-cc2a-43ad-bf26-51674d4b5129">Shader Enumerations</a>
 

 

