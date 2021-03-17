---
UID: NF:d3d11shader.ID3D11FunctionLinkingGraph.CreateModuleInstance
title: ID3D11FunctionLinkingGraph::CreateModuleInstance (d3d11shader.h)
description: Initializes a shader module from the function-linking-graph object.
helpviewer_keywords: ["CreateModuleInstance","CreateModuleInstance method [Direct3D 11]","CreateModuleInstance method [Direct3D 11]","ID3D11FunctionLinkingGraph interface","ID3D11FunctionLinkingGraph interface [Direct3D 11]","CreateModuleInstance method","ID3D11FunctionLinkingGraph.CreateModuleInstance","ID3D11FunctionLinkingGraph::CreateModuleInstance","d3d11shader/ID3D11FunctionLinkingGraph::CreateModuleInstance","direct3d11.id3d11functionlinkinggraph_createmoduleinstance"]
old-location: direct3d11\id3d11functionlinkinggraph_createmoduleinstance.htm
tech.root: direct3d11
ms.assetid: 7E854D31-3E34-43A7-ABEB-7FBAC94217F3
ms.date: 12/05/2018
ms.keywords: CreateModuleInstance, CreateModuleInstance method [Direct3D 11], CreateModuleInstance method [Direct3D 11],ID3D11FunctionLinkingGraph interface, ID3D11FunctionLinkingGraph interface [Direct3D 11],CreateModuleInstance method, ID3D11FunctionLinkingGraph.CreateModuleInstance, ID3D11FunctionLinkingGraph::CreateModuleInstance, d3d11shader/ID3D11FunctionLinkingGraph::CreateModuleInstance, direct3d11.id3d11functionlinkinggraph_createmoduleinstance
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
 - ID3D11FunctionLinkingGraph::CreateModuleInstance
 - d3d11shader/ID3D11FunctionLinkingGraph::CreateModuleInstance
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
 - ID3D11FunctionLinkingGraph.CreateModuleInstance
---

# ID3D11FunctionLinkingGraph::CreateModuleInstance


## -description

Initializes a shader module from the function-linking-graph object.

## -parameters

### -param ppModuleInstance [out]

Type: <b><a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance">ID3D11ModuleInstance</a>**</b>

The address of a pointer to an <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance">ID3D11ModuleInstance</a> interface for the shader module to initialize.

### -param ppErrorBuffer [out, optional]

Type: <b><a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a>**</b>

An optional pointer to a variable that receives a pointer to the <a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a> interface that you can use to access compiler error messages, or <b>NULL</b> if there are no errors.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph">ID3D11FunctionLinkingGraph</a>