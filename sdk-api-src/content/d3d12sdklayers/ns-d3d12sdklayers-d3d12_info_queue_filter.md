---
UID: NS:d3d12sdklayers.D3D12_INFO_QUEUE_FILTER
title: D3D12_INFO_QUEUE_FILTER
author: windows-sdk-content
description: Debug message filter; contains a lists of message types to allow or deny.
old-location: direct3d12\d3d12_info_queue_filter.htm
tech.root: direct3d12
ms.assetid: 5CD64E71-8530-43FB-B441-25C61ED6F317
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: D3D12_INFO_QUEUE_FILTER, D3D12_INFO_QUEUE_FILTER structure, d3d12sdklayers/D3D12_INFO_QUEUE_FILTER, direct3d12.d3d12_info_queue_filter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d12sdklayers.h
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
 - d3d12sdklayers.h
api_name:
 - D3D12_INFO_QUEUE_FILTER
product: Windows
targetos: Windows
req.typenames: D3D12_INFO_QUEUE_FILTER
req.redist: 
---

# D3D12_INFO_QUEUE_FILTER structure


## -description


Debug message filter; contains a lists of message types to allow or deny.


## -struct-fields




### -field AllowList

Specifies types of messages that you want to allow. See <a href="https://msdn.microsoft.com/en-us/library/Dn950143(v=VS.85).aspx">D3D12_INFO_QUEUE_FILTER_DESC</a>.


          


### -field DenyList

Specifies types of messages that you want to deny.


          


## -remarks



For use with an <a href="https://msdn.microsoft.com/en-us/library/Dn950163(v=VS.85).aspx">ID3D12InfoQueue</a> Interface.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn950152(v=VS.85).aspx">Debug Layer Structures</a>
 

 

