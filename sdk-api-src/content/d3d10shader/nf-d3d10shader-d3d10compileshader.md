---
UID: NF:d3d10shader.D3D10CompileShader
title: D3D10CompileShader function (d3d10shader.h)
description: Compile an HLSL shader.
helpviewer_keywords: ["8461622f-7f35-e519-3be6-83d985b2cece","D3D10CompileShader","D3D10CompileShader function [Direct3D 10]","d3d10shader/D3D10CompileShader","direct3d10.d3d10compileshader"]
old-location: direct3d10\d3d10compileshader.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10compileshader.htm
ms.date: 12/05/2018
ms.keywords: 8461622f-7f35-e519-3be6-83d985b2cece, D3D10CompileShader, D3D10CompileShader function [Direct3D 10], d3d10shader/D3D10CompileShader, direct3d10.d3d10compileshader
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
 - D3D10CompileShader
 - d3d10shader/D3D10CompileShader
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
 - D3D10CompileShader
---

# D3D10CompileShader function


## -description

Compile an <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-reference">HLSL</a> shader.


<div class="alert"><b>Note</b>  Use <a href="/windows/desktop/direct3d10/d3dx10compilefrommemory">D3DX10CompileFromMemory</a> instead of this function.</div><div> </div>

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

Type: <b><a href="/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)">LPD3D10INCLUDE</a>*</b>

Optional. Pointer to an <a href="/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)">ID3D10Include Interface</a> interface for handling include files. Setting this to <b>NULL</b> will cause a compile error if a shader contains a #include.

### -param pFunctionName [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

Name of the shader-entry point function where shader execution begins.

### -param pProfile [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

A string that specifies the <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-models">shader profile</a> or shader model.

### -param Flags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Shader <a href="/windows/desktop/direct3d10/d3d10-shader">compile options</a>.

### -param ppShader [out]

Type: <b><a href="/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob">ID3D10Blob</a>**</b>

A pointer to an <a href="/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob">ID3D10Blob Interface</a> that contains the compiled shader, as well as any embedded debug and symbol-table information.

### -param ppErrorMsgs [out]

Type: <b><a href="/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob">ID3D10Blob</a>**</b>

A pointer to an <a href="/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob">ID3D10Blob Interface</a> that contains a listing of errors and warnings that occurred during compilation. These errors and warnings are identical to the debug output from a debugger.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

This function uses the version of the HLSL compiler released in the November 2006 DirectX SDK.

This function implements two ways to supply the input shader information. Either use <i>pSrcData</i> and <i>SrcDataLen</i> to specify a string that contains the shader HLSL code (and set <i>pFileName</i> to <b>NULL</b>) or use <i>pFileName</i> to specify the name of a shader or effect file (and set <i>pSrcData</i> to <b>NULL</b>).

To setup a programmable-pipeline stage, compile a shader and then bind the shader to the appropriate pipeline stage. For instance, here is an example compiling a geometry shader (see <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage-getting-started">Compile a Geometry Shader</a>).

This function, D3D10CompileShader, calls the version of the shader compiler that is shipped each time the operating system releases. A more up-to-date version of the shader compiler ships when the DirectX SDK ships, which can be accessed from D3DX by calling a version of the shader compiler entry-point function such as <a href="/windows/desktop/direct3d10/d3dx10compilefromfile">D3DX10CompileFromFile</a>.  It is preferable to use the D3DX entry-point functions to ensure the latest version of the shader compiler will be used if you will be redistributing the DirectX redistributable libraries.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-shader-functions">Shader Functions</a>