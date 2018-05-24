---
UID: NF:d3d10shader.D3D10PreprocessShader
title: D3D10PreprocessShader function
author: windows-driver-content
description: Generate a shader-text string that contains the shader tokens that would be found in a compiled shader.
old-location: direct3d10\d3d10preprocessshader.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10preprocessshader.htm
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: D3D10PreprocessShader, D3D10PreprocessShader function [Direct3D 10], d3d10shader/D3D10PreprocessShader, d3e7d365-dba7-908d-52f5-76fc58522bad, direct3d10.d3d10preprocessshader
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: D3D10_MESSAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	D3D10.dll
api_name:
-	D3D10PreprocessShader
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: D3D10.dll
req.irql: 
---

# D3D10PreprocessShader function


## -description


Generate a shader-text string that contains the shader tokens that would be found in a compiled shader.


## -parameters




### -param pSrcData [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

Pointer to a string containing the shader source code.


### -param SrcDataSize [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

Size of pSrcData, in bytes.


### -param pFileName [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The name of the file that contains the shader code.


### -param pDefines [in]

Type: <b>const <a href="https://msdn.microsoft.com/35953846-a07e-4ca3-91d9-3ddb3944614d">D3D10_SHADER_MACRO</a>*</b>

Optional. Pointer to an array of macro definitions (see <a href="https://msdn.microsoft.com/35953846-a07e-4ca3-91d9-3ddb3944614d">D3D10_SHADER_MACRO</a>). 
          The last structure in the array serves as a terminator and must have all members set to 0.  
          If not used, set <i>pDefines</i> to <b>NULL</b>.


### -param pInclude [in]

Type: <b><a href="https://msdn.microsoft.com/9e8a6b37-0b0c-46d1-aa4a-35efc07f1a6b">LPD3D10INCLUDE</a></b>

Optional. Pointer to an <a href="https://msdn.microsoft.com/9e8a6b37-0b0c-46d1-aa4a-35efc07f1a6b">ID3D10Include Interface</a> interface for handling include files. Setting this to <b>NULL</b> will cause a compile error if a shader contains a #include.


### -param ppShaderText [out]

Type: <b><a href="https://msdn.microsoft.com/d180fee0-1a69-4250-a0c4-d6e3754f063a">ID3D10Blob</a>**</b>

A pointer to a buffer that receives a pointer to an <a href="https://msdn.microsoft.com/d180fee0-1a69-4250-a0c4-d6e3754f063a">ID3D10Blob Interface</a> that contains a single string containing shader-tokens.


### -param ppErrorMsgs [out]

Type: <b><a href="https://msdn.microsoft.com/d180fee0-1a69-4250-a0c4-d6e3754f063a">ID3D10Blob</a>**</b>

A pointer to a buffer that receives a pointer to an <a href="https://msdn.microsoft.com/d180fee0-1a69-4250-a0c4-d6e3754f063a">ID3D10Blob Interface</a> that contains a listing of errors and warnings that occurred during compilation. These errors and warnings are identical to the debug output from a debugger.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



Use this function to generate a shader-token stream, which is the compiled output of the shader compiler.




## -see-also




<a href="https://msdn.microsoft.com/c8b33c08-7b3f-4b33-9b3c-4aa2b45b8f32">Shader Functions</a>
 

 

