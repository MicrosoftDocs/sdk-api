---
UID: NS:d3dcommon._D3D_SHADER_MACRO
title: D3D_SHADER_MACRO (d3dcommon.h)
description: Defines a shader macro.
helpviewer_keywords: ["*LPD3D_SHADER_MACRO","D3D_SHADER_MACRO","D3D_SHADER_MACRO structure [Direct3D 11]","LPD3D_SHADER_MACRO","LPD3D_SHADER_MACRO structure pointer [Direct3D 11]","d3dcommon/D3D_SHADER_MACRO","d3dcommon/LPD3D_SHADER_MACRO","direct3d11.d3d_shader_macro"]
old-location: direct3d11\d3d_shader_macro.htm
tech.root: direct3d11
ms.assetid: 8cfe0b3c-5ce8-4d59-8fd9-0fdf200c9552
ms.date: 12/05/2018
ms.keywords: '*LPD3D_SHADER_MACRO, D3D_SHADER_MACRO, D3D_SHADER_MACRO structure [Direct3D 11], LPD3D_SHADER_MACRO, LPD3D_SHADER_MACRO structure pointer [Direct3D 11], d3dcommon/D3D_SHADER_MACRO, d3dcommon/LPD3D_SHADER_MACRO, direct3d11.d3d_shader_macro'
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
req.typenames: D3D_SHADER_MACRO, *LPD3D_SHADER_MACRO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D_SHADER_MACRO
 - d3dcommon/_D3D_SHADER_MACRO
 - LPD3D_SHADER_MACRO
 - d3dcommon/LPD3D_SHADER_MACRO
 - D3D_SHADER_MACRO
 - d3dcommon/D3D_SHADER_MACRO
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
 - D3D_SHADER_MACRO
---

# D3D_SHADER_MACRO structure


## -description

Defines a shader macro.

## -struct-fields

### -field Name

The macro name.

### -field Definition

The macro definition.

## -remarks

You can use shader macros in your shaders. The <b>D3D_SHADER_MACRO</b> structure defines a single shader macro as shown in the following example:


```

D3D_SHADER_MACRO Shader_Macros[] = { "zero", "0", NULL, NULL };

```


The following shader or effect creation functions take an array of shader macros as an input parameter:

<ul>
<li>
<a href="/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10compileshader">D3D10CompileShader</a>
</li>
<li>
<a href="/windows/desktop/direct3d10/d3dx10createeffectfromfile">D3DX10CreateEffectFromFile</a>
</li>
<li>
<a href="/windows/desktop/direct3d10/d3dx10preprocessshaderfromfile">D3DX10PreprocessShaderFromFile</a>
</li>
<li>
<a href="/windows/desktop/direct3d11/d3dx11createasyncshaderpreprocessprocessor">D3DX11CreateAsyncShaderPreprocessProcessor</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-common-structures">Common Version Structures</a>