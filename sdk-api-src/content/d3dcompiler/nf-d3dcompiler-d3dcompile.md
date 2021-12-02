---
UID: NF:d3dcompiler.D3DCompile
title: D3DCompile function (d3dcompiler.h)
description: Compile HLSL code or an effect file into bytecode for a given target.
helpviewer_keywords: ["D3DCompile","D3DCompile function [HLSL]","a18240ba-8d29-6dcc-da59-7c146428c2b8","d3dcompiler/D3DCompile","direct3dhlsl.d3dcompile"]
old-location: direct3dhlsl\d3dcompile.htm
tech.root: direct3dhlsl
ms.assetid: VS|directx_sdk|~\d3dcompile.htm
ms.date: 12/05/2018
ms.keywords: D3DCompile, D3DCompile function [HLSL], a18240ba-8d29-6dcc-da59-7c146428c2b8, d3dcompiler/D3DCompile, direct3dhlsl.d3dcompile
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
req.lib: d3dcompiler.lib
req.dll: d3dcompiler_47.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3DCompile
 - d3dcompiler/D3DCompile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - d3dcompiler.dll
api_name:
 - D3DCompile
---

# D3DCompile function


## -description

Compile HLSL code or an  effect file into bytecode for a given target.

## -parameters

### -param pSrcData [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCVOID</a></b>

A pointer to uncompiled shader data; either ASCII HLSL code or a compiled effect.

### -param SrcDataSize [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

Length of <i>pSrcData</i>.

### -param pSourceName [in, optional]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

 You can use this parameter for strings that specify  error messages. If not used, set to <b>NULL</b>.

### -param pDefines [in, optional]

Type: <b>const <a href="/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro">D3D_SHADER_MACRO</a>*</b>

An optional array of <a href="/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro">D3D_SHADER_MACRO</a> structures that define shader macros. Each macro definition contains a name and a null-terminated definition. If not used, set to <b>NULL</b>. The last structure in the array serves as a terminator and must have all members set to <b>NULL</b>.

### -param pInclude [in, optional]

Type: <b><a href="/windows/desktop/api/d3dcommon/nn-d3dcommon-id3dinclude">ID3DInclude</a>*</b>

Optional. A pointer to an <a href="/windows/desktop/api/d3dcommon/nn-d3dcommon-id3dinclude">ID3DInclude</a> for handling include files. Setting this to <b>NULL</b> will cause a compile error if a shader contains a #include. You can pass the <b>D3D_COMPILE_STANDARD_FILE_INCLUDE</b> macro, which is a pointer to a default include handler. This default include handler includes files that are relative to the current directory and files that are relative to the directory of the initial source file. When you use <b>D3D_COMPILE_STANDARD_FILE_INCLUDE</b>, you must specify the source file name in the <i>pSourceName</i> parameter; the compiler will derive the initial relative directory from <i>pSourceName</i>.


```cpp
#define D3D_COMPILE_STANDARD_FILE_INCLUDE ((ID3DInclude*)(UINT_PTR)1)

```

### -param pEntrypoint [in, optional]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

The name of the shader entry point function where shader execution begins. When you compile using a fx profile (for example, fx_4_0, fx_5_0, and so on), <b>D3DCompile</b> ignores <i>pEntrypoint</i>. In this case, we recommend that you set <i>pEntrypoint</i> to <b>NULL</b> because it is good programming practice to set a pointer parameter to <b>NULL</b> if the called function will not use it. For all other shader profiles, a valid <i>pEntrypoint</i> is required.

### -param pTarget [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

A string that specifies the shader target or set of shader features to compile against. The shader target can be shader model 2, shader model 3, shader model 4, or shader model 5. The target can also be an effect type (for example, fx_4_1). For info about the targets that various profiles support, see <a href="/windows/desktop/direct3dhlsl/specifying-compiler-targets">Specifying Compiler Targets</a>.

### -param Flags1 [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Flags defined by <a href="/windows/desktop/direct3dhlsl/d3dcompile-constants">D3D compile constants</a>.

### -param Flags2 [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Flags defined by <a href="/windows/desktop/direct3dhlsl/d3dcompile-effect-constants">D3D compile effect constants</a>. When you compile a shader and not an effect file, <b>D3DCompile</b> ignores <i>Flags2</i>; we recommend that you set <i>Flags2</i> to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.

### -param ppCode [out]

Type: <b><a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a>**</b>

A pointer to a variable that receives a pointer to the <a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a> interface that you can use to access the compiled code.

### -param ppErrorMsgs [out, optional]

Type: <b><a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a>**</b>

A pointer to a variable that receives a pointer to the <a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a> interface that you can use to access compiler error messages, or <b>NULL</b> if there are no errors.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 return codes</a>.

## -remarks

The difference between <b>D3DCompile</b> and <a href="/windows/desktop/direct3dhlsl/d3dcompile2">D3DCompile2</a> is that the latter method takes some optional parameters that can be used to control some aspects of how bytecode is generated. If this extra flexibility is not required, there is no performance gain from using <b>D3DCompile2</b>.

## -see-also

<a href="/windows/desktop/direct3dhlsl/dx-graphics-d3dcompiler-reference-functions">Functions</a>