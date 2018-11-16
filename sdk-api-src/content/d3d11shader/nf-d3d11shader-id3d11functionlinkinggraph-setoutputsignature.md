---
UID: NF:d3d11shader.ID3D11FunctionLinkingGraph.SetOutputSignature
title: ID3D11FunctionLinkingGraph::SetOutputSignature
author: windows-sdk-content
description: Sets the output signature of the function-linking-graph.
old-location: direct3d11\id3d11functionlinkinggraph_setoutputsignature.htm
tech.root: direct3d11
ms.assetid: C32E3BF1-E08C-4949-A8DE-4359704D2E40
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ID3D11FunctionLinkingGraph interface [Direct3D 11],SetOutputSignature method, ID3D11FunctionLinkingGraph.SetOutputSignature, ID3D11FunctionLinkingGraph::SetOutputSignature, SetOutputSignature, SetOutputSignature method [Direct3D 11], SetOutputSignature method [Direct3D 11],ID3D11FunctionLinkingGraph interface, d3d11shader/ID3D11FunctionLinkingGraph::SetOutputSignature, direct3d11.id3d11functionlinkinggraph_setoutputsignature
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ID3D11FunctionLinkingGraph.SetOutputSignature
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d11shader.h
: 
- ID3D11FunctionLinkingGraph.SetOutputSignature
: 
---

# ID3D11FunctionLinkingGraph::SetOutputSignature


## -description


Sets the output signature of the function-linking-graph.


## -parameters




### -param pOutputParameters [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Dn280419(v=VS.85).aspx">D3D11_PARAMETER_DESC</a>*</b>

An array of  <a href="https://msdn.microsoft.com/en-us/library/Dn280419(v=VS.85).aspx">D3D11_PARAMETER_DESC</a> structures for the parameters of the output signature.


### -param cOutputParameters [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The number of output parameters in the <i>pOutputParameters</i> array.


### -param ppOutputNode [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn280562(v=VS.85).aspx">ID3D11LinkingNode</a>**</b>

A pointer to a variable that receives a pointer to the <a href="https://msdn.microsoft.com/en-us/library/Dn280562(v=VS.85).aspx">ID3D11LinkingNode</a> interface that represents the output signature of the function-linking-graph.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the <a href="https://msdn.microsoft.com/en-us/library/Ff476174(v=VS.85).aspx">Direct3D 11 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn280535(v=VS.85).aspx">ID3D11FunctionLinkingGraph</a>
 

 

