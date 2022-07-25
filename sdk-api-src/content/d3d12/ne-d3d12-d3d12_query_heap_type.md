---
UID: NE:d3d12.D3D12_QUERY_HEAP_TYPE
title: D3D12_QUERY_HEAP_TYPE (d3d12.h)
description: Specifies the type of query heap to create.
helpviewer_keywords: ["D3D12_QUERY_HEAP_TYPE","D3D12_QUERY_HEAP_TYPE enumeration","D3D12_QUERY_HEAP_TYPE_COPY_QUEUE_TIMESTAMP","D3D12_QUERY_HEAP_TYPE_OCCLUSION","D3D12_QUERY_HEAP_TYPE_PIPELINE_STATISTICS","D3D12_QUERY_HEAP_TYPE_SO_STATISTICS","D3D12_QUERY_HEAP_TYPE_TIMESTAMP","D3D12_QUERY_HEAP_TYPE_VIDEO_DECODE_STATISTICS","d3d12/D3D12_QUERY_HEAP_TYPE","d3d12/D3D12_QUERY_HEAP_TYPE_COPY_QUEUE_TIMESTAMP","d3d12/D3D12_QUERY_HEAP_TYPE_OCCLUSION","d3d12/D3D12_QUERY_HEAP_TYPE_PIPELINE_STATISTICS","d3d12/D3D12_QUERY_HEAP_TYPE_SO_STATISTICS","d3d12/D3D12_QUERY_HEAP_TYPE_TIMESTAMP","d3d12/D3D12_QUERY_HEAP_TYPE_VIDEO_DECODE_STATISTICS","direct3d12.d3d12_query_heap_type"]
old-location: direct3d12\d3d12_query_heap_type.htm
tech.root: direct3d12
ms.assetid: FDD5F81B-F356-49D9-B6FE-FE2847934E61
ms.date: 12/05/2018
ms.keywords: D3D12_QUERY_HEAP_TYPE, D3D12_QUERY_HEAP_TYPE enumeration, D3D12_QUERY_HEAP_TYPE_COPY_QUEUE_TIMESTAMP, D3D12_QUERY_HEAP_TYPE_OCCLUSION, D3D12_QUERY_HEAP_TYPE_PIPELINE_STATISTICS, D3D12_QUERY_HEAP_TYPE_SO_STATISTICS, D3D12_QUERY_HEAP_TYPE_TIMESTAMP, D3D12_QUERY_HEAP_TYPE_VIDEO_DECODE_STATISTICS, d3d12/D3D12_QUERY_HEAP_TYPE, d3d12/D3D12_QUERY_HEAP_TYPE_COPY_QUEUE_TIMESTAMP, d3d12/D3D12_QUERY_HEAP_TYPE_OCCLUSION, d3d12/D3D12_QUERY_HEAP_TYPE_PIPELINE_STATISTICS, d3d12/D3D12_QUERY_HEAP_TYPE_SO_STATISTICS, d3d12/D3D12_QUERY_HEAP_TYPE_TIMESTAMP, d3d12/D3D12_QUERY_HEAP_TYPE_VIDEO_DECODE_STATISTICS, direct3d12.d3d12_query_heap_type
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
targetos: Windows
req.typenames: D3D12_QUERY_HEAP_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_QUERY_HEAP_TYPE
 - d3d12/D3D12_QUERY_HEAP_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_QUERY_HEAP_TYPE
---

# D3D12_QUERY_HEAP_TYPE enumeration


## -description

Specifies the type of query heap to create.

## -enum-fields

### -field D3D12_QUERY_HEAP_TYPE_OCCLUSION:0

This returns a binary 0/1 result:  0 indicates that no samples passed depth and stencil testing, 1 indicates that at least one sample passed depth and stencil testing.  This enables occlusion queries to not interfere with any GPU performance optimization associated with depth/stencil testing.

### -field D3D12_QUERY_HEAP_TYPE_TIMESTAMP:1

Indicates that the heap is for high-performance timing data.

### -field D3D12_QUERY_HEAP_TYPE_PIPELINE_STATISTICS:2

Indicates the heap is to contain pipeline data. Refer to <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_query_data_pipeline_statistics">D3D12_QUERY_DATA_PIPELINE_STATISTICS</a>.

### -field D3D12_QUERY_HEAP_TYPE_SO_STATISTICS:3

Indicates the heap is to contain stream output data. Refer to <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_query_data_so_statistics">D3D12_QUERY_DATA_SO_STATISTICS</a>.

### -field D3D12_QUERY_HEAP_TYPE_VIDEO_DECODE_STATISTICS:4

Indicates the heap is to contain video decode statistics data. Refer to [D3D12_QUERY_DATA_VIDEO_DECODE_STATISTICS](../d3d12video/ns-d3d12video-d3d12_query_data_video_decode_statistics.md).

Video decode statistics can only be queried from video decode command lists (<a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type">D3D12_COMMAND_LIST_TYPE_VIDEO_DECODE</a>). See <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type">D3D12_QUERY_TYPE_DECODE_STATISTICS</a> for more details.

### -field D3D12_QUERY_HEAP_TYPE_COPY_QUEUE_TIMESTAMP:5

Indicates the heap is to contain timestamp queries emitted exclusively by copy command lists. Copy queue timestamps can only be queried from a copy command list, and a copy command list can not emit to a regular timestamp query Heap.

Support for this query heap type is not universal. You must use <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport">CheckFeatureSupport</a> with [D3D12_FEATURE_D3D12_OPTIONS3](./ne-d3d12-d3d12_feature.md) to determine whether the adapter supports copy queue timestamp queries.

## -remarks

This enum is used by the <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_query_heap_desc">D3D12_QUERY_HEAP_DESC</a> structure.

## -see-also

[Core enumerations](/windows/win32/direct3d12/direct3d-12-enumerations)
