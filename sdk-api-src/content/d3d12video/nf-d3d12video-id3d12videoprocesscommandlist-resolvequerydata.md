---
UID: NF:d3d12video.ID3D12VideoProcessCommandList.ResolveQueryData
title: ID3D12VideoProcessCommandList::ResolveQueryData
description: Extracts data from a query.
helpviewer_keywords: ["ID3D12VideoProcessCommandList::ResolveQueryData","ResolveQueryData","ID3D12VideoProcessCommandList.ResolveQueryData","ID3D12VideoProcessCommandList::ResolveQueryData","ID3D12VideoProcessCommandList.ResolveQueryData"]
tech.root: mf
ms.assetid: a30beb4e-98e3-4644-843d-c206eb4ef138
ms.date: 05/28/2019
ms.keywords: ID3D12VideoProcessCommandList::ResolveQueryData, ResolveQueryData, ID3D12VideoProcessCommandList.ResolveQueryData, ID3D12VideoProcessCommandList::ResolveQueryData, ID3D12VideoProcessCommandList.ResolveQueryData
req.header: d3d12video.h
req.include-header: 
req.redist: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: d3d12.dll
req.irql: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
targetos: Windows
f1_keywords:
 - ID3D12VideoProcessCommandList::ResolveQueryData
 - d3d12video/ID3D12VideoProcessCommandList::ResolveQueryData
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12VideoProcessCommandList::ResolveQueryData
---

# ID3D12VideoProcessCommandList::ResolveQueryData


## -description

Extracts data from a query.

## -parameters

### -param pQueryHeap

A pointer to an [ID3D12QueryHeap](/windows/desktop/api/d3d12/nn-d3d12-id3d12queryheap) specifying the storage containing the queries to resolve.

### -param Type

A member of the [D3D12_QUERY_TYPE](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type) enumeration specifying the type of the query.

### -param StartIndex

The index of the first query to resolve.

### -param NumQueries

The number of queries to resolve.

### -param pDestinationBuffer

A pointer to an [ID3D12Resource](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) representing the destination buffer. The resource must be in the state [D3D12_RESOURCE_STATE_COPY_DEST](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states).

### -param AlignedDestinationBufferOffset

The alignment offset into the destination buffer. This must be a multiple of 8 bytes.

## -remarks

## -see-also