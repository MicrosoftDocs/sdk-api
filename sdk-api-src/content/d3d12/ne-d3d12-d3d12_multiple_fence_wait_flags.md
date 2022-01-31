---
UID: NE:d3d12.D3D12_MULTIPLE_FENCE_WAIT_FLAGS
title: D3D12_MULTIPLE_FENCE_WAIT_FLAGS (d3d12.h)
description: Specifies multiple wait flags for multiple fences.
helpviewer_keywords: ["D3D12_MULTIPLE_FENCE_WAIT_FLAGS","D3D12_MULTIPLE_FENCE_WAIT_FLAGS enumeration","D3D12_MULTIPLE_FENCE_WAIT_FLAG_ALL","D3D12_MULTIPLE_FENCE_WAIT_FLAG_ANY","D3D12_MULTIPLE_FENCE_WAIT_FLAG_NONE","d3d12/D3D12_MULTIPLE_FENCE_WAIT_FLAGS","d3d12/D3D12_MULTIPLE_FENCE_WAIT_FLAG_ALL","d3d12/D3D12_MULTIPLE_FENCE_WAIT_FLAG_ANY","d3d12/D3D12_MULTIPLE_FENCE_WAIT_FLAG_NONE","direct3d12.d3d12_multiple_fence_wait_flags"]
old-location: direct3d12\d3d12_multiple_fence_wait_flags.htm
tech.root: direct3d12
ms.assetid: A5C52F58-C082-41C2-99E4-800DFBA250D2
ms.date: 12/05/2018
ms.keywords: D3D12_MULTIPLE_FENCE_WAIT_FLAGS, D3D12_MULTIPLE_FENCE_WAIT_FLAGS enumeration, D3D12_MULTIPLE_FENCE_WAIT_FLAG_ALL, D3D12_MULTIPLE_FENCE_WAIT_FLAG_ANY, D3D12_MULTIPLE_FENCE_WAIT_FLAG_NONE, d3d12/D3D12_MULTIPLE_FENCE_WAIT_FLAGS, d3d12/D3D12_MULTIPLE_FENCE_WAIT_FLAG_ALL, d3d12/D3D12_MULTIPLE_FENCE_WAIT_FLAG_ANY, d3d12/D3D12_MULTIPLE_FENCE_WAIT_FLAG_NONE, direct3d12.d3d12_multiple_fence_wait_flags
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
req.typenames: D3D12_MULTIPLE_FENCE_WAIT_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_MULTIPLE_FENCE_WAIT_FLAGS
 - d3d12/D3D12_MULTIPLE_FENCE_WAIT_FLAGS
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
 - D3D12_MULTIPLE_FENCE_WAIT_FLAGS
---

# D3D12_MULTIPLE_FENCE_WAIT_FLAGS enumeration


## -description

Specifies multiple wait flags for multiple fences.

## -enum-fields

### -field D3D12_MULTIPLE_FENCE_WAIT_FLAG_NONE:0

No flags are being passed. This means to use the default behavior, which is to wait for all fences before signaling the event.

### -field D3D12_MULTIPLE_FENCE_WAIT_FLAG_ANY:0x1

Modifies behavior to indicate that the event should be signaled after any one of the fence values has been reached by its corresponding fence.

### -field D3D12_MULTIPLE_FENCE_WAIT_FLAG_ALL:0

An alias for **D3D12_MULTIPLE_FENCE_WAIT_FLAG_NONE**, meaning to use the default behavior and wait for all fences.

## -remarks

This enum is used by the <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device1-seteventonmultiplefencecompletion">SetEventOnMultipleFenceCompletion</a> method.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>



<a href="/windows/desktop/direct3d12/root-signature-version-1-1">Root Signature Version 1.1</a>
