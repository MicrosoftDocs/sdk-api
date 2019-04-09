---
UID: NF:d3d11shader.ID3D11FunctionLinkingGraph.CreateModuleInstance
title: ID3D11FunctionLinkingGraph::CreateModuleInstance (d3d11shader.h)
author: windows-sdk-content
description: Initializes a shader module from the function-linking-graph object.
old-location: direct3d11\id3d11functionlinkinggraph_createmoduleinstance.htm
tech.root: direct3d11
ms.assetid: 7E854D31-3E34-43A7-ABEB-7FBAC94217F3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateModuleInstance, CreateModuleInstance method [Direct3D 11], CreateModuleInstance method [Direct3D 11],ID3D11FunctionLinkingGraph interface, ID3D11FunctionLinkingGraph interface [Direct3D 11],CreateModuleInstance method, ID3D11FunctionLinkingGraph.CreateModuleInstance, ID3D11FunctionLinkingGraph::CreateModuleInstance, d3d11shader/ID3D11FunctionLinkingGraph::CreateModuleInstance, direct3d11.id3d11functionlinkinggraph_createmoduleinstance
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
 - ID3D11FunctionLinkingGraph.CreateModuleInstance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11FunctionLinkingGraph::CreateModuleInstance


## -description


Initializes a shader module from the function-linking-graph object.


## -parameters




### -param ppModuleInstance [out]

Type: <b><a href="https://msdn.microsoft.com/BBC64078-FCA8-4868-B9CD-3E6F3C86BFC5">ID3D11ModuleInstance</a>**</b>

The address of a pointer to an <a href="https://msdn.microsoft.com/BBC64078-FCA8-4868-B9CD-3E6F3C86BFC5">ID3D11ModuleInstance</a> interface for the shader module to initialize.


### -param ppErrorBuffer [out, optional]

Type: <b><a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a>**</b>

An optional pointer to a variable that receives a pointer to the <a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a> interface that you can use to access compiler error messages, or <b>NULL</b> if there are no errors.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/B1952085-CCD2-40F6-9A23-83B4F18FC30A">ID3D11FunctionLinkingGraph</a>
 

 

