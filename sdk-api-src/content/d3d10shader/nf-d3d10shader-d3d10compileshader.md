---
UID: NF:d3d10shader.D3D10CompileShader
title: D3D10CompileShader function
author: windows-driver-content
description: Compile an HLSL shader.
old-location: direct3d10\d3d10compileshader.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10compileshader.htm
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: 8461622f-7f35-e519-3be6-83d985b2cece, D3D10CompileShader, D3D10CompileShader function [Direct3D 10], d3d10shader/D3D10CompileShader, direct3d10.d3d10compileshader
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
-	D3D10CompileShader
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: D3D10.dll
req.irql: 
---

# D3D10CompileShader function


## -description


Compile an <a href="https://msdn.microsoft.com/1d0e12ff-8559-4e5c-9914-6ed313ea5464">HLSL</a> shader.


<div class="alert"><b>Note</b>  Use <a href="https://msdn.microsoft.com/c6458d82-a649-402c-8180-5b7320f9fdb0">D3DX10CompileFromMemory</a> instead of this function.</div><div> </div>

## -parameters




### -param pSrcData [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

Pointer to a string containing the shader source code.


### -param SrcDataSize

TBD


### -param pFileName [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The name of the file that contains the shader code.


### -param pDefines [in]

Type: <b>const <a href="https://msdn.microsoft.com/35953846-a07e-4ca3-91d9-3ddb3944614d">D3D10_SHADER_MACRO</a>*</b>

Optional. Pointer to an array of macro definitions (see <a href="https://msdn.microsoft.com/35953846-a07e-4ca3-91d9-3ddb3944614d">D3D10_SHADER_MACRO</a>). 
          The last structure in the array serves as a terminator and must have all members set to 0.  
          If not used, set <i>pDefines</i> to <b>NULL</b>.


### -param pInclude [in]

Type: <b><a href="https://msdn.microsoft.com/9e8a6b37-0b0c-46d1-aa4a-35efc07f1a6b">LPD3D10INCLUDE</a>*</b>

Optional. Pointer to an <a href="https://msdn.microsoft.com/9e8a6b37-0b0c-46d1-aa4a-35efc07f1a6b">ID3D10Include Interface</a> interface for handling include files. Setting this to <b>NULL</b> will cause a compile error if a shader contains a #include.


### -param pFunctionName [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

Name of the shader-entry point function where shader execution begins.


### -param pProfile [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

A string that specifies the <a href="https://msdn.microsoft.com/6224f05e-20b1-42ea-96fb-63dd0edb720e">shader profile</a> or shader model.


### -param Flags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Shader <a href="https://msdn.microsoft.com/418633d8-47ee-40d0-9b80-89aa860f2e8b">compile options</a>.


### -param ppShader [out]

Type: <b><a href="https://msdn.microsoft.com/d180fee0-1a69-4250-a0c4-d6e3754f063a">ID3D10Blob</a>**</b>

A pointer to an <a href="https://msdn.microsoft.com/d180fee0-1a69-4250-a0c4-d6e3754f063a">ID3D10Blob Interface</a> that contains the compiled shader, as well as any embedded debug and symbol-table information.


### -param ppErrorMsgs [out]

Type: <b><a href="https://msdn.microsoft.com/d180fee0-1a69-4250-a0c4-d6e3754f063a">ID3D10Blob</a>**</b>

A pointer to an <a href="https://msdn.microsoft.com/d180fee0-1a69-4250-a0c4-d6e3754f063a">ID3D10Blob Interface</a> that contains a listing of errors and warnings that occurred during compilation. These errors and warnings are identical to the debug output from a debugger.


#### - SrcDataLen [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

Size of pSrcData, in bytes.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



This function uses the version of the HLSL compiler released in the November 2006 DirectX SDK.

This function implements two ways to supply the input shader information. Either use <i>pSrcData</i> and <i>SrcDataLen</i> to specify a string that contains the shader HLSL code (and set <i>pFileName</i> to <b>NULL</b>) or use <i>pFileName</i> to specify the name of a shader or effect file (and set <i>pSrcData</i> to <b>NULL</b>).

To setup a programmable-pipeline stage, compile a shader and then bind the shader to the appropriate pipeline stage. For instance, here is an example compiling a geometry shader (see <a href="https://msdn.microsoft.com/37146486-5922-4833-850c-cc4a51de0957">Compile a Geometry Shader</a>).

This function, D3D10CompileShader, calls the version of the shader compiler that is shipped each time the operating system releases. A more up-to-date version of the shader compiler ships when the DirectX SDK ships, which can be accessed from D3DX by calling a version of the shader compiler entry-point function such as <a href="https://msdn.microsoft.com/b0ca0b6a-3ff0-49ee-83de-14c4686a7104">D3DX10CompileFromFile</a>.  It is preferable to use the D3DX entry-point functions to ensure the latest version of the shader compiler will be used if you will be redistributing the DirectX redistributable libraries.




## -see-also




<a href="https://msdn.microsoft.com/c8b33c08-7b3f-4b33-9b3c-4aa2b45b8f32">Shader Functions</a>
 

 

