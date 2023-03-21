---
UID: NS:d3d12.D3D12_SHADER_BYTECODE
title: D3D12_SHADER_BYTECODE (d3d12.h)
description: Describes shader data. (D3D12_SHADER_BYTECODE)
helpviewer_keywords: ["D3D12_SHADER_BYTECODE","D3D12_SHADER_BYTECODE structure","d3d12/D3D12_SHADER_BYTECODE","direct3d12.d3d12_shader_bytecode"]
old-location: direct3d12\d3d12_shader_bytecode.htm
tech.root: direct3d12
ms.assetid: E2195755-A0C2-4824-A2EB-553F7909847F
ms.date: 12/05/2018
ms.keywords: D3D12_SHADER_BYTECODE, D3D12_SHADER_BYTECODE structure, d3d12/D3D12_SHADER_BYTECODE, direct3d12.d3d12_shader_bytecode
req.header: d3d12.h
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
req.typenames: D3D12_SHADER_BYTECODE
req.redist:
ms.custom: 19H1
f1_keywords:
 - D3D12_SHADER_BYTECODE
 - d3d12/D3D12_SHADER_BYTECODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_SHADER_BYTECODE
---

# D3D12_SHADER_BYTECODE structure


## -description

Describes shader data.

## -struct-fields

### -field pShaderBytecode

A pointer to a memory block that contains the shader data.

### -field BytecodeLength

The size, in bytes, of the shader data that the <b>pShaderBytecode</b> member points to.

## -remarks

The <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc">D3D12_GRAPHICS_PIPELINE_STATE_DESC</a> and <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc">D3D12_COMPUTE_PIPELINE_STATE_DESC</a> objects contain <b>D3D12_SHADER_BYTECODE</b> structures that describe various shader types.

When loading a shader from FXC/DXC, this may be the entire compiled blob as is loaded from disk.

## -see-also

<a href="/windows/desktop/direct3d12/cd3dx12-shader-bytecode">CD3DX12_SHADER_BYTECODE</a>

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>
