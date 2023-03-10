---
UID: NF:d3d12video.ID3D12VideoDecodeCommandList.EndQuery
title: ID3D12VideoDecodeCommandList::EndQuery
description: Ends a query. (ID3D12VideoDecodeCommandList::EndQuery)
helpviewer_keywords: ["ID3D12VideoDecodeCommandList::EndQuery","EndQuery","ID3D12VideoDecodeCommandList.EndQuery","ID3D12VideoDecodeCommandList::EndQuery","ID3D12VideoDecodeCommandList.EndQuery"]
tech.root: mf
ms.assetid: 6919b1be-e7eb-4b9a-ab51-d5c912803c3f
ms.date: 05/28/2019
ms.keywords: ID3D12VideoDecodeCommandList::EndQuery, EndQuery, ID3D12VideoDecodeCommandList.EndQuery, ID3D12VideoDecodeCommandList::EndQuery, ID3D12VideoDecodeCommandList.EndQuery
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
 - ID3D12VideoDecodeCommandList::EndQuery
 - d3d12video/ID3D12VideoDecodeCommandList::EndQuery
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12VideoDecodeCommandList::EndQuery
---

# ID3D12VideoDecodeCommandList::EndQuery


## -description

Ends a query.

## -parameters

### -param pQueryHeap

A pointer to an [ID3D12QueryHeap](/windows/desktop/api/d3d12/nn-d3d12-id3d12queryheap) specifying the storage for this query.

### -param Type

A member of the [D3D12_QUERY_TYPE](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type) enumeration specifying the type of the query.

### -param Index

The index of the query within the query heap.

## -remarks

## -see-also
