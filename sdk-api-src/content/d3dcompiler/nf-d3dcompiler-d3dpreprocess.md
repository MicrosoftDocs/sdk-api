---
UID: NF:d3dcompiler.D3DPreprocess
title: D3DPreprocess function
author: windows-sdk-content
description: Preprocesses uncompiled HLSL code.
old-location: direct3dhlsl\d3dpreprocess.htm
old-project: direct3dhlsl
ms.assetid: VS|directx_sdk|~\d3dpreprocess.htm
ms.author: windowssdkdev
ms.date: 06/18/2018
ms.keywords: 91482c2f-2730-5aba-e73a-43653c75ff49, D3DPreprocess, D3DPreprocess function [HLSL], d3dcompiler/D3DPreprocess, direct3dhlsl.d3dpreprocess
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
tech.root: 
req.typenames: D3D_BLOB_PART
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - d3dcompiler_47.dll
api_name:
 - D3DPreprocess
product: Windows
targetos: Windows
req.lib: D3dcompiler_47.lib
req.dll: D3dcompiler_47.dll
req.irql: 
---

# D3DPreprocess function


## -description


Preprocesses uncompiled HLSL code.


## -parameters




### -param pSrcData [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCVOID</a></b>

A pointer to uncompiled shader data; either ASCII HLSL code or a compiled effect.


### -param SrcDataSize [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

Length of <i>pSrcData</i>.


### -param pSourceName [in, optional]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

 The name of the file that contains the uncompiled HLSL code.


### -param pDefines [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/8cfe0b3c-5ce8-4d59-8fd9-0fdf200c9552">D3D_SHADER_MACRO</a>*</b>

 An array of NULL-terminated macro definitions (see <a href="https://msdn.microsoft.com/8cfe0b3c-5ce8-4d59-8fd9-0fdf200c9552">D3D_SHADER_MACRO</a>).


### -param pInclude [in, optional]

Type: <b><a href="https://msdn.microsoft.com/2020ce65-3a6e-4a9f-9e97-b94e3c75f4f5">ID3DInclude</a>*</b>

 A pointer to an <a href="https://msdn.microsoft.com/2020ce65-3a6e-4a9f-9e97-b94e3c75f4f5">ID3DInclude</a> for handling include files. Setting this to <b>NULL</b> will cause a compile error if a shader contains a #include. You can pass the <b>D3D_COMPILE_STANDARD_FILE_INCLUDE</b> macro, which is a pointer to a default include handler. This default include handler includes files that are relative to the current directory and files that are relative to the directory of the initial source file. When you use <b>D3D_COMPILE_STANDARD_FILE_INCLUDE</b>, you must specify the source file name in the <i>pSourceName</i> parameter; the compiler will derive the initial relative directory from <i>pSourceName</i>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#define D3D_COMPILE_STANDARD_FILE_INCLUDE ((ID3DInclude*)(UINT_PTR)1)
</pre>
</td>
</tr>
</table></span></div>

### -param ppCodeText [out]

Type: <b><a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a>**</b>

The address of a <a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a> that contains the compiled code.


### -param ppErrorMsgs [out, optional]

Type: <b><a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a>**</b>

 A pointer to an <a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a> that contains compiler error messages, or <b>NULL</b> if there were no errors.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 return codes</a>.




## -remarks



<b>D3DPreprocess</b> outputs <a href="https://msdn.microsoft.com/library/Dd607350(v=VS.85).aspx">#line</a> directives and preserves line numbering of source input so that output line numbering can be properly related to the input source.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>
 

 

