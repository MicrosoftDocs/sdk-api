---
UID: NS:d3d10_1shader._D3D10_SHADER_DEBUG_INPUT_INFO
title: D3D10_SHADER_DEBUG_INPUT_INFO (d3d10_1shader.h)
description: Describes a shader input.
helpviewer_keywords: ["985acea2-3d0c-4a4c-f9db-ed556aec5b34","D3D10_SHADER_DEBUG_INPUT_INFO","D3D10_SHADER_DEBUG_INPUT_INFO structure [Direct3D 10]","d3d10_1shader/D3D10_SHADER_DEBUG_INPUT_INFO","direct3d10.d3d10_shader_debug_input_info"]
old-location: direct3d10\d3d10_shader_debug_input_info.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_debug_input_info.htm
ms.date: 12/05/2018
ms.keywords: 985acea2-3d0c-4a4c-f9db-ed556aec5b34, D3D10_SHADER_DEBUG_INPUT_INFO, D3D10_SHADER_DEBUG_INPUT_INFO structure [Direct3D 10], d3d10_1shader/D3D10_SHADER_DEBUG_INPUT_INFO, direct3d10.d3d10_shader_debug_input_info
req.header: d3d10_1shader.h
req.include-header: D3D10Shader.h
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
req.typenames: D3D10_SHADER_DEBUG_INPUT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D10_SHADER_DEBUG_INPUT_INFO
 - d3d10_1shader/_D3D10_SHADER_DEBUG_INPUT_INFO
 - D3D10_SHADER_DEBUG_INPUT_INFO
 - d3d10_1shader/D3D10_SHADER_DEBUG_INPUT_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d10_1shader.h
api_name:
 - D3D10_SHADER_DEBUG_INPUT_INFO
---

# D3D10_SHADER_DEBUG_INPUT_INFO structure


## -description

Describes a shader input.

## -struct-fields

### -field Var

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index into array of variables to initialize.

### -field InitialRegisterSet

Type: <b><a href="/windows/win32/api/d3d10_1shader/ne-d3d10_1shader-d3d10_shader_debug_regtype">D3D10_SHADER_DEBUG_REGTYPE</a></b>

Must be D3D10_SHADER_DEBUG_REG_INPUT, D3D10_SHADER_DEBUG_REG_CBUFFER or D3D10_SHADER_DEBUG_REG_TBUFFER.

### -field InitialBank

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Will contain a cbuffer or tbuffer slot, geometry shader input primitive number, identifying register for an indexable temp, or -1.

### -field InitialRegister

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Register in register set.  <b>InitialRegister</b> will be -1 if it is temporary.

### -field InitialComponent

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Gives the component.  <b>InitialComponent</b> will be -1 it is temporary.

### -field InitialValue

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Initial value if the variable is a literal.

## -remarks

The <b>D3D10_SHADER_DEBUG_INPUT_INFO</b> structure is used with the <a href="/windows/win32/api/d3d10_1shader/ns-d3d10_1shader-d3d10_shader_debug_info">D3D10_SHADER_DEBUG_INFO</a> structure.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-shader-structures">Shader Structures</a>