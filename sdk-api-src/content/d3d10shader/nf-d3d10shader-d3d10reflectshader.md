---
UID: NF:d3d10shader.D3D10ReflectShader
title: D3D10ReflectShader function (d3d10shader.h)
description: This function -- which creates a shader-reflection object for retrieving information about a compiled shader -- has been deprecated. Instead, use D3DReflect.
helpviewer_keywords: ["D3D10ReflectShader","D3D10ReflectShader function [Direct3D 10]","abc201df-57cf-fbbd-708b-94ffa50ba7d4","d3d10shader/D3D10ReflectShader","direct3d10.d3d10reflectshader"]
old-location: direct3d10\d3d10reflectshader.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10reflectshader.htm
ms.date: 12/05/2018
ms.keywords: D3D10ReflectShader, D3D10ReflectShader function [Direct3D 10], abc201df-57cf-fbbd-708b-94ffa50ba7d4, d3d10shader/D3D10ReflectShader, direct3d10.d3d10reflectshader
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
req.lib: D3D10.lib
req.dll: D3D10.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10ReflectShader
 - d3d10shader/D3D10ReflectShader
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3D10.dll
api_name:
 - D3D10ReflectShader
---

# D3D10ReflectShader function


## -description

This function -- which creates a shader-reflection object for retrieving information about a compiled shader -- has been deprecated. Instead, use <a href="/windows/desktop/direct3dhlsl/d3dreflect">D3DReflect</a>.

## -parameters

### -param pShaderBytecode [in]

Type: <b>const void*</b>

A pointer to the compiled shader.

### -param BytecodeLength [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

Length of pShaderBytecode.

### -param ppReflector [out]

Type: <b><a href="/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflection">ID3D10ShaderReflection</a>**</b>

Address of a reflection interface.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Return value.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-shader-functions">Shader Functions</a>