---
UID: NF:d3d12video.ID3D12VideoProcessCommandList.BeginQuery
title: ID3D12VideoProcessCommandList::BeginQuery
description: Starts a query running. (ID3D12VideoProcessCommandList::BeginQuery)
helpviewer_keywords: ["ID3D12VideoProcessCommandList::BeginQuery","BeginQuery","ID3D12VideoProcessCommandList.BeginQuery","ID3D12VideoProcessCommandList::BeginQuery","ID3D12VideoProcessCommandList.BeginQuery"]
tech.root: mf
ms.assetid: 0cf0c814-02d2-4901-a65d-ef7836dd198a
ms.date: 05/28/2019
ms.keywords: ID3D12VideoProcessCommandList::BeginQuery, BeginQuery, ID3D12VideoProcessCommandList.BeginQuery, ID3D12VideoProcessCommandList::BeginQuery, ID3D12VideoProcessCommandList.BeginQuery
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
 - ID3D12VideoProcessCommandList::BeginQuery
 - d3d12video/ID3D12VideoProcessCommandList::BeginQuery
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12VideoProcessCommandList::BeginQuery
---

# ID3D12VideoProcessCommandList::BeginQuery


## -description

Starts a query running.

## -parameters

### -param pQueryHeap

A pointer to an [ID3D12QueryHeap](/windows/desktop/api/d3d12/nn-d3d12-id3d12queryheap) specifying the storage for this query.

### -param Type

A member of the [D3D12_QUERY_TYPE](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type) enumeration specifying the type of the query.

### -param Index

The index of the query within the query heap.

## -remarks

Some queries do not use **BeginQuery** and only have an **EndQuery**.  See each query type in [D3D12_QUERY_TYPE](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type) to determine proper usage.

## -see-also
