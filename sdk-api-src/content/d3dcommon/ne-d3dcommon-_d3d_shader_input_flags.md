---
UID: NE:d3dcommon._D3D_SHADER_INPUT_FLAGS
title: "_D3D_SHADER_INPUT_FLAGS"
author: windows-sdk-content
description: Values that identify shader-input options.
old-location: direct3d11\d3d_shader_input_flags.htm
old-project: direct3d11
ms.assetid: 3c79331e-73c0-42d7-9948-6ac2671a4ab5
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: D3D10_SIF_COMPARISON_SAMPLER, D3D10_SIF_TEXTURE_COMPONENTS, D3D10_SIF_TEXTURE_COMPONENT_0, D3D10_SIF_TEXTURE_COMPONENT_1, D3D10_SIF_USERPACKED, D3D_SHADER_INPUT_FLAGS, D3D_SHADER_INPUT_FLAGS enumeration [Direct3D 11], D3D_SIF_COMPARISON_SAMPLER, D3D_SIF_FORCE_DWORD, D3D_SIF_TEXTURE_COMPONENTS, D3D_SIF_TEXTURE_COMPONENT_0, D3D_SIF_TEXTURE_COMPONENT_1, D3D_SIF_UNUSED, D3D_SIF_USERPACKED, _D3D_SHADER_INPUT_FLAGS, d3dcommon/D3D10_SIF_COMPARISON_SAMPLER, d3dcommon/D3D10_SIF_TEXTURE_COMPONENTS, d3dcommon/D3D10_SIF_TEXTURE_COMPONENT_0, d3dcommon/D3D10_SIF_TEXTURE_COMPONENT_1, d3dcommon/D3D10_SIF_USERPACKED, d3dcommon/D3D_SHADER_INPUT_FLAGS, d3dcommon/D3D_SIF_COMPARISON_SAMPLER, d3dcommon/D3D_SIF_FORCE_DWORD, d3dcommon/D3D_SIF_TEXTURE_COMPONENTS, d3dcommon/D3D_SIF_TEXTURE_COMPONENT_0, d3dcommon/D3D_SIF_TEXTURE_COMPONENT_1, d3dcommon/D3D_SIF_UNUSED, d3dcommon/D3D_SIF_USERPACKED, direct3d11.d3d_shader_input_flags
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
 - D3DCommon.h
api_name:
 - D3D_SHADER_INPUT_FLAGS
product: Windows
targetos: Windows
req.lib: D3d9.lib
req.dll: 
req.irql: 
---

# _D3D_SHADER_INPUT_FLAGS enumeration


## -description


Values that identify shader-input options.


## -enum-fields




### -field D3D_SIF_USERPACKED


            Assign a shader input to a register based on the register assignment in the HLSL code (instead of letting the compiler choose the register).
          


### -field D3D_SIF_COMPARISON_SAMPLER


            Use a comparison sampler, which uses the <a href="https://msdn.microsoft.com/library/Bb509696(v=VS.85).aspx">SampleCmp (DirectX HLSL Texture Object)</a> and <a href="https://msdn.microsoft.com/library/Bb509697(v=VS.85).aspx">SampleCmpLevelZero (DirectX HLSL Texture Object)</a> sampling functions.
          


### -field D3D_SIF_TEXTURE_COMPONENT_0


            A 2-bit value for encoding texture components.
          


### -field D3D_SIF_TEXTURE_COMPONENT_1


            A 2-bit value for encoding texture components.
          


### -field D3D_SIF_TEXTURE_COMPONENTS


            A 2-bit value for encoding texture components.
          


### -field D3D_SIF_UNUSED


            This value is reserved.
          


### -field D3D10_SIF_USERPACKED


            Assign a shader input to a register based on the register assignment in the HLSL code (instead of letting the compiler choose the register).
          


### -field D3D10_SIF_COMPARISON_SAMPLER


            Use a comparison sampler, which uses the <a href="https://msdn.microsoft.com/library/Bb509696(v=VS.85).aspx">SampleCmp (DirectX HLSL Texture Object)</a> and <a href="https://msdn.microsoft.com/library/Bb509697(v=VS.85).aspx">SampleCmpLevelZero (DirectX HLSL Texture Object)</a> sampling functions.
          


### -field D3D10_SIF_TEXTURE_COMPONENT_0


            A 2-bit value for encoding texture components.
          


### -field D3D10_SIF_TEXTURE_COMPONENT_1


            A 2-bit value for encoding texture components.
          


### -field D3D10_SIF_TEXTURE_COMPONENTS


            A 2-bit value for encoding texture components.
          


### -field D3D_SIF_FORCE_DWORD


            Forces the enumeration to compile to 32 bits.
            This value is not used directly by titles.
          


## -remarks



<b>D3D_SHADER_INPUT_FLAGS</b>-typed values are specified in
          the <b>uFlags</b> member of the <a href="https://msdn.microsoft.com/384ad8f8-0991-4cd2-bb3d-76b8338686da">D3D11_SHADER_INPUT_BIND_DESC</a> structure.
        




## -see-also




<a href="https://msdn.microsoft.com/002154d5-74a6-48fb-b55f-8687e4505fc7">Common Version Enumerations</a>
 

 

