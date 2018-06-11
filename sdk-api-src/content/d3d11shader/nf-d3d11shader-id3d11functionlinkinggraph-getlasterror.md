---
UID: NF:d3d11shader.ID3D11FunctionLinkingGraph.GetLastError
title: ID3D11FunctionLinkingGraph::GetLastError
author: windows-sdk-content
description: Gets the error from the last function call of the function-linking-graph.
old-location: direct3d11\id3d11functionlinkinggraph_getlasterror.htm
old-project: direct3d11
ms.assetid: 5BD10944-5C49-4DA2-A2B7-73DA21A49A12
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: GetLastError, GetLastError method [Direct3D 11], GetLastError method [Direct3D 11],ID3D11FunctionLinkingGraph interface, ID3D11FunctionLinkingGraph interface [Direct3D 11],GetLastError method, ID3D11FunctionLinkingGraph.GetLastError, ID3D11FunctionLinkingGraph::GetLastError, d3d11shader/ID3D11FunctionLinkingGraph::GetLastError, direct3d11.id3d11functionlinkinggraph_getlasterror
ms.prod: windows
ms.technology: windows-sdk
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
 - ID3D11FunctionLinkingGraph.GetLastError
product: Windows
targetos: Windows
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
---

# ID3D11FunctionLinkingGraph::GetLastError


## -description


Gets the error from the last function call of the function-linking-graph.


## -parameters




### -param ppErrorBuffer [out, optional]

Type: <b><a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a>**</b>


            An pointer to a variable that receives a pointer to the <a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a> interface that you can use to access the error.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>


            Returns S_OK if successful; otherwise, returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.
          




## -see-also




<a href="https://msdn.microsoft.com/B1952085-CCD2-40F6-9A23-83B4F18FC30A">ID3D11FunctionLinkingGraph</a>
 

 

