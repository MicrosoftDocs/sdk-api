---
UID: NS:d3d12sdklayers.D3D12_INFO_QUEUE_FILTER_DESC
title: D3D12_INFO_QUEUE_FILTER_DESC
author: windows-sdk-content
description: Allow or deny certain types of messages to pass through a filter.
old-location: direct3d12\d3d12_info_queue_filter_desc.htm
tech.root: direct3d12
ms.assetid: 079494EC-3FC3-490D-B2BC-0FBD976ECC97
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: D3D12_INFO_QUEUE_FILTER_DESC, D3D12_INFO_QUEUE_FILTER_DESC structure, d3d12sdklayers/D3D12_INFO_QUEUE_FILTER_DESC, direct3d12.d3d12_info_queue_filter_desc
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
 - D3D12_INFO_QUEUE_FILTER_DESC
product: Windows
targetos: Windows
req.typenames: D3D12_INFO_QUEUE_FILTER_DESC
req.redist: 
---

# D3D12_INFO_QUEUE_FILTER_DESC structure


## -description


Allow or deny certain types of messages to pass through a filter.


## -struct-fields




### -field NumCategories

Number of message categories to allow or deny.




### -field pCategoryList

Array of message categories to allow or deny. Array must have at least <i>NumCategories</i> members (see <a href="https://msdn.microsoft.com/297923A3-CE6A-46AF-B8B6-E2AE0C1920CC">D3D12_MESSAGE_CATEGORY</a>).




### -field NumSeverities

Number of message severity levels to allow or deny.




### -field pSeverityList

Array of message severity levels to allow or deny. Array must have at least <i>NumSeverities</i> members (see <a href="https://msdn.microsoft.com/44D94C37-4BA8-49FC-BEEF-6666AD59B627">D3D12_MESSAGE_SEVERITY</a>).




### -field NumIDs

Number of message IDs to allow or deny.


          


### -field pIDList

Array of message IDs to allow or deny. Array must have at least <i>NumIDs</i> members (see <a href="https://msdn.microsoft.com/95681EB0-C00B-42C8-91E1-1D1F657C886B">D3D12_MESSAGE_ID</a>).


          


## -remarks



For use with an <a href="https://msdn.microsoft.com/61667AAC-05AC-4745-8992-E9377641D411">ID3D12InfoQueue</a> Interface.




## -see-also




<a href="https://msdn.microsoft.com/FE8796A7-98D1-4333-8755-2A47567560B3">Debug Layer Structures</a>
 

 

