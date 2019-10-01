---
UID: NS:d3d12.D3D12_QUERY_DATA_SO_STATISTICS
title: D3D12_QUERY_DATA_SO_STATISTICS (d3d12.h)
author: windows-sdk-content
description: Describes query data for stream output.
old-location: direct3d12\d3d12_query_data_so_statistics.htm
tech.root: direct3d12
ms.assetid: 7A71F6DA-AAC2-4070-90E9-F91F090AD1A1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D12_QUERY_DATA_SO_STATISTICS, D3D12_QUERY_DATA_SO_STATISTICS structure, d3d12/D3D12_QUERY_DATA_SO_STATISTICS, direct3d12.d3d12_query_data_so_statistics
ms.topic: struct
f1_keywords: 
 - "d3d12/D3D12_QUERY_DATA_SO_STATISTICS"
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
 - D3D12_QUERY_DATA_SO_STATISTICS
targetos: Windows
req.typenames: D3D12_QUERY_DATA_SO_STATISTICS
req.redist: 
ms.custom: 19H1
---

# D3D12_QUERY_DATA_SO_STATISTICS structure


## -description


Describes query data for stream output.


## -struct-fields




### -field NumPrimitivesWritten

Specifies the number of primitives written.


### -field PrimitivesStorageNeeded

Specifies the total amount of storage needed by the primitives.


## -remarks



Use this structure with <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type">D3D12_QUERY_HEAP_TYPE</a> and <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createqueryheap">CreateQueryHeap</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>
 

 

