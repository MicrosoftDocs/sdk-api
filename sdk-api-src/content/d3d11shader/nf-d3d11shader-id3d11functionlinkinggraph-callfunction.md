---
UID: NF:d3d11shader.ID3D11FunctionLinkingGraph.CallFunction
title: ID3D11FunctionLinkingGraph::CallFunction
author: windows-sdk-content
description: Creates a call-function linking node to use in the function-linking-graph.
old-location: direct3d11\id3d11functionlinkinggraph_callfunction.htm
tech.root: direct3d11
ms.assetid: 0DEEE3E4-7D4E-40BD-9D96-A1C91CF5E4BE
ms.author: windowssdkdev
ms.date: 11/16/2018
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
---

# ID3D11FunctionLinkingGraph::CallFunction


## -description


Creates a call-function linking node to use in the function-linking-graph.


## -parameters




### -param pModuleInstanceNamespace [in, optional]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The optional namespace for the function, or <b>NULL</b> if no namespace is needed.
          


### -param pModuleWithFunctionPrototype [in]

Type: <b><a href="https://msdn.microsoft.com/5915DACB-1D3A-496C-96C6-77D85CC6560B">ID3D11Module</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/BBC64078-FCA8-4868-B9CD-3E6F3C86BFC5">ID3D11ModuleInstance</a> interface for the library module that contains the function prototype.
          


### -param pFunctionName [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The name of the function.


### -param ppCallNode [out]

Type: <b><a href="https://msdn.microsoft.com/533D2DA8-107A-48B1-928F-5788DC9CF706">ID3D11LinkingNode</a>**</b>

A pointer to a variable that receives a pointer to the <a href="https://msdn.microsoft.com/533D2DA8-107A-48B1-928F-5788DC9CF706">ID3D11LinkingNode</a> interface that represents the function in the function-linking-graph.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.
          




## -see-also




<a href="https://msdn.microsoft.com/B1952085-CCD2-40F6-9A23-83B4F18FC30A">ID3D11FunctionLinkingGraph</a>
 

 

