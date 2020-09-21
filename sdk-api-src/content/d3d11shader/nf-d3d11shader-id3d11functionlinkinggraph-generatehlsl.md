---
UID: NF:d3d11shader.ID3D11FunctionLinkingGraph.GenerateHlsl
title: ID3D11FunctionLinkingGraph::GenerateHlsl (d3d11shader.h)
description: Generates Microsoft High Level Shader Language (HLSL) shader code that represents the function-linking-graph.
helpviewer_keywords: ["GenerateHlsl","GenerateHlsl method [Direct3D 11]","GenerateHlsl method [Direct3D 11]","ID3D11FunctionLinkingGraph interface","ID3D11FunctionLinkingGraph interface [Direct3D 11]","GenerateHlsl method","ID3D11FunctionLinkingGraph.GenerateHlsl","ID3D11FunctionLinkingGraph::GenerateHlsl","d3d11shader/ID3D11FunctionLinkingGraph::GenerateHlsl","direct3d11.id3d11functionlinkinggraph_generatehlsl"]
old-location: direct3d11\id3d11functionlinkinggraph_generatehlsl.htm
tech.root: direct3d11
ms.assetid: CD3B815A-0D18-4568-BCDF-7E2D5F1C139F
ms.date: 12/05/2018
ms.keywords: GenerateHlsl, GenerateHlsl method [Direct3D 11], GenerateHlsl method [Direct3D 11],ID3D11FunctionLinkingGraph interface, ID3D11FunctionLinkingGraph interface [Direct3D 11],GenerateHlsl method, ID3D11FunctionLinkingGraph.GenerateHlsl, ID3D11FunctionLinkingGraph::GenerateHlsl, d3d11shader/ID3D11FunctionLinkingGraph::GenerateHlsl, direct3d11.id3d11functionlinkinggraph_generatehlsl
req.header: d3d11shader.h
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
 - ID3D11FunctionLinkingGraph::GenerateHlsl
 - d3d11shader/ID3D11FunctionLinkingGraph::GenerateHlsl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3DCompiler_47.dll
api_name:
 - ID3D11FunctionLinkingGraph.GenerateHlsl
---

# ID3D11FunctionLinkingGraph::GenerateHlsl


## -description

Generates Microsoft High Level Shader Language (HLSL) shader code that represents the function-linking-graph.

## -parameters

### -param uFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Reserved

### -param ppBuffer [out]

Type: <b><a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a>**</b>

An pointer to a variable that receives a pointer to the <a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a> interface that you can use to access the HLSL shader source code that represents the function-linking-graph. You can compile this HLSL code, but first you must  add code or include statements for the functions called in the function-linking-graph.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph">ID3D11FunctionLinkingGraph</a>