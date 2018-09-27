---
UID: NS:d3d12sdklayers.D3D12_INFO_QUEUE_FILTER
title: D3D12_INFO_QUEUE_FILTER
author: windows-sdk-content
description: Debug message filter; contains a lists of message types to allow or deny.
old-location: direct3d12\d3d12_info_queue_filter.htm
tech.root: direct3d12
ms.assetid: 5CD64E71-8530-43FB-B441-25C61ED6F317
ms.author: windowssdkdev
ms.date: 09/26/2018
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

Specifies types of messages that you want to allow. See <a href="https://msdn.microsoft.com/079494EC-3FC3-490D-B2BC-0FBD976ECC97">D3D12_INFO_QUEUE_FILTER_DESC</a>.


          


### -field DenyList

Specifies types of messages that you want to deny.


          


## -remarks



For use with an <a href="https://msdn.microsoft.com/61667AAC-05AC-4745-8992-E9377641D411">ID3D12InfoQueue</a> Interface.




## -see-also




<a href="https://msdn.microsoft.com/FE8796A7-98D1-4333-8755-2A47567560B3">Debug Layer Structures</a>
 

 

