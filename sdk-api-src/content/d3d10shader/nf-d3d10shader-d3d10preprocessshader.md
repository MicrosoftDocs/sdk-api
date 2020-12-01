---
UID: NF:d3d10shader.D3D10PreprocessShader
title: D3D10PreprocessShader function (d3d10shader.h)
description: Generate a shader-text string that contains the shader tokens that would be found in a compiled shader.
helpviewer_keywords: ["D3D10PreprocessShader","D3D10PreprocessShader function [Direct3D 10]","d3d10shader/D3D10PreprocessShader","d3e7d365-dba7-908d-52f5-76fc58522bad","direct3d10.d3d10preprocessshader"]
old-location: direct3d10\d3d10preprocessshader.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10preprocessshader.htm
ms.date: 12/05/2018
ms.keywords: D3D10PreprocessShader, D3D10PreprocessShader function [Direct3D 10], d3d10shader/D3D10PreprocessShader, d3e7d365-dba7-908d-52f5-76fc58522bad, direct3d10.d3d10preprocessshader
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
 - D3D10PreprocessShader
 - d3d10shader/D3D10PreprocessShader
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
 - D3D10PreprocessShader
---

# D3D10PreprocessShader function


## -description

Generate a shader-text string that contains the shader tokens that would be found in a compiled shader.

## -parameters

### -param pSrcData [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

Pointer to a string containing the shader source code.

### -param SrcDataSize [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

Size of pSrcData, in bytes.

### -param pFileName [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

The name of the file that contains the shader code.

### -param pDefines [in]

Type: <b>const <a href="/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro">D3D10_SHADER_MACRO</a>*</b>

Optional. Pointer to an array of macro definitions (see <a href="/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro">D3D10_SHADER_MACRO</a>). 
          The last structure in the array serves as a terminator and must have all members set to 0.  
          If not used, set <i>pDefines</i> to <b>NULL</b>.

### -param pInclude [in]

Type: <b><a href="/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)">LPD3D10INCLUDE</a></b>

Optional. Pointer to an <a href="/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)">ID3D10Include Interface</a> interface for handling include files. Setting this to <b>NULL</b> will cause a compile error if a shader contains a #include.

### -param ppShaderText [out]

Type: <b><a href="/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob">ID3D10Blob</a>**</b>

A pointer to a buffer that receives a pointer to an <a href="/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob">ID3D10Blob Interface</a> that contains a single string containing shader-tokens.

### -param ppErrorMsgs [out]

Type: <b><a href="/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob">ID3D10Blob</a>**</b>

A pointer to a buffer that receives a pointer to an <a href="/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob">ID3D10Blob Interface</a> that contains a listing of errors and warnings that occurred during compilation. These errors and warnings are identical to the debug output from a debugger.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

Use this function to generate a shader-token stream, which is the compiled output of the shader compiler.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-shader-functions">Shader Functions</a>