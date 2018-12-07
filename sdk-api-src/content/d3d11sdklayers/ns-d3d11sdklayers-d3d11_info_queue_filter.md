---
UID: NS:d3d11sdklayers.D3D11_INFO_QUEUE_FILTER
title: D3D11_INFO_QUEUE_FILTER
author: windows-sdk-content
description: Debug message filter; contains a lists of message types to allow or deny.
old-location: direct3d11\d3d11_info_queue_filter.htm
tech.root: direct3d11
ms.assetid: 6ff12751-86dd-4ae0-b532-661a70dad21f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 9211ecf7-c9cd-c8c2-618a-e4909600a06e, D3D11_INFO_QUEUE_FILTER, D3D11_INFO_QUEUE_FILTER structure [Direct3D 11], d3d11sdklayers/D3D11_INFO_QUEUE_FILTER, direct3d11.d3d11_info_queue_filter
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: D3D11_INFO_QUEUE_FILTER
req.redist: 
---

# D3D11_INFO_QUEUE_FILTER structure


## -description


Debug message filter; contains a lists of message types to allow or deny.


## -struct-fields




### -field AllowList

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476178(v=VS.85).aspx">D3D11_INFO_QUEUE_FILTER_DESC</a></b>

Types of messages that you want to allow. See <a href="https://msdn.microsoft.com/en-us/library/Ff476178(v=VS.85).aspx">D3D11_INFO_QUEUE_FILTER_DESC</a>.


### -field DenyList

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476178(v=VS.85).aspx">D3D11_INFO_QUEUE_FILTER_DESC</a></b>

Types of messages that you want to deny.


## -remarks



For use with an <a href="https://msdn.microsoft.com/en-us/library/Ff476538(v=VS.85).aspx">ID3D11InfoQueue Interface</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476155(v=VS.85).aspx">Core Structures</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476159(v=VS.85).aspx">Layer Structures</a>
 

 

