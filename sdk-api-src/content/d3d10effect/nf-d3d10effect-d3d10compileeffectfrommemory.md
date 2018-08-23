---
UID: NF:d3d10effect.D3D10CompileEffectFromMemory
title: D3D10CompileEffectFromMemory function
author: windows-sdk-content
description: Compile an effect.
old-location: direct3d10\d3d10compileeffectfrommemory.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10compileeffectfrommemory.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: D3D10CompileEffectFromMemory, D3D10CompileEffectFromMemory function [Direct3D 10], a15fb616-366d-0a19-dbf6-a1e603c6c9db, d3d10effect/D3D10CompileEffectFromMemory, direct3d10.d3d10compileeffectfrommemory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: d3d10effect.h
req.include-header: 
req.redist: 
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
req.typenames: D3D10_DEVICE_STATE_TYPES
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
req.lib: D3D10.lib
req.dll: D3D10.dll
req.irql: 
---

# D3D10CompileEffectFromMemory function


## -description


Compile an effect.

<div class="alert"><b>Note</b>  Use <a href="https://msdn.microsoft.com/en-us/library/Bb310587(v=VS.85).aspx">D3DX10CompileFromMemory</a> instead of this function.</div><div> </div>

## -parameters




### -param pData [in]

Type: <b>void*</b>

A pointer to effect data; either ASCII <a href="https://msdn.microsoft.com/en-us/library/Bb509638(v=VS.85).aspx">HLSL</a> code or a compiled effect.


### -param DataLength [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

Length of <i>pData</i>.


### -param pSrcFileName [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The name of the effect file.


### -param pDefines [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Bb172436(v=VS.85).aspx">D3D10_SHADER_MACRO</a>*</b>

Optional. An array of NULL-terminated macro definitions (see <a href="https://msdn.microsoft.com/en-us/library/Bb172436(v=VS.85).aspx">D3D10_SHADER_MACRO</a>).


### -param pInclude [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173775(v=VS.85).aspx">ID3D10Include</a>*</b>

Optional. A pointer to an <a href="https://msdn.microsoft.com/en-us/library/Bb173775(v=VS.85).aspx">ID3D10Include Interface</a> for handling include files. Setting this to <b>NULL</b> will cause a compile error if a shader contains a #include.


### -param HLSLFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Shader <a href="https://msdn.microsoft.com/en-us/library/Bb172416(v=VS.85).aspx">compile options</a>.


### -param FXFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Effect <a href="https://msdn.microsoft.com/en-us/library/Bb205176(v=VS.85).aspx">compile options</a>.


### -param ppCompiledEffect [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn933260(v=VS.85).aspx">ID3D10Blob</a>**</b>

The address of a <a href="https://msdn.microsoft.com/en-us/library/Dn933260(v=VS.85).aspx">ID3D10Blob Interface</a> that contains the compiled effect.


### -param ppErrors [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn933260(v=VS.85).aspx">ID3D10Blob</a>**</b>

Optional. A pointer to an <a href="https://msdn.microsoft.com/en-us/library/Dn933260(v=VS.85).aspx">ID3D10Blob Interface</a> that contains compiler error messages, or <b>NULL</b> if there were no errors.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



This function uses the version of the HLSL compiler released in the November 2006 DirectX SDK.

For an example, see <a href="https://msdn.microsoft.com/en-us/library/Bb205078(v=VS.85).aspx">Compile an Effect (Direct3D 10)</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205177(v=VS.85).aspx">Effect Functions (Direct3D 10)</a>
 

 

