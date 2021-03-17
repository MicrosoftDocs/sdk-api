---
UID: NS:d3d12.D3D12_FEATURE_DATA_EXISTING_HEAPS
title: D3D12_FEATURE_DATA_EXISTING_HEAPS (d3d12.h)
description: Provides detail about whether the adapter supports creating heaps from existing system memory.
helpviewer_keywords: ["D3D12_FEATURE_DATA_EXISTING_HEAPS","D3D12_FEATURE_DATA_EXISTING_HEAPS structure","d3d12/D3D12_FEATURE_DATA_EXISTING_HEAPS","direct3d12.d3d12_feature_data_existing_heaps"]
old-location: direct3d12\d3d12_feature_data_existing_heaps.htm
tech.root: direct3d12
ms.assetid: 7F0D0FAD-BF29-43AD-95FA-85B9719C4782
ms.date: 12/05/2018
ms.keywords: D3D12_FEATURE_DATA_EXISTING_HEAPS, D3D12_FEATURE_DATA_EXISTING_HEAPS structure, d3d12/D3D12_FEATURE_DATA_EXISTING_HEAPS, direct3d12.d3d12_feature_data_existing_heaps
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
req.typenames: D3D12_FEATURE_DATA_EXISTING_HEAPS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_FEATURE_DATA_EXISTING_HEAPS
 - d3d12/D3D12_FEATURE_DATA_EXISTING_HEAPS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_FEATURE_DATA_EXISTING_HEAPS
---

# D3D12_FEATURE_DATA_EXISTING_HEAPS structure


## -description

Provides detail about whether the adapter supports creating heaps from existing system memory. Such heaps are not intended for general use, but are exceptionally useful for diagnostic purposes, because they are guaranteed to persist even after the adapter faults or experiences a device-removal event. Persistence is not guaranteed for heaps returned by <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap">ID3D12Device::CreateHeap</a> or <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource">ID3D12Device::CreateCommittedResource</a>, even when the heap resides in system memory.

## -struct-fields

### -field Supported

<b>TRUE</b> if the adapter can create a heap from existing system memory. Otherwise, <b>FALSE</b>.

## -remarks

For a variety of performance and compatibility reasons, applications should not make use of this feature except for diagnostic purposes. In particular, heaps created using this feature only support system-memory heaps with cross-adapter properties, which precludes many optimization opportunities that typical application scenarios could otherwise take advantage of.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>



<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature">D3D12_FEATURE</a>



<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource">ID3D12Device::CreateCommittedResource</a>



<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap">ID3D12Device::CreateHeap</a>