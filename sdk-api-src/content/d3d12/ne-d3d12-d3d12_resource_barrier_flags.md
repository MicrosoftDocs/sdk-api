---
UID: NE:d3d12.D3D12_RESOURCE_BARRIER_FLAGS
title: D3D12_RESOURCE_BARRIER_FLAGS (d3d12.h)
description: Flags for setting split resource barriers.
helpviewer_keywords: ["D3D12_RESOURCE_BARRIER_FLAGS","D3D12_RESOURCE_BARRIER_FLAGS enumeration","D3D12_RESOURCE_BARRIER_FLAG_BEGIN_ONLY","D3D12_RESOURCE_BARRIER_FLAG_END_ONLY","D3D12_RESOURCE_BARRIER_FLAG_NONE","d3d12/D3D12_RESOURCE_BARRIER_FLAGS","d3d12/D3D12_RESOURCE_BARRIER_FLAG_BEGIN_ONLY","d3d12/D3D12_RESOURCE_BARRIER_FLAG_END_ONLY","d3d12/D3D12_RESOURCE_BARRIER_FLAG_NONE","direct3d12.d3d12_resource_barrier_flags"]
old-location: direct3d12\d3d12_resource_barrier_flags.htm
tech.root: direct3d12
ms.assetid: 352DF566-2E30-49C6-9D1B-35F0AEEA3338
ms.date: 12/05/2018
ms.keywords: D3D12_RESOURCE_BARRIER_FLAGS, D3D12_RESOURCE_BARRIER_FLAGS enumeration, D3D12_RESOURCE_BARRIER_FLAG_BEGIN_ONLY, D3D12_RESOURCE_BARRIER_FLAG_END_ONLY, D3D12_RESOURCE_BARRIER_FLAG_NONE, d3d12/D3D12_RESOURCE_BARRIER_FLAGS, d3d12/D3D12_RESOURCE_BARRIER_FLAG_BEGIN_ONLY, d3d12/D3D12_RESOURCE_BARRIER_FLAG_END_ONLY, d3d12/D3D12_RESOURCE_BARRIER_FLAG_NONE, direct3d12.d3d12_resource_barrier_flags
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
req.typenames: D3D12_RESOURCE_BARRIER_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_RESOURCE_BARRIER_FLAGS
 - d3d12/D3D12_RESOURCE_BARRIER_FLAGS
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
 - D3D12_RESOURCE_BARRIER_FLAGS
---

# D3D12_RESOURCE_BARRIER_FLAGS enumeration


## -description

Flags for setting split resource barriers.

## -enum-fields

### -field D3D12_RESOURCE_BARRIER_FLAG_NONE:0

No flags.

### -field D3D12_RESOURCE_BARRIER_FLAG_BEGIN_ONLY:0x1

This starts a barrier transition in a new state, putting a resource in a temporary no-access condition.

### -field D3D12_RESOURCE_BARRIER_FLAG_END_ONLY:0x2

This barrier completes a transition, setting a new state and restoring active access to a resource.

## -remarks

Split barriers allow a single transition to be split into begin and end halves (refer to <a href="/windows/win32/direct3d12/user-mode-heap-synchronization">Multi-engine synchronization</a>).

This enum is used by the <i>Flags</i> member of the
          <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_barrier">D3D12_RESOURCE_BARRIER</a> structure.

## -see-also

<a href="/windows/win32/direct3d12/direct3d-12-enumerations">Core Enumerations</a>



<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier">ResourceBarrier</a>



<a href="/windows/win32/direct3d12/using-resource-barriers-to-synchronize-resource-states-in-direct3d-12">Using Resource Barriers to Synchronize Resource States in Direct3D 12</a>

