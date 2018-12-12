---
UID: NF:d3d10effect.D3D10CompileEffectFromMemory
title: D3D10CompileEffectFromMemory function
author: windows-sdk-content
description: Compile an effect.
old-location: direct3d10\d3d10compileeffectfrommemory.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10compileeffectfrommemory.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D10CompileEffectFromMemory, D3D10CompileEffectFromMemory function [Direct3D 10], a15fb616-366d-0a19-dbf6-a1e603c6c9db, d3d10effect/D3D10CompileEffectFromMemory, direct3d10.d3d10compileeffectfrommemory
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3D10.dll
api_name:
 - D3D10CompileEffectFromMemory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# D3D10CompileEffectFromMemory function


## -description


Compile an effect.

<div class="alert"><b>Note</b>  Use <a href="https://msdn.microsoft.com/c6458d82-a649-402c-8180-5b7320f9fdb0">D3DX10CompileFromMemory</a> instead of this function.</div><div> </div>

## -parameters




### -param pData [in]

Type: <b>void*</b>

A pointer to effect data; either ASCII <a href="https://msdn.microsoft.com/1d0e12ff-8559-4e5c-9914-6ed313ea5464">HLSL</a> code or a compiled effect.


### -param DataLength [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

Length of <i>pData</i>.


### -param pSrcFileName [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The name of the effect file.


### -param pDefines [in]

Type: <b>const <a href="https://msdn.microsoft.com/35953846-a07e-4ca3-91d9-3ddb3944614d">D3D10_SHADER_MACRO</a>*</b>

Optional. An array of NULL-terminated macro definitions (see <a href="https://msdn.microsoft.com/35953846-a07e-4ca3-91d9-3ddb3944614d">D3D10_SHADER_MACRO</a>).


### -param pInclude [in]

Type: <b><a href="https://msdn.microsoft.com/9e8a6b37-0b0c-46d1-aa4a-35efc07f1a6b">ID3D10Include</a>*</b>

Optional. A pointer to an <a href="https://msdn.microsoft.com/9e8a6b37-0b0c-46d1-aa4a-35efc07f1a6b">ID3D10Include Interface</a> for handling include files. Setting this to <b>NULL</b> will cause a compile error if a shader contains a #include.


### -param HLSLFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Shader <a href="https://msdn.microsoft.com/418633d8-47ee-40d0-9b80-89aa860f2e8b">compile options</a>.


### -param FXFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Effect <a href="https://msdn.microsoft.com/434bcff8-47ea-480d-bc0b-44d3ed1f8cce">compile options</a>.


### -param ppCompiledEffect [out]

Type: <b><a href="https://msdn.microsoft.com/d180fee0-1a69-4250-a0c4-d6e3754f063a">ID3D10Blob</a>**</b>

The address of a <a href="https://msdn.microsoft.com/d180fee0-1a69-4250-a0c4-d6e3754f063a">ID3D10Blob Interface</a> that contains the compiled effect.


### -param ppErrors [out]

Type: <b><a href="https://msdn.microsoft.com/d180fee0-1a69-4250-a0c4-d6e3754f063a">ID3D10Blob</a>**</b>

Optional. A pointer to an <a href="https://msdn.microsoft.com/d180fee0-1a69-4250-a0c4-d6e3754f063a">ID3D10Blob Interface</a> that contains compiler error messages, or <b>NULL</b> if there were no errors.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



This function uses the version of the HLSL compiler released in the November 2006 DirectX SDK.

For an example, see <a href="https://msdn.microsoft.com/b8d8a0b7-b520-44e4-8691-6eb46202c092">Compile an Effect (Direct3D 10)</a>.




## -see-also




<a href="https://msdn.microsoft.com/b76643f0-387f-49c6-80e5-4d7b406b4db7">Effect Functions (Direct3D 10)</a>
 

 

