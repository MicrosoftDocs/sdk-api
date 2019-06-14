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
ms.custom: 19H1
---

# D3DDisassemble10Effect function


## -description


Disassembles compiled HLSL code from a Direct3D10 effect.


## -parameters




### -param pEffect [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect">ID3D10Effect</a>*</b>

A pointer to source data as compiled HLSL code.


### -param Flags [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Shader <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-shader">compile options</a>.


### -param ppDisassembly [out]

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a>**</b>

A pointer to a buffer that receives the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a> interface that contains disassembly text.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns one of the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 return codes</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/dx-graphics-d3dcompiler-reference-functions">Functions</a>
 

 

