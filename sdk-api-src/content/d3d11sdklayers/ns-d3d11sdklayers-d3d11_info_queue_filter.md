---
UID: NS:d3d11sdklayers.D3D11_INFO_QUEUE_FILTER
title: D3D11_INFO_QUEUE_FILTER
author: windows-sdk-content
description: Debug message filter; contains a lists of message types to allow or deny.
old-location: direct3d11\d3d11_info_queue_filter.htm
old-project: direct3d11
ms.assetid: 6ff12751-86dd-4ae0-b532-661a70dad21f
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: 9211ecf7-c9cd-c8c2-618a-e4909600a06e, D3D11_INFO_QUEUE_FILTER, D3D11_INFO_QUEUE_FILTER structure [Direct3D 11], d3d11sdklayers/D3D11_INFO_QUEUE_FILTER, direct3d11.d3d11_info_queue_filter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d11sdklayers.h
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
req.typenames: D3D11_INFO_QUEUE_FILTER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11SDKLayers.h
api_name:
 - D3D11_INFO_QUEUE_FILTER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_INFO_QUEUE_FILTER structure


## -description


Debug message filter; contains a lists of message types to allow or deny.


## -struct-fields




### -field AllowList

Type: <b><a href="https://msdn.microsoft.com/265aa51a-7352-4d3a-b523-9e497e1e6a94">D3D11_INFO_QUEUE_FILTER_DESC</a></b>

Types of messages that you want to allow. See <a href="https://msdn.microsoft.com/265aa51a-7352-4d3a-b523-9e497e1e6a94">D3D11_INFO_QUEUE_FILTER_DESC</a>.


### -field DenyList

Type: <b><a href="https://msdn.microsoft.com/265aa51a-7352-4d3a-b523-9e497e1e6a94">D3D11_INFO_QUEUE_FILTER_DESC</a></b>

Types of messages that you want to deny.


## -remarks



For use with an <a href="https://msdn.microsoft.com/240820c7-1c1f-4e2d-8b3e-497fd931d7d2">ID3D11InfoQueue Interface</a>.




## -see-also




<a href="https://msdn.microsoft.com/2a45182a-7114-4075-b8b8-147f52fe7aa9">Core Structures</a>



<a href="https://msdn.microsoft.com/65f0830f-f009-47fb-b04e-24790e677338">Layer Structures</a>
 

 

