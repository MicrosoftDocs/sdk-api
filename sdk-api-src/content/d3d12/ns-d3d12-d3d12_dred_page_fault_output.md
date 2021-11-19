---
UID: NS:d3d12.D3D12_DRED_PAGE_FAULT_OUTPUT
title: D3D12_DRED_PAGE_FAULT_OUTPUT
description: Describes allocation data related to a GPU page fault on a given virtual address (VA).
helpviewer_keywords: ["D3D12_DRED_PAGE_FAULT_OUTPUT","D3D12_DRED_PAGE_FAULT_OUTPUT structure","d3d12/D3D12_DRED_PAGE_FAULT_OUTPUT","direct3d12.d3d12_dred_page_fault_output"]
tech.root: direct3d12
ms.date: 02/06/2019
ms.keywords: D3D12_DRED_PAGE_FAULT_OUTPUT, D3D12_DRED_PAGE_FAULT_OUTPUT structure, d3d12/D3D12_DRED_PAGE_FAULT_OUTPUT, direct3d12.d3d12_dred_page_fault_output
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
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
req.typenames: D3D12_DRED_PAGE_FAULT_OUTPUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_DRED_PAGE_FAULT_OUTPUT
 - d3d12/D3D12_DRED_PAGE_FAULT_OUTPUT
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
 - D3D12_DRED_PAGE_FAULT_OUTPUT
---

# D3D12_DRED_PAGE_FAULT_OUTPUT structure


## -description

Describes allocation data related to a GPU page fault on a given virtual address (VA). Contains the VA of a GPU page fault, together with a list of matching allocation nodes for active objects, and a list of allocation nodes for recently deleted objects.

## -struct-fields

### -field PageFaultVA

A [D3D12_GPU_VIRTUAL_ADDRESS](/windows/desktop/direct3d12/d3d12_gpu_virtual_address) containing the GPU virtual address (VA) of the faulting operation if device removal was due to a GPU page fault.

### -field pHeadExistingAllocationNode

A pointer to a constant [D3D12_DRED_ALLOCATION_NODE](ns-d3d12-d3d12_dred_allocation_node.md) object representing the head of a linked list of allocation nodes for active allocated runtime objects with virtual address (VA) ranges that match the faulting VA (`PageFaultVA`). Has a value of `nullptr` if the list is empty.

### -field pHeadRecentFreedAllocationNode

A pointer to a constant [D3D12_DRED_ALLOCATION_NODE](ns-d3d12-d3d12_dred_allocation_node.md) object representing the head of a linked list of allocation nodes for recently freed runtime objects with virtual address (VA) ranges that match the faulting VA (`PageFaultVA`). Has a value of `nullptr` if the list is empty.

## -see-also

* [Core structures](/windows/desktop/direct3d12/direct3d-12-structures)
* [Use DRED to diagnose GPU faults](/windows/desktop/direct3d12/use-dred)

