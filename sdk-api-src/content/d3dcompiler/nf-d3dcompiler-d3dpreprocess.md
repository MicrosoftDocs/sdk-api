---
UID: NF:d3dcompiler.D3DPreprocess
title: D3DPreprocess function (d3dcompiler.h)
description: Preprocesses uncompiled HLSL code.
helpviewer_keywords: ["91482c2f-2730-5aba-e73a-43653c75ff49","D3DPreprocess","D3DPreprocess function [HLSL]","d3dcompiler/D3DPreprocess","direct3dhlsl.d3dpreprocess"]
old-location: direct3dhlsl\d3dpreprocess.htm
tech.root: direct3dhlsl
ms.assetid: VS|directx_sdk|~\d3dpreprocess.htm
ms.date: 12/05/2018
ms.keywords: 91482c2f-2730-5aba-e73a-43653c75ff49, D3DPreprocess, D3DPreprocess function [HLSL], d3dcompiler/D3DPreprocess, direct3dhlsl.d3dpreprocess
req.header: d3dcompiler.h
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
req.lib: D3dcompiler_47.lib
req.dll: D3dcompiler_47.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3DPreprocess
 - d3dcompiler/D3DPreprocess
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - d3dcompiler_47.dll
api_name:
 - D3DPreprocess
---

# D3DPreprocess function


## -description

Preprocesses uncompiled HLSL code.

## -parameters

### -param pSrcData [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCVOID</a></b>

A pointer to uncompiled shader data; either ASCII HLSL code or a compiled effect.

### -param SrcDataSize [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

Length of <i>pSrcData</i>.

### -param pSourceName [in, optional]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

 The name of the file that contains the uncompiled HLSL code.

### -param pDefines [in, optional]

Type: <b>const <a href="/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro">D3D_SHADER_MACRO</a>*</b>

 An array of NULL-terminated macro definitions (see <a href="/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro">D3D_SHADER_MACRO</a>).

### -param pInclude [in, optional]

Type: <b><a href="/windows/desktop/api/d3dcommon/nn-d3dcommon-id3dinclude">ID3DInclude</a>*</b>

 A pointer to an <a href="/windows/desktop/api/d3dcommon/nn-d3dcommon-id3dinclude">ID3DInclude</a> for handling include files. Setting this to <b>NULL</b> will cause a compile error if a shader contains a #include. You can pass the <b>D3D_COMPILE_STANDARD_FILE_INCLUDE</b> macro, which is a pointer to a default include handler. This default include handler includes files that are relative to the current directory and files that are relative to the directory of the initial source file. When you use <b>D3D_COMPILE_STANDARD_FILE_INCLUDE</b>, you must specify the source file name in the <i>pSourceName</i> parameter; the compiler will derive the initial relative directory from <i>pSourceName</i>.


```cpp
#define D3D_COMPILE_STANDARD_FILE_INCLUDE ((ID3DInclude*)(UINT_PTR)1)

```

### -param ppCodeText [out]

Type: <b><a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a>**</b>

A pointer to a variable that receives a pointer to the <a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a> interface that you can use to access the preprocessed code.

### -param ppErrorMsgs [out, optional]

Type: <b><a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a>**</b>

 A pointer to an <a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a> that contains compiler error messages, or <b>NULL</b> if there were no errors.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 return codes</a>.

## -remarks

<b>D3DPreprocess</b> outputs <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-appendix-pre-line">#line</a> directives and preserves line numbering of source input so that output line numbering can be properly related to the input source.

## -see-also

<a href="/windows/desktop/direct3dhlsl/dx-graphics-d3dcompiler-reference-functions">Functions</a>
