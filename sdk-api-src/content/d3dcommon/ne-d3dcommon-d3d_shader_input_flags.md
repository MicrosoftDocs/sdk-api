---
UID: NE:d3dcommon._D3D_SHADER_INPUT_FLAGS
title: D3D_SHADER_INPUT_FLAGS (d3dcommon.h)
description: Values that identify shader-input options.
helpviewer_keywords: ["D3D10_SIF_COMPARISON_SAMPLER","D3D10_SIF_TEXTURE_COMPONENTS","D3D10_SIF_TEXTURE_COMPONENT_0","D3D10_SIF_TEXTURE_COMPONENT_1","D3D10_SIF_USERPACKED","D3D_SHADER_INPUT_FLAGS","D3D_SHADER_INPUT_FLAGS enumeration [Direct3D 11]","D3D_SIF_COMPARISON_SAMPLER","D3D_SIF_FORCE_DWORD","D3D_SIF_TEXTURE_COMPONENTS","D3D_SIF_TEXTURE_COMPONENT_0","D3D_SIF_TEXTURE_COMPONENT_1","D3D_SIF_UNUSED","D3D_SIF_USERPACKED","d3dcommon/D3D10_SIF_COMPARISON_SAMPLER","d3dcommon/D3D10_SIF_TEXTURE_COMPONENTS","d3dcommon/D3D10_SIF_TEXTURE_COMPONENT_0","d3dcommon/D3D10_SIF_TEXTURE_COMPONENT_1","d3dcommon/D3D10_SIF_USERPACKED","d3dcommon/D3D_SHADER_INPUT_FLAGS","d3dcommon/D3D_SIF_COMPARISON_SAMPLER","d3dcommon/D3D_SIF_FORCE_DWORD","d3dcommon/D3D_SIF_TEXTURE_COMPONENTS","d3dcommon/D3D_SIF_TEXTURE_COMPONENT_0","d3dcommon/D3D_SIF_TEXTURE_COMPONENT_1","d3dcommon/D3D_SIF_UNUSED","d3dcommon/D3D_SIF_USERPACKED","direct3d11.d3d_shader_input_flags"]
old-location: direct3d11\d3d_shader_input_flags.htm
tech.root: direct3d11
ms.assetid: 3c79331e-73c0-42d7-9948-6ac2671a4ab5
ms.date: 12/05/2018
ms.keywords: D3D10_SIF_COMPARISON_SAMPLER, D3D10_SIF_TEXTURE_COMPONENTS, D3D10_SIF_TEXTURE_COMPONENT_0, D3D10_SIF_TEXTURE_COMPONENT_1, D3D10_SIF_USERPACKED, D3D_SHADER_INPUT_FLAGS, D3D_SHADER_INPUT_FLAGS enumeration [Direct3D 11], D3D_SIF_COMPARISON_SAMPLER, D3D_SIF_FORCE_DWORD, D3D_SIF_TEXTURE_COMPONENTS, D3D_SIF_TEXTURE_COMPONENT_0, D3D_SIF_TEXTURE_COMPONENT_1, D3D_SIF_UNUSED, D3D_SIF_USERPACKED, d3dcommon/D3D10_SIF_COMPARISON_SAMPLER, d3dcommon/D3D10_SIF_TEXTURE_COMPONENTS, d3dcommon/D3D10_SIF_TEXTURE_COMPONENT_0, d3dcommon/D3D10_SIF_TEXTURE_COMPONENT_1, d3dcommon/D3D10_SIF_USERPACKED, d3dcommon/D3D_SHADER_INPUT_FLAGS, d3dcommon/D3D_SIF_COMPARISON_SAMPLER, d3dcommon/D3D_SIF_FORCE_DWORD, d3dcommon/D3D_SIF_TEXTURE_COMPONENTS, d3dcommon/D3D_SIF_TEXTURE_COMPONENT_0, d3dcommon/D3D_SIF_TEXTURE_COMPONENT_1, d3dcommon/D3D_SIF_UNUSED, d3dcommon/D3D_SIF_USERPACKED, direct3d11.d3d_shader_input_flags
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D_SHADER_INPUT_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D_SHADER_INPUT_FLAGS
 - d3dcommon/_D3D_SHADER_INPUT_FLAGS
 - D3D_SHADER_INPUT_FLAGS
 - d3dcommon/D3D_SHADER_INPUT_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3DCommon.h
api_name:
 - D3D_SHADER_INPUT_FLAGS
---

# D3D_SHADER_INPUT_FLAGS enumeration


## -description

Values that identify shader-input options.

> [!NOTE]
> For programming with Direct3D 10, this API has a type alias that begins `D3D10_` instead of `D3D_`. These Direct3D 10 type aliases are defined in `d3d10.h`, `d3d10misc.h`, and `d3d10shader.h`.

## -enum-fields

### -field D3D_SIF_USERPACKED:0x1

Assign a shader input to a register based on the register assignment in the HLSL code (instead of letting the compiler choose the register).

### -field D3D_SIF_COMPARISON_SAMPLER:0x2

Use a comparison sampler, which uses the <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-samplecmp">SampleCmp (DirectX HLSL Texture Object)</a> and <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-samplecmplevelzero">SampleCmpLevelZero (DirectX HLSL Texture Object)</a> sampling functions.

### -field D3D_SIF_TEXTURE_COMPONENT_0:0x4

A 2-bit value for encoding texture components.

### -field D3D_SIF_TEXTURE_COMPONENT_1:0x8

A 2-bit value for encoding texture components.

### -field D3D_SIF_TEXTURE_COMPONENTS:0xc

A 2-bit value for encoding texture components.

### -field D3D_SIF_UNUSED:0x10

This value is reserved.

### -field D3D10_SIF_USERPACKED

Assign a shader input to a register based on the register assignment in the HLSL code (instead of letting the compiler choose the register).

### -field D3D10_SIF_COMPARISON_SAMPLER

Use a comparison sampler, which uses the <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-samplecmp">SampleCmp (DirectX HLSL Texture Object)</a> and <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-samplecmplevelzero">SampleCmpLevelZero (DirectX HLSL Texture Object)</a> sampling functions.

### -field D3D10_SIF_TEXTURE_COMPONENT_0

A 2-bit value for encoding texture components.

### -field D3D10_SIF_TEXTURE_COMPONENT_1

A 2-bit value for encoding texture components.

### -field D3D10_SIF_TEXTURE_COMPONENTS

A 2-bit value for encoding texture components.

### -field D3D_SIF_FORCE_DWORD:0x7fffffff

Forces the enumeration to compile to 32 bits.
            This value is not used directly by titles.

## -remarks

<b>D3D_SHADER_INPUT_FLAGS</b>-typed values are specified in
          the <b>uFlags</b> member of the <a href="/windows/win32/api/d3d11shader/ns-d3d11shader-d3d11_shader_input_bind_desc">D3D11_SHADER_INPUT_BIND_DESC</a> structure.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-common-enumerations">Common Version Enumerations</a>
