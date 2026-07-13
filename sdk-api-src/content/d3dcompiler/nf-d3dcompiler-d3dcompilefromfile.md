---
UID: NF:d3dcompiler.D3DCompileFromFile
title: D3DCompileFromFile function (d3dcompiler.h)
description: Compiles Microsoft High Level Shader Language (HLSL) code into bytecode for a given target. (D3DCompileFromFile)
helpviewer_keywords: ["D3DCompileFromFile","D3DCompileFromFile function [HLSL]","d3dcompiler/D3DCompileFromFile","direct3dhlsl.d3dcompilefromfile"]
old-location: direct3dhlsl\d3dcompilefromfile.htm
tech.root: direct3dhlsl
ms.assetid: 09F1DB4F-C279-4E25-8A1C-34272EB62C07
ms.date: 12/05/2018
ms.keywords: D3DCompileFromFile, D3DCompileFromFile function [HLSL], d3dcompiler/D3DCompileFromFile, direct3dhlsl.d3dcompilefromfile
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
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3DCompileFromFile
 - d3dcompiler/D3DCompileFromFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3DCompiler_47.dll
api_name:
 - D3DCompileFromFile
---

# D3DCompileFromFile function


## -description

<div class="alert"><b>Note</b>  You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store. Refer to the section, "Compiling shaders for UWP", in the remarks for <a href="/windows/desktop/direct3dhlsl/d3dcompile2">D3DCompile2</a>.</div><div> </div>Compiles Microsoft High Level Shader Language (HLSL) code into bytecode for a given target.

## -parameters

### -param pFileName [in]

A pointer to a constant null-terminated string that contains  the name of the file that contains the shader code.

### -param pDefines [in, optional]

An optional array of <a href="/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro">D3D_SHADER_MACRO</a> structures that define shader macros. Each macro definition contains a name and a null-terminated definition. If not used, set to <b>NULL</b>. The last structure in the array serves as a terminator and must have all members set to <b>NULL</b>.

### -param pInclude [in, optional]

 An optional pointer to an <a href="/windows/desktop/api/d3dcommon/nn-d3dcommon-id3dinclude">ID3DInclude</a> interface that the compiler uses to handle include files. If you set this parameter to <b>NULL</b> and the shader contains a #include, a compile error occurs. You can pass the <b>D3D_COMPILE_STANDARD_FILE_INCLUDE</b> macro, which is a pointer to a default include handler. This default include handler includes files that are relative to the current directory.


```
#define D3D_COMPILE_STANDARD_FILE_INCLUDE ((ID3DInclude*)(UINT_PTR)1)

```

### -param pEntrypoint [in]

A pointer to a constant null-terminated string that contains  the name of the shader entry point function where shader execution begins. When you compile an effect, <b>D3DCompileFromFile</b> ignores <i>pEntrypoint</i>; we recommend that you set <i>pEntrypoint</i> to <b>NULL</b> because it is good programming practice to set a pointer parameter to <b>NULL</b> if the called function will not use it.

### -param pTarget [in]

A pointer to a constant null-terminated string that specifies the shader target or set of shader features to compile against. The shader target can be a shader model (for example, shader model 2, shader model 3, shader model 4, or shader model 5 and later). The target can also be an effect type (for example, fx_4_1). For info about the targets that various profiles support, see <a href="/windows/desktop/direct3dhlsl/specifying-compiler-targets">Specifying Compiler Targets</a>.

### -param Flags1 [in]

A combination of shader <a href="/windows/desktop/direct3dhlsl/d3dcompile-constants">compile options</a> that are combined by using a bitwise <b>OR</b> operation. The resulting value specifies how the compiler compiles the HLSL code.

### -param Flags2 [in]

A combination of effect <a href="/windows/desktop/direct3dhlsl/d3dcompile-effect-constants">compile options</a> that are combined by using a bitwise <b>OR</b> operation. The resulting value specifies how the compiler compiles the effect. When you compile a shader and not an effect file, <b>D3DCompileFromFile</b> ignores <i>Flags2</i>; we recommend that you set <i>Flags2</i> to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.

### -param ppCode [out]

A pointer to a variable that receives a pointer to the <a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a> interface that you can use to access the compiled code.

### -param ppErrorMsgs [out, optional]

An optional pointer to a variable that receives a pointer to the <a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a> interface that you can use to access compiler error messages, or <b>NULL</b> if there are no errors.

## -returns

Returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 return codes</a>.

## -remarks

<div class="alert"><b>Note</b>  The D3dcompiler_44.dll or later version of the file contains the <b>D3DCompileFromFile</b> compiler function.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/direct3dhlsl/dx-graphics-d3dcompiler-reference-functions">Functions</a>
