---
UID: NF:d3d12video.ID3D12VideoEncodeCommandList.EndQuery
title: ID3D12VideoEncodeCommandList::EndQuery
ms.date: 11/4/2019
targetos: Windows
description: Ends a query. (ID3D12VideoEncodeCommandList::EndQuery)
tech.root: mf
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: d3d12.dll
req.header: d3d12video.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12VideoEncodeCommandList::EndQuery
f1_keywords:
 - ID3D12VideoEncodeCommandList::EndQuery
 - d3d12video/ID3D12VideoEncodeCommandList::EndQuery
dev_langs:
 - c++
---

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
