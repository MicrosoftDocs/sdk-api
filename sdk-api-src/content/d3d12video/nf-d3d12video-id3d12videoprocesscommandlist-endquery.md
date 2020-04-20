---
UID: NF:d3d12video.ID3D12VideoProcessCommandList.EndQuery
title: ID3D12VideoProcessCommandList::EndQuery
description: Ends a query.helpviewer_keywords: ["ID3D12VideoProcessCommandList::EndQuery","EndQuery","ID3D12VideoProcessCommandList.EndQuery","ID3D12VideoProcessCommandList::EndQuery","ID3D12VideoProcessCommandList.EndQuery"]
tech.root: mf
ms.assetid: e90086c6-2044-444c-a655-d1f3aea002b4
ms.date: 05/28/2019
f1_keywords:
- ID3D12VideoProcessCommandList::EndQuery
dev_langs:
- c++
ms.keywords: ID3D12VideoProcessCommandList::EndQuery, EndQuery, ID3D12VideoProcessCommandList.EndQuery, ID3D12VideoProcessCommandList::EndQuery, ID3D12VideoProcessCommandList.EndQuery
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
topic_type:
- apiref
api_type:
- COM
api_location:
- d3d12.dll
api_name:
- ID3D12VideoProcessCommandList::EndQuery
targetos: Windows
---

# ID3D12VideoProcessCommandList::EndQuery


## -description

Ends a query.

## -parameters

### -param pQueryHeap

A pointer to an [ID3D12QueryHeap](https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12queryheap) specifying the storage for this query.

### -param Type

A member of the [D3D12_QUERY_TYPE](https://docs.microsoft.com/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type) enumeration specifying the type of the query.

### -param Index

The index of the query within the query heap.

## -remarks

## -see-also
