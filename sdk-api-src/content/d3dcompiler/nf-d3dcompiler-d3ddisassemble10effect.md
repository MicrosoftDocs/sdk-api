---
UID: NF:d3dcompiler.D3DDisassemble10Effect
title: D3DDisassemble10Effect function (d3dcompiler.h)
author: windows-sdk-content
description: Disassembles compiled HLSL code from a Direct3D10 effect.
old-location: direct3dhlsl\d3ddisassemble10effect.htm
tech.root: direct3dhlsl
ms.assetid: VS|directx_sdk|~\d3ddisassemble10effect.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 712a7486-754f-69f6-11b7-5bf288ee98af, D3DDisassemble10Effect, D3DDisassemble10Effect function [HLSL], d3dcompiler/D3DDisassemble10Effect, direct3dhlsl.d3ddisassemble10effect
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
req.lib: D3dcompiler_47.lib
req.dll: D3dcompiler_47.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - d3dcompiler_47.dll
api_name:
 - D3DDisassemble10Effect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# D3DDisassemble10Effect function


## -description


Disassembles compiled HLSL code from a Direct3D10 effect.


## -parameters




### -param pEffect [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173630(v=VS.85).aspx">ID3D10Effect</a>*</b>

A pointer to source data as compiled HLSL code.


### -param Flags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Shader <a href="http://msdn.microsoft.com/en-us/library/bb172416(VS.85).aspx">compile options</a>.


### -param ppDisassembly [out]

Type: <b><a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a>**</b>

A pointer to a buffer that receives the <a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a> interface that contains disassembly text.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 return codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd607342(v=VS.85).aspx">Functions</a>
 

 

