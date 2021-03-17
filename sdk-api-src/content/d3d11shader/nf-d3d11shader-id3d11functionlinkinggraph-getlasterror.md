---
UID: NF:d3d11shader.ID3D11FunctionLinkingGraph.GetLastError
title: ID3D11FunctionLinkingGraph::GetLastError (d3d11shader.h)
description: Gets the error from the last function call of the function-linking-graph.
helpviewer_keywords: ["GetLastError","GetLastError method [Direct3D 11]","GetLastError method [Direct3D 11]","ID3D11FunctionLinkingGraph interface","ID3D11FunctionLinkingGraph interface [Direct3D 11]","GetLastError method","ID3D11FunctionLinkingGraph.GetLastError","ID3D11FunctionLinkingGraph::GetLastError","d3d11shader/ID3D11FunctionLinkingGraph::GetLastError","direct3d11.id3d11functionlinkinggraph_getlasterror"]
old-location: direct3d11\id3d11functionlinkinggraph_getlasterror.htm
tech.root: direct3d11
ms.assetid: 5BD10944-5C49-4DA2-A2B7-73DA21A49A12
ms.date: 12/05/2018
ms.keywords: GetLastError, GetLastError method [Direct3D 11], GetLastError method [Direct3D 11],ID3D11FunctionLinkingGraph interface, ID3D11FunctionLinkingGraph interface [Direct3D 11],GetLastError method, ID3D11FunctionLinkingGraph.GetLastError, ID3D11FunctionLinkingGraph::GetLastError, d3d11shader/ID3D11FunctionLinkingGraph::GetLastError, direct3d11.id3d11functionlinkinggraph_getlasterror
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
 - ID3D11FunctionLinkingGraph::GetLastError
 - d3d11shader/ID3D11FunctionLinkingGraph::GetLastError
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
 - ID3D11FunctionLinkingGraph.GetLastError
---

# ID3D11FunctionLinkingGraph::GetLastError


## -description

Gets the error from the last function call of the function-linking-graph.

## -parameters

### -param ppErrorBuffer [out, optional]

Type: <b><a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a>**</b>

An pointer to a variable that receives a pointer to the <a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a> interface that you can use to access the error.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph">ID3D11FunctionLinkingGraph</a>