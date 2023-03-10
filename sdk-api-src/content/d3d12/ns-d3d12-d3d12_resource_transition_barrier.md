---
UID: NS:d3d12.D3D12_RESOURCE_TRANSITION_BARRIER
title: D3D12_RESOURCE_TRANSITION_BARRIER (d3d12.h)
description: Describes the transition of subresources between different usages.
helpviewer_keywords: ["D3D12_RESOURCE_TRANSITION_BARRIER","D3D12_RESOURCE_TRANSITION_BARRIER structure","d3d12/D3D12_RESOURCE_TRANSITION_BARRIER","direct3d12.d3d12_resource_transition_barrier"]
old-location: direct3d12\d3d12_resource_transition_barrier.htm
tech.root: direct3d12
ms.assetid: 52C21198-827A-4E75-ADB8-DCA0204A4469
ms.date: 12/05/2018
ms.keywords: D3D12_RESOURCE_TRANSITION_BARRIER, D3D12_RESOURCE_TRANSITION_BARRIER structure, d3d12/D3D12_RESOURCE_TRANSITION_BARRIER, direct3d12.d3d12_resource_transition_barrier
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
req.typenames: D3D12_RESOURCE_TRANSITION_BARRIER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_RESOURCE_TRANSITION_BARRIER
 - d3d12/D3D12_RESOURCE_TRANSITION_BARRIER
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
 - D3D12_RESOURCE_TRANSITION_BARRIER
---

# D3D12_RESOURCE_TRANSITION_BARRIER structure


## -description

Describes the transition of subresources between different usages.

## -struct-fields

### -field pResource

A pointer to the <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a> object that represents the resource used in the transition.

### -field Subresource

The index of the subresource for the transition.
            Use the <b>D3D12_RESOURCE_BARRIER_ALL_SUBRESOURCES</b> flag ( 0xffffffff ) to transition all subresources in a resource at the same time.

### -field StateBefore

The "before" usages of the subresources, as a bitwise-OR'd combination of <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states">D3D12_RESOURCE_STATES</a> enumeration constants.

### -field StateAfter

The "after" usages of the subresources, as a bitwise-OR'd combination of <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states">D3D12_RESOURCE_STATES</a> enumeration constants.

## -remarks

This struct is used by the <b>Transition</b> member of the
        <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier">D3D12_RESOURCE_BARRIER</a> struct.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>



<a href="/windows/desktop/direct3d12/using-resource-barriers-to-synchronize-resource-states-in-direct3d-12">Using Resource Barriers to Synchronize Resource States in Direct3D 12</a>