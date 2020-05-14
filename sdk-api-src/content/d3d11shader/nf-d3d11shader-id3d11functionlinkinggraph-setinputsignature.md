---
UID: NF:d3d11shader.ID3D11FunctionLinkingGraph.SetInputSignature
title: ID3D11FunctionLinkingGraph::SetInputSignature (d3d11shader.h)
description: Sets the input signature of the function-linking-graph.helpviewer_keywords: ["ID3D11FunctionLinkingGraph interface [Direct3D 11]","SetInputSignature method","ID3D11FunctionLinkingGraph.SetInputSignature","ID3D11FunctionLinkingGraph::SetInputSignature","SetInputSignature","SetInputSignature method [Direct3D 11]","SetInputSignature method [Direct3D 11]","ID3D11FunctionLinkingGraph interface","d3d11shader/ID3D11FunctionLinkingGraph::SetInputSignature","direct3d11.id3d11functionlinkinggraph_setinputsignature"]
old-location: direct3d11\id3d11functionlinkinggraph_setinputsignature.htm
tech.root: direct3d11
ms.assetid: 9108BA38-6A0A-4438-BC63-A80790E4A5F0
ms.date: 12/05/2018
ms.keywords: ID3D11FunctionLinkingGraph interface [Direct3D 11],SetInputSignature method, ID3D11FunctionLinkingGraph.SetInputSignature, ID3D11FunctionLinkingGraph::SetInputSignature, SetInputSignature, SetInputSignature method [Direct3D 11], SetInputSignature method [Direct3D 11],ID3D11FunctionLinkingGraph interface, d3d11shader/ID3D11FunctionLinkingGraph::SetInputSignature, direct3d11.id3d11functionlinkinggraph_setinputsignature
f1_keywords:
- d3d11shader/ID3D11FunctionLinkingGraph.SetInputSignature
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D3DCompiler_47.dll
api_name:
- ID3D11FunctionLinkingGraph.SetInputSignature
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11FunctionLinkingGraph::SetInputSignature


## -description


Sets the input signature of the function-linking-graph.


## -parameters




### -param pInputParameters [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc">D3D11_PARAMETER_DESC</a>*</b>

An array of  <a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc">D3D11_PARAMETER_DESC</a> structures for the parameters of the input signature.


### -param cInputParameters [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of input parameters in the <i>pInputParameters</i> array.


### -param ppInputNode [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode">ID3D11LinkingNode</a>**</b>

A pointer to a variable that receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode">ID3D11LinkingNode</a> interface that represents the input signature of the function-linking-graph.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph">ID3D11FunctionLinkingGraph</a>
 

 

