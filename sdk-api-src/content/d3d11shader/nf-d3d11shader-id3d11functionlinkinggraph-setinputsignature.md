---
UID: NF:d3d11shader.ID3D11FunctionLinkingGraph.SetInputSignature
title: ID3D11FunctionLinkingGraph::SetInputSignature method
author: windows-driver-content
description: Sets the input signature of the function-linking-graph.
old-location: direct3d11\id3d11functionlinkinggraph_setinputsignature.htm
old-project: direct3d11
ms.assetid: 9108BA38-6A0A-4438-BC63-A80790E4A5F0
ms.author: windowsdriverdev
ms.date: 4/6/2018
ms.keywords: ID3D11FunctionLinkingGraph, ID3D11FunctionLinkingGraph interface [Direct3D 11], SetInputSignature method, ID3D11FunctionLinkingGraph::SetInputSignature, SetInputSignature method [Direct3D 11], SetInputSignature method [Direct3D 11], ID3D11FunctionLinkingGraph interface, SetInputSignature,ID3D11FunctionLinkingGraph.SetInputSignature, d3d11shader/ID3D11FunctionLinkingGraph::SetInputSignature, direct3d11.id3d11functionlinkinggraph_setinputsignature
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
req.typenames: D3D11_SHADER_VERSION_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3DCompiler_47.dll
api_name:
-	ID3D11FunctionLinkingGraph.SetInputSignature
product: Windows
targetos: Windows
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
---

# ID3D11FunctionLinkingGraph::SetInputSignature method


## -description


Sets the input signature of the function-linking-graph.


## -parameters




### -param pInputParameters [in]

Type: <b>const <a href="https://msdn.microsoft.com/C6F1079C-A686-44EA-933B-9DE2D70CFA33">D3D11_PARAMETER_DESC</a>*</b>

An array of  <a href="https://msdn.microsoft.com/C6F1079C-A686-44EA-933B-9DE2D70CFA33">D3D11_PARAMETER_DESC</a> structures for the parameters of the input signature.


### -param cInputParameters [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of input parameters in the <i>pInputParameters</i> array.


### -param ppInputNode [out]

Type: <b><a href="https://msdn.microsoft.com/533D2DA8-107A-48B1-928F-5788DC9CF706">ID3D11LinkingNode</a>**</b>

A pointer to a variable that receives a pointer to the <a href="https://msdn.microsoft.com/533D2DA8-107A-48B1-928F-5788DC9CF706">ID3D11LinkingNode</a> interface that represents the input signature of the function-linking-graph.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/B1952085-CCD2-40F6-9A23-83B4F18FC30A">ID3D11FunctionLinkingGraph</a>
 

 

