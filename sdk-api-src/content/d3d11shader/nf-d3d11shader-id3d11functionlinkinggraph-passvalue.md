---
UID: NF:d3d11shader.ID3D11FunctionLinkingGraph.PassValue
title: ID3D11FunctionLinkingGraph::PassValue
author: windows-sdk-content
description: Passes a value from a source linking node to a destination linking node.
old-location: direct3d11\id3d11functionlinkinggraph_passvalue.htm
old-project: direct3d11
ms.assetid: 78489B91-E56D-4338-BCCB-6807EA0E8367
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ID3D11FunctionLinkingGraph interface [Direct3D 11],PassValue method, ID3D11FunctionLinkingGraph.PassValue, ID3D11FunctionLinkingGraph::PassValue, PassValue, PassValue method [Direct3D 11], PassValue method [Direct3D 11],ID3D11FunctionLinkingGraph interface, d3d11shader/ID3D11FunctionLinkingGraph::PassValue, direct3d11.id3d11functionlinkinggraph_passvalue
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11shader.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D3D11_SHADER_VERSION_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3DCompiler_47.dll
api_name:
 - ID3D11FunctionLinkingGraph.PassValue
product: Windows
targetos: Windows
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
---

# ID3D11FunctionLinkingGraph::PassValue


## -description


Passes a value from a source linking node to a destination linking node.


## -parameters




### -param pSrcNode [in]

Type: <b><a href="https://msdn.microsoft.com/533D2DA8-107A-48B1-928F-5788DC9CF706">ID3D11LinkingNode</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/533D2DA8-107A-48B1-928F-5788DC9CF706">ID3D11LinkingNode</a> interface for the source linking node.


### -param SrcParameterIndex [in]

Type: <b>INT</b>

The zero-based index of the source parameter.


### -param pDstNode [in]

Type: <b><a href="https://msdn.microsoft.com/533D2DA8-107A-48B1-928F-5788DC9CF706">ID3D11LinkingNode</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/533D2DA8-107A-48B1-928F-5788DC9CF706">ID3D11LinkingNode</a> interface for the destination linking node.


### -param DstParameterIndex [in]

Type: <b>INT</b>

The zero-based index of the destination parameter.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/B1952085-CCD2-40F6-9A23-83B4F18FC30A">ID3D11FunctionLinkingGraph</a>
 

 

