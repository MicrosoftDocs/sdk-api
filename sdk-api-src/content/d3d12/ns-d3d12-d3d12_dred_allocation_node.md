---
UID: NS:d3d12.D3D12_DRED_ALLOCATION_NODE
title: D3D12_DRED_ALLOCATION_NODE
description: Describes, as a node in a linked list, data about an allocation tracked by Device Removed Extended Data (DRED).
helpviewer_keywords: ["D3D12_DRED_ALLOCATION_NODE","D3D12_DRED_ALLOCATION_NODE structure","d3d12/D3D12_DRED_ALLOCATION_NODE","direct3d12.d3d12_dred_allocation_node"]
tech.root: direct3d12
ms.date: 02/06/2019
ms.keywords: D3D12_DRED_ALLOCATION_NODE, D3D12_DRED_ALLOCATION_NODE structure, d3d12/D3D12_DRED_ALLOCATION_NODE, direct3d12.d3d12_dred_allocation_node
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
req.typenames: D3D12_DRED_ALLOCATION_NODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_DRED_ALLOCATION_NODE
 - d3d12/D3D12_DRED_ALLOCATION_NODE
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
 - D3D12_DRED_ALLOCATION_NODE
---

# D3D12_DRED_ALLOCATION_NODE structure


## -description

Describes, as a node in a linked list, data about an allocation tracked by Device Removed Extended Data (DRED). This data includes the GPU VA allocation ranges, and an associated runtime object debug name and type. Each **D3D12_DRED_ALLOCATION_NODE** object is singly linked to the next via its `pNext` member; except for the last node in the list, which has its `pNext` set to `nullptr`. A linked list structure is necessary because a runtime object can share allocation ranges with other objects.

If device removal is caused by a GPU page fault&mdash;and DRED page fault reporting is enabled&mdash;then DRED builds a list of D3D12_DRED_ALLOCATION_NODE structs that includes all matching allocation nodes for active and recently-freed runtime objects.

## -struct-fields

### -field ObjectNameA

A pointer to the ANSI debug name of the allocated runtime object.

### -field ObjectNameW

A pointer to the wide debug name of the allocated runtime object.

### -field AllocationType

A [D3D12_DRED_ALLOCATION_TYPE](ne-d3d12-d3d12_dred_allocation_type.md) value representing the runtime object's allocation type.

### -field pNext

A pointer to a constant **D3D12_DRED_ALLOCATION_NODE** representing the next allocation node in the list, or `nullptr` if this is the last node.

## -see-also

* [Core structures](/windows/desktop/direct3d12/direct3d-12-structures)
* [Use DRED to diagnose GPU faults](/windows/desktop/direct3d12/use-dred)

