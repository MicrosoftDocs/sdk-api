---
UID: NF:d3d11shader.ID3D11FunctionLinkingGraph.PassValueWithSwizzle
title: ID3D11FunctionLinkingGraph::PassValueWithSwizzle
author: windows-sdk-content
description: Passes a value with swizzle from a source linking node to a destination linking node.
old-location: direct3d11\id3d11functionlinkinggraph_passvaluewithswizzle.htm
old-project: direct3d11
ms.assetid: 3D74F848-A58D-4FE9-89D3-7F02A8C86A61
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: ID3D11FunctionLinkingGraph interface [Direct3D 11],PassValueWithSwizzle method, ID3D11FunctionLinkingGraph.PassValueWithSwizzle, ID3D11FunctionLinkingGraph::PassValueWithSwizzle, PassValueWithSwizzle, PassValueWithSwizzle method [Direct3D 11], PassValueWithSwizzle method [Direct3D 11],ID3D11FunctionLinkingGraph interface, d3d11shader/ID3D11FunctionLinkingGraph::PassValueWithSwizzle, direct3d11.id3d11functionlinkinggraph_passvaluewithswizzle
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
 - ID3D11FunctionLinkingGraph.PassValueWithSwizzle
product: Windows
targetos: Windows
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
---

# ID3D11FunctionLinkingGraph::PassValueWithSwizzle


## -description


Passes a value with swizzle from a source linking node to a destination linking node.


## -parameters




### -param pSrcNode [in]

Type: <b><a href="https://msdn.microsoft.com/533D2DA8-107A-48B1-928F-5788DC9CF706">ID3D11LinkingNode</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/533D2DA8-107A-48B1-928F-5788DC9CF706">ID3D11LinkingNode</a> interface for the source linking node.


### -param SrcParameterIndex [in]

Type: <b>INT</b>

The zero-based index of the source parameter.


### -param pSrcSwizzle [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The name of the source swizzle.


### -param pDstNode [in]

Type: <b><a href="https://msdn.microsoft.com/533D2DA8-107A-48B1-928F-5788DC9CF706">ID3D11LinkingNode</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/533D2DA8-107A-48B1-928F-5788DC9CF706">ID3D11LinkingNode</a> interface for the destination linking node.


### -param DstParameterIndex [in]

Type: <b>INT</b>

The zero-based index of the destination parameter.


### -param pDstSwizzle [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The name of the destination swizzle.


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/windows/desktop/455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/B1952085-CCD2-40F6-9A23-83B4F18FC30A">ID3D11FunctionLinkingGraph</a>
 

 

