---
UID: NF:d3d10effect.D3D10CompileEffectFromMemory
title: D3D10CompileEffectFromMemory function (d3d10effect.h)
description: Compile an effect.
helpviewer_keywords: ["D3D10CompileEffectFromMemory","D3D10CompileEffectFromMemory function [Direct3D 10]","a15fb616-366d-0a19-dbf6-a1e603c6c9db","d3d10effect/D3D10CompileEffectFromMemory","direct3d10.d3d10compileeffectfrommemory"]
old-location: direct3d10\d3d10compileeffectfrommemory.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10compileeffectfrommemory.htm
ms.date: 12/05/2018
ms.keywords: D3D10CompileEffectFromMemory, D3D10CompileEffectFromMemory function [Direct3D 10], a15fb616-366d-0a19-dbf6-a1e603c6c9db, d3d10effect/D3D10CompileEffectFromMemory, direct3d10.d3d10compileeffectfrommemory
req.header: d3d10effect.h
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
 - D3D10CompileEffectFromMemory
 - d3d10effect/D3D10CompileEffectFromMemory
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
 - D3D10CompileEffectFromMemory
---

# D3D10CompileEffectFromMemory function


## -description

Compile an effect.

<div class="alert"><b>Note</b>  Use <a href="/windows/desktop/direct3d10/d3dx10compilefrommemory">D3DX10CompileFromMemory</a> instead of this function.</div><div> </div>

## -parameters

### -param pData [in]

Type: <b>void*</b>

A pointer to effect data; either ASCII <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-reference">HLSL</a> code or a compiled effect.

### -param DataLength [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

Length of <i>pData</i>.

### -param pSrcFileName [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

The name of the effect file.

### -param pDefines [in]

Type: <b>const <a href="/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro">D3D10_SHADER_MACRO</a>*</b>

Optional. An array of NULL-terminated macro definitions (see <a href="/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro">D3D10_SHADER_MACRO</a>).

### -param pInclude [in]

Type: <b><a href="/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)">ID3D10Include</a>*</b>

Optional. A pointer to an <a href="/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)">ID3D10Include Interface</a> for handling include files. Setting this to <b>NULL</b> will cause a compile error if a shader contains a #include.

### -param HLSLFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Shader <a href="/windows/desktop/direct3d10/d3d10-shader">compile options</a>.

### -param FXFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Effect <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-effect-constants">compile options</a>.

### -param ppCompiledEffect [out]

Type: <b><a href="/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob">ID3D10Blob</a>**</b>

The address of a <a href="/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob">ID3D10Blob Interface</a> that contains the compiled effect.

### -param ppErrors [out]

Type: <b><a href="/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob">ID3D10Blob</a>**</b>

Optional. A pointer to an <a href="/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob">ID3D10Blob Interface</a> that contains compiler error messages, or <b>NULL</b> if there were no errors.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

This function uses the version of the HLSL compiler released in the November 2006 DirectX SDK.

For an example, see <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-effects-compile">Compile an Effect (Direct3D 10)</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-effect-functions">Effect Functions (Direct3D 10)</a>