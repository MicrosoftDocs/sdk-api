---
UID: NF:d3d11shader.ID3D11FunctionLinkingGraph.CallFunction
title: ID3D11FunctionLinkingGraph::CallFunction
author: windows-sdk-content
description: Creates a call-function linking node to use in the function-linking-graph.
old-location: direct3d11\id3d11functionlinkinggraph_callfunction.htm
tech.root: direct3d11
ms.assetid: 0DEEE3E4-7D4E-40BD-9D96-A1C91CF5E4BE
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CallFunction, CallFunction method [Direct3D 11], CallFunction method [Direct3D 11],ID3D11FunctionLinkingGraph interface, ID3D11FunctionLinkingGraph interface [Direct3D 11],CallFunction method, ID3D11FunctionLinkingGraph.CallFunction, ID3D11FunctionLinkingGraph::CallFunction, d3d11shader/ID3D11FunctionLinkingGraph::CallFunction, direct3d11.id3d11functionlinkinggraph_callfunction
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
 - ID3D11FunctionLinkingGraph.CallFunction
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
- ID3D11FunctionLinkingGraph.CallFunction
: 
---

# ID3D11FunctionLinkingGraph::CallFunction


## -description


Creates a call-function linking node to use in the function-linking-graph.


## -parameters




### -param pModuleInstanceNamespace [in, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">LPCSTR</a></b>

The optional namespace for the function, or <b>NULL</b> if no namespace is needed.
          


### -param pModuleWithFunctionPrototype [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn280563(v=VS.85).aspx">ID3D11Module</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/en-us/library/Dn280564(v=VS.85).aspx">ID3D11ModuleInstance</a> interface for the library module that contains the function prototype.
          


### -param pFunctionName [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">LPCSTR</a></b>

The name of the function.


### -param ppCallNode [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn280562(v=VS.85).aspx">ID3D11LinkingNode</a>**</b>

A pointer to a variable that receives a pointer to the <a href="https://msdn.microsoft.com/en-us/library/Dn280562(v=VS.85).aspx">ID3D11LinkingNode</a> interface that represents the function in the function-linking-graph.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the <a href="https://msdn.microsoft.com/en-us/library/Ff476174(v=VS.85).aspx">Direct3D 11 Return Codes</a>.
          




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn280535(v=VS.85).aspx">ID3D11FunctionLinkingGraph</a>
 

 

