---
UID: NS:d3d12.D3D12_QUERY_HEAP_DESC
title: D3D12_QUERY_HEAP_DESC (d3d12.h)
author: windows-sdk-content
description: Describes the purpose of a query heap. A query heap contains an array of individual queries.
old-location: direct3d12\d3d12_query_heap_desc.htm
tech.root: direct3d12
ms.assetid: 1B1CB0D8-B370-4D38-BDA9-21C58D6A8F15
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D12_QUERY_HEAP_DESC, D3D12_QUERY_HEAP_DESC structure, d3d12/D3D12_QUERY_HEAP_DESC, direct3d12.d3d12_query_heap_desc
ms.topic: struct
req.header: d3d12.h
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
 - D3D12.h
api_name:
 - D3D12_QUERY_HEAP_DESC
product: Windows
targetos: Windows
req.typenames: D3D12_QUERY_HEAP_DESC
req.redist: 
ms.custom: 19H1
---

# D3D12_QUERY_HEAP_DESC structure


## -description


Describes the purpose of a query heap. 
          A query heap contains an array of individual queries.
        


## -struct-fields




### -field Type

Specifies one member of <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type">D3D12_QUERY_HEAP_TYPE</a>.
          


### -field Count

Specifies the number of queries the heap should contain.
          


### -field NodeMask

For single GPU operation, set this to zero. If there are multiple GPU nodes, set a bit to identify the node (the  device's physical adapter) to which the query heap applies.
            Each bit in the mask corresponds to a single node.
            Only 1 bit must be set.
          Refer to <a href="https://docs.microsoft.com/windows/desktop/direct3d12/mulit-engine">Multi-Adapter</a>.


## -remarks



Use this structure with <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createqueryheap">CreateQueryHeap</a>.
        




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>
 

 

