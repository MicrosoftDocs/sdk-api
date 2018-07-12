---
UID: NE:d3d12.D3D12_QUERY_HEAP_TYPE
title: D3D12_QUERY_HEAP_TYPE
author: windows-sdk-content
description: Specifies the type of query heap to create.
old-location: direct3d12\d3d12_query_heap_type.htm
old-project: direct3d12
ms.assetid: FDD5F81B-F356-49D9-B6FE-FE2847934E61
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: D3D12_QUERY_HEAP_TYPE, D3D12_QUERY_HEAP_TYPE enumeration, D3D12_QUERY_HEAP_TYPE_COPY_QUEUE_TIMESTAMP, D3D12_QUERY_HEAP_TYPE_OCCLUSION, D3D12_QUERY_HEAP_TYPE_PIPELINE_STATISTICS, D3D12_QUERY_HEAP_TYPE_SO_STATISTICS, D3D12_QUERY_HEAP_TYPE_TIMESTAMP, D3D12_QUERY_HEAP_TYPE_VIDEO_DECODE_STATISTICS, d3d12/D3D12_QUERY_HEAP_TYPE, d3d12/D3D12_QUERY_HEAP_TYPE_COPY_QUEUE_TIMESTAMP, d3d12/D3D12_QUERY_HEAP_TYPE_OCCLUSION, d3d12/D3D12_QUERY_HEAP_TYPE_PIPELINE_STATISTICS, d3d12/D3D12_QUERY_HEAP_TYPE_SO_STATISTICS, d3d12/D3D12_QUERY_HEAP_TYPE_TIMESTAMP, d3d12/D3D12_QUERY_HEAP_TYPE_VIDEO_DECODE_STATISTICS, direct3d12.d3d12_query_heap_type
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: D3D12_QUERY_HEAP_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_QUERY_HEAP_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_QUERY_HEAP_TYPE enumeration


## -description


Specifies the type of query heap to create.


## -enum-fields




### -field D3D12_QUERY_HEAP_TYPE_OCCLUSION

This returns a binary 0/1 result:  0 indicates that no samples passed depth and stencil testing, 1 indicates that at least one sample passed depth and stencil testing.  This enables occlusion queries to not interfere with any GPU performance optimization associated with depth/stencil testing.  


### -field D3D12_QUERY_HEAP_TYPE_TIMESTAMP

Indicates that the heap is for high-performance timing data. 


### -field D3D12_QUERY_HEAP_TYPE_PIPELINE_STATISTICS

Indicates the heap is to contain pipeline data. Refer to <a href="https://msdn.microsoft.com/0A84A3C8-0F6F-420E-88C9-26EC03F03179">D3D12_QUERY_DATA_PIPELINE_STATISTICS</a>.


### -field D3D12_QUERY_HEAP_TYPE_SO_STATISTICS

Indicates the heap is to contain stream output data. Refer to <a href="https://msdn.microsoft.com/7A71F6DA-AAC2-4070-90E9-F91F090AD1A1">D3D12_QUERY_DATA_SO_STATISTICS</a>.


### -field D3D12_QUERY_HEAP_TYPE_VIDEO_DECODE_STATISTICS

Indicates the heap is to contain video decode statistics data. Refer to <a href="direct3d12.d3d12_query_data_video_decode_statistics">D3D12_QUERY_DATA_VIDEO_DECODE_STATISTICS</a>


Video decode statistics can only be queried from video decode command lists (<a href="https://msdn.microsoft.com/28BC70FF-6818-4B8D-9DE4-8316AB2FB288">D3D12_COMMAND_LIST_TYPE_VIDEO_DECODE</a>). See <a href="https://msdn.microsoft.com/F6FA9ACE-0089-4C7B-99D7-FD286CF4B18D">D3D12_QUERY_TYPE_DECODE_STATISTICS</a> for more details.


### -field D3D12_QUERY_HEAP_TYPE_COPY_QUEUE_TIMESTAMP

Indicates the heap is to contain timestamp queries emitted exclusively by copy command lists. Copy queue timestamps can only be queried from a copy command list, and a copy command list can not emit to a regular timestamp query Heap.

Support for this query heap type is not universal. You must use <a href="https://msdn.microsoft.com/2E986E37-30C7-45FE-BC8B-A6DD5670938F">CheckFeatureSupport</a> with <a href="direct3d12.d3d12_feature_d3d12_options3">D3D12_FEATURE_D3D12_OPTIONS3</a> to determine whether the adapter supports copy queue timestamp queries.


## -remarks



This enum is used by the <a href="https://msdn.microsoft.com/1B1CB0D8-B370-4D38-BDA9-21C58D6A8F15">D3D12_QUERY_HEAP_DESC</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

