---
UID: NF:d3d11shader.ID3D11FunctionLinkingGraph.PassValue
title: ID3D11FunctionLinkingGraph::PassValue (d3d11shader.h)
description: Passes a value from a source linking node to a destination linking node.
helpviewer_keywords: ["ID3D11FunctionLinkingGraph interface [Direct3D 11]","PassValue method","ID3D11FunctionLinkingGraph.PassValue","ID3D11FunctionLinkingGraph::PassValue","PassValue","PassValue method [Direct3D 11]","PassValue method [Direct3D 11]","ID3D11FunctionLinkingGraph interface","d3d11shader/ID3D11FunctionLinkingGraph::PassValue","direct3d11.id3d11functionlinkinggraph_passvalue"]
old-location: direct3d11\id3d11functionlinkinggraph_passvalue.htm
tech.root: direct3d11
ms.assetid: 78489B91-E56D-4338-BCCB-6807EA0E8367
ms.date: 12/05/2018
ms.keywords: ID3D11FunctionLinkingGraph interface [Direct3D 11],PassValue method, ID3D11FunctionLinkingGraph.PassValue, ID3D11FunctionLinkingGraph::PassValue, PassValue, PassValue method [Direct3D 11], PassValue method [Direct3D 11],ID3D11FunctionLinkingGraph interface, d3d11shader/ID3D11FunctionLinkingGraph::PassValue, direct3d11.id3d11functionlinkinggraph_passvalue
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
 - ID3D11FunctionLinkingGraph::PassValue
 - d3d11shader/ID3D11FunctionLinkingGraph::PassValue
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
 - ID3D11FunctionLinkingGraph.PassValue
---

# ID3D11FunctionLinkingGraph::PassValue


## -description

Passes a value from a source linking node to a destination linking node.

## -parameters

### -param pSrcNode [in]

Type: <b><a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode">ID3D11LinkingNode</a>*</b>

A pointer to the <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode">ID3D11LinkingNode</a> interface for the source linking node.

### -param SrcParameterIndex [in]

Type: <b>INT</b>

The zero-based index of the source parameter.

### -param pDstNode [in]

Type: <b><a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode">ID3D11LinkingNode</a>*</b>

A pointer to the <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode">ID3D11LinkingNode</a> interface for the destination linking node.

### -param DstParameterIndex [in]

Type: <b>INT</b>

The zero-based index of the destination parameter.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph">ID3D11FunctionLinkingGraph</a>