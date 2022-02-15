---
UID: NE:d3d12.D3D12_FENCE_FLAGS
title: D3D12_FENCE_FLAGS (d3d12.h)
description: Specifies fence options.
helpviewer_keywords: ["D3D12_FENCE_FLAGS","D3D12_FENCE_FLAGS enumeration","D3D12_FENCE_FLAG_NONE","D3D12_FENCE_FLAG_NON_MONITORED","D3D12_FENCE_FLAG_SHARED","D3D12_FENCE_FLAG_SHARED_CROSS_ADAPTER","d3d12/D3D12_FENCE_FLAGS","d3d12/D3D12_FENCE_FLAG_NONE","d3d12/D3D12_FENCE_FLAG_NON_MONITORED","d3d12/D3D12_FENCE_FLAG_SHARED","d3d12/D3D12_FENCE_FLAG_SHARED_CROSS_ADAPTER","direct3d12.d3d12_fence_flags"]
old-location: direct3d12\d3d12_fence_flags.htm
tech.root: direct3d12
ms.assetid: EF725566-B77A-40EE-B5E3-86C5D13CC7D5
ms.date: 12/05/2018
ms.keywords: D3D12_FENCE_FLAGS, D3D12_FENCE_FLAGS enumeration, D3D12_FENCE_FLAG_NONE, D3D12_FENCE_FLAG_NON_MONITORED, D3D12_FENCE_FLAG_SHARED, D3D12_FENCE_FLAG_SHARED_CROSS_ADAPTER, d3d12/D3D12_FENCE_FLAGS, d3d12/D3D12_FENCE_FLAG_NONE, d3d12/D3D12_FENCE_FLAG_NON_MONITORED, d3d12/D3D12_FENCE_FLAG_SHARED, d3d12/D3D12_FENCE_FLAG_SHARED_CROSS_ADAPTER, direct3d12.d3d12_fence_flags
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
req.typenames: D3D12_FENCE_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_FENCE_FLAGS
 - d3d12/D3D12_FENCE_FLAGS
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
 - D3D12_FENCE_FLAGS
---

# D3D12_FENCE_FLAGS enumeration


## -description

Specifies fence options.

## -enum-fields

### -field D3D12_FENCE_FLAG_NONE:0

No options are specified.

### -field D3D12_FENCE_FLAG_SHARED:0x1

The fence is shared.

### -field D3D12_FENCE_FLAG_SHARED_CROSS_ADAPTER:0x2

The fence is shared with another GPU adapter.

### -field D3D12_FENCE_FLAG_NON_MONITORED:0x4

The fence is of the non-monitored type. Non-monitored fences should only be used when the adapter doesn't support monitored fences, or when a fence is shared with an adapter that doesn't support monitored fences.

## -remarks

This enum is used by the <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createfence">ID3D12Device::CreateFence</a> method.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
