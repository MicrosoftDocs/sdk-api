---
UID: NF:d3dcompiler.D3DCreateFunctionLinkingGraph
title: D3DCreateFunctionLinkingGraph function (d3dcompiler.h)
description: Creates a function-linking-graph interface.
helpviewer_keywords: ["D3DCreateFunctionLinkingGraph","D3DCreateFunctionLinkingGraph function [HLSL]","d3dcompiler/D3DCreateFunctionLinkingGraph","direct3dhlsl.d3dcreatefunctionlinkinggraph"]
old-location: direct3dhlsl\d3dcreatefunctionlinkinggraph.htm
tech.root: direct3dhlsl
ms.assetid: D0BC7D62-EBF8-4144-8DC0-A87BF1B83006
ms.date: 12/05/2018
ms.keywords: D3DCreateFunctionLinkingGraph, D3DCreateFunctionLinkingGraph function [HLSL], d3dcompiler/D3DCreateFunctionLinkingGraph, direct3dhlsl.d3dcreatefunctionlinkinggraph
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
 - D3DCreateFunctionLinkingGraph
 - d3dcompiler/D3DCreateFunctionLinkingGraph
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
 - D3DCreateFunctionLinkingGraph
---

# D3DCreateFunctionLinkingGraph function


## -description

Creates a function-linking-graph interface. <div class="alert"><b>Note</b>  This function is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.
</div>
<div> </div>

## -parameters

### -param uFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Reserved

### -param ppFunctionLinkingGraph [out]

Type: <b><a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph">ID3D11FunctionLinkingGraph</a>**</b>

A pointer to a variable that receives a pointer to the <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph">ID3D11FunctionLinkingGraph</a> interface that is used for constructing shaders that consist of a sequence of precompiled function calls.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

<div class="alert"><b>Note</b>  The D3dcompiler_47.dll or later version of the DLL contains the <b>D3DCreateFunctionLinkingGraph</b> function.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/direct3dhlsl/dx-graphics-d3dcompiler-reference-functions">Functions</a>



<a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph">ID3D11FunctionLinkingGraph</a>