---
UID: NS:d3d12sdklayers.D3D12_INFO_QUEUE_FILTER_DESC
title: D3D12_INFO_QUEUE_FILTER_DESC (d3d12sdklayers.h)
author: windows-sdk-content
description: Allow or deny certain types of messages to pass through a filter.
old-location: direct3d12\d3d12_info_queue_filter_desc.htm
tech.root: direct3d12
ms.assetid: 079494EC-3FC3-490D-B2BC-0FBD976ECC97
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D12_INFO_QUEUE_FILTER_DESC, D3D12_INFO_QUEUE_FILTER_DESC structure, d3d12sdklayers/D3D12_INFO_QUEUE_FILTER_DESC, direct3d12.d3d12_info_queue_filter_desc
ms.topic: struct
f1_keywords: 
 - "d3d12sdklayers/D3D12_INFO_QUEUE_FILTER_DESC"
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
targetos: Windows
req.typenames: D3D12_INFO_QUEUE_FILTER_DESC
req.redist: 
ms.custom: 19H1
---

# D3D12_INFO_QUEUE_FILTER_DESC structure


## -description


Allow or deny certain types of messages to pass through a filter.


## -struct-fields




### -field NumCategories

Number of message categories to allow or deny.




### -field pCategoryList

Array of message categories to allow or deny. Array must have at least <i>NumCategories</i> members (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_category">D3D12_MESSAGE_CATEGORY</a>).




### -field NumSeverities

Number of message severity levels to allow or deny.




### -field pSeverityList

Array of message severity levels to allow or deny. Array must have at least <i>NumSeverities</i> members (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_severity">D3D12_MESSAGE_SEVERITY</a>).




### -field NumIDs

Number of message IDs to allow or deny.


          


### -field pIDList

Array of message IDs to allow or deny. Array must have at least <i>NumIDs</i> members (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_id">D3D12_MESSAGE_ID</a>).


          


## -remarks



For use with an <a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue">ID3D12InfoQueue</a> Interface.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-sdklayers-structures">Debug Layer Structures</a>
 

 

