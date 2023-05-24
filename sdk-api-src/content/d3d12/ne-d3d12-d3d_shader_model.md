---
UID: NE:d3d12.D3D_SHADER_MODEL
title: D3D_SHADER_MODEL (d3d12.h)
description: Specifies a shader model.
helpviewer_keywords: ["D3D_SHADER_MODEL","D3D_SHADER_MODEL enumeration","D3D_SHADER_MODEL_5_1","D3D_SHADER_MODEL_6_0","D3D_SHADER_MODEL_6_1","d3d12/D3D_SHADER_MODEL","d3d12/D3D_SHADER_MODEL_5_1","d3d12/D3D_SHADER_MODEL_6_0","d3d12/D3D_SHADER_MODEL_6_1","direct3d12.d3d_shader_model"]
old-location: direct3d12\d3d_shader_model.htm
tech.root: direct3d12
ms.assetid: 8C0674AF-CFDD-4511-B621-AB817A81B9BB
ms.date: 11/30/2022
ms.keywords: D3D_SHADER_MODEL, D3D_SHADER_MODEL enumeration, D3D_SHADER_MODEL_5_1, D3D_SHADER_MODEL_6_0, D3D_SHADER_MODEL_6_1, d3d12/D3D_SHADER_MODEL, d3d12/D3D_SHADER_MODEL_5_1, d3d12/D3D_SHADER_MODEL_6_0, d3d12/D3D_SHADER_MODEL_6_1, direct3d12.d3d_shader_model
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
req.typenames: D3D_SHADER_MODEL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D_SHADER_MODEL
 - d3d12/D3D_SHADER_MODEL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D_SHADER_MODEL
---

## -description

Specifies a shader model.

## -enum-fields

### -field D3D_SHADER_MODEL_5_1:0x51

Indicates shader model 5.1.

### -field D3D_SHADER_MODEL_6_0:0x60

Indicates shader model 6.0. Compiling a shader model 6.0 shader requires using the DXC compiler (see [DirectX Shader Compiler](https://github.com/Microsoft/DirectXShaderCompiler)), and is not supported by legacy **FXC**.

### -field D3D_SHADER_MODEL_6_1:0x61

Indicates shader model 6.1.

### -field D3D_SHADER_MODEL_6_2:0x62

### -field D3D_SHADER_MODEL_6_3:0x63

### -field D3D_SHADER_MODEL_6_4:0x64

Shader model 6.4 support was added in Windows 10, Version 1903, and is required for DirectX Raytracing (DXR).

### -field D3D_SHADER_MODEL_6_5:0x65

Shader model 6.5 support was added in Windows 10, Version 2004, and is required for Direct Machine Learning.

### -field D3D_SHADER_MODEL_6_6:0x66

Shader model 6.6 support was added in Windows 11 and the DirectX 12 Agility SDK.

### -field D3D_SHADER_MODEL_6_7:0x67

Shader model 6.7 support was added in the DirectX 12 Agility SDK v1.6. See [Agility SDK 1.606.3: Shader Model 6.7 is now publicly available!](https://devblogs.microsoft.com/directx/shader-model-6-7/) on the DirectX developer blog.

## -remarks

This enum is used by the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_model">D3D12_FEATURE_DATA_SHADER_MODEL</a> structure.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core enumerations</a>
