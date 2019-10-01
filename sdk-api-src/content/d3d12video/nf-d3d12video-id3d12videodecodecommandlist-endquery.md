---
UID: NF:d3d12video.ID3D12VideoDecodeCommandList.EndQuery
title: ID3D12VideoDecodeCommandList::EndQuery
author: windows-sdk-content
description: Ends a query.
tech.root: mf
ms.assetid: 6919b1be-e7eb-4b9a-ab51-d5c912803c3f
ms.author: windowssdkdev
ms.date: 05/28/2019
ms.topic: method
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
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12VideoDecodeCommandList::EndQuery
targetos: Windows

---

# ID3D12VideoDecodeCommandList::EndQuery


## -description

Ends a query.

## -parameters

### -param pQueryHeap

A pointer to an [ID3D12QueryHeap](https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12queryheap) specifying the storage for this query.

### -param Type

A member of the [D3D12_QUERY_TYPE](https://docs.microsoft.com/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type) enumeration specifying the type of the query.

### -param Index

The index of the query within the query heap.

## -returns
This method returns void.

## -remarks

## -see-also