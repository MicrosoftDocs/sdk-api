---
UID: NF:d3dcompiler.D3DCompileFromFile
title: D3DCompileFromFile function
author: windows-sdk-content
description: Compiles Microsoft High Level Shader Language (HLSL) code into bytecode for a given target.
old-location: direct3dhlsl\d3dcompilefromfile.htm
old-project: direct3dhlsl
ms.assetid: 09F1DB4F-C279-4E25-8A1C-34272EB62C07
ms.author: windowssdkdev
ms.date: 04/12/2018
ms.keywords: D3DCompileFromFile, D3DCompileFromFile function [HLSL], d3dcompiler/D3DCompileFromFile, direct3dhlsl.d3dcompilefromfile
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: D3D_BLOB_PART
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	D3DCompiler_47.dll
api_name:
-	D3DCompileFromFile
product: Windows
targetos: Windows
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
---

# D3DCompileFromFile function


## -description


<div class="alert"><b>Note</b>  You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store. Refer to the section, "Compiling shaders for UWP", in the remarks for <a href="https://msdn.microsoft.com/0CE217EA-44F4-4017-B2ED-95E8B122CA95">D3DCompile2</a>.</div><div> </div>Compiles Microsoft High Level Shader Language (HLSL) code into bytecode for a given target.


## -parameters




### -param pFileName [in]

A pointer to a constant null-terminated string that contains  the name of the file that contains the shader code.


### -param pDefines [in, optional]

An optional array of <a href="https://msdn.microsoft.com/8cfe0b3c-5ce8-4d59-8fd9-0fdf200c9552">D3D_SHADER_MACRO</a> structures that define shader macros. Each macro definition contains a name and a NULL-terminated definition. If not used, set to <b>NULL</b>.


### -param pInclude [in, optional]

 An optional pointer to an <a href="https://msdn.microsoft.com/2020ce65-3a6e-4a9f-9e97-b94e3c75f4f5">ID3DInclude</a> interface that the compiler uses to handle include files. If you set this parameter to <b>NULL</b> and the shader contains a #include, a compile error occurs. You can pass the <b>D3D_COMPILE_STANDARD_FILE_INCLUDE</b> macro, which is a pointer to a default include handler. This default include handler includes files that are relative to the current directory.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>#define D3D_COMPILE_STANDARD_FILE_INCLUDE ((ID3DInclude*)(UINT_PTR)1)
</pre>
</td>
</tr>
</table></span></div>

### -param pEntrypoint [in]

A pointer to a constant null-terminated string that contains  the name of the shader entry point function where shader execution begins. When you compile an effect, <b>D3DCompileFromFile</b> ignores <i>pEntrypoint</i>; we recommend that you set <i>pEntrypoint</i> to <b>NULL</b> because it is good programming practice to set a pointer parameter to <b>NULL</b> if the called function will not use it.


### -param pTarget [in]

A pointer to a constant null-terminated string that specifies the shader target or set of shader features to compile against. The shader target can be a shader model (for example, shader model 2, shader model 3, shader model 4, or shader model 5 and later). The target can also be an effect type (for example, fx_4_1). For info about the targets that various profiles support, see <a href="https://msdn.microsoft.com/594E1C14-C1D4-4207-91A1-28892CE6D821">Specifying Compiler Targets</a>. 


### -param Flags1 [in]

A combination of shader <a href="https://msdn.microsoft.com/039627DD-D6A4-4EA3-8E91-D2A20770E6FF">compile options</a> that are combined by using a bitwise <b>OR</b> operation. The resulting value specifies how the compiler compiles the HLSL code.


### -param Flags2 [in]

A combination of effect <a href="https://msdn.microsoft.com/AA46E5ED-92DD-4327-B852-8DD23A878562">compile options</a> that are combined by using a bitwise <b>OR</b> operation. The resulting value specifies how the compiler compiles the effect. When you compile a shader and not an effect file, <b>D3DCompileFromFile</b> ignores <i>Flags2</i>; we recommend that you set <i>Flags2</i> to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.


### -param ppCode [out]

A pointer to a variable that receives a pointer to the <a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a> interface that you can use to access the compiled code.


### -param ppErrorMsgs [out, optional]

An optional pointer to a variable that receives a pointer to the <a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a> interface that you can use to access compiler error messages, or <b>NULL</b> if there are no errors.


## -returns



Returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 return codes</a>.




## -remarks



<div class="alert"><b>Note</b>  The D3dcompiler_44.dll or later version of the file contains the <b>D3DCompileFromFile</b> compiler function.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>
 

 

