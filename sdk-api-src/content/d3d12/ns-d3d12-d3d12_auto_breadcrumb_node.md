---
UID: NS:d3d12.D3D12_AUTO_BREADCRUMB_NODE
title: D3D12_AUTO_BREADCRUMB_NODE
description: Represents Device Removed Extended Data (DRED) auto-breadcrumb data as a node in a linked list.
helpviewer_keywords: ["D3D12_AUTO_BREADCRUMB_NODE","D3D12_AUTO_BREADCRUMB_NODE structure","d3d12/D3D12_AUTO_BREADCRUMB_NODE","direct3d12.d3d12_auto_breadcrumb_node"]
tech.root: direct3d12
ms.date: 10/23/2023
ms.keywords: D3D12_AUTO_BREADCRUMB_NODE, D3D12_AUTO_BREADCRUMB_NODE structure, d3d12/D3D12_AUTO_BREADCRUMB_NODE, direct3d12.d3d12_auto_breadcrumb_node
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
req.typenames: D3D12_AUTO_BREADCRUMB_NODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_AUTO_BREADCRUMB_NODE
 - d3d12/D3D12_AUTO_BREADCRUMB_NODE
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
 - D3D12_AUTO_BREADCRUMB_NODE
---

## -description

Represents Device Removed Extended Data (DRED) auto-breadcrumb data as a node in a linked list. Each **D3D12_AUTO_BREADCRUMB_NODE** object is singly linked to the next via its `pNext` member; except for the last node in the list, which has its `pNext` set to `nullptr`.

The Direct3D 12 runtime creates one of these for each graphics command list, and tracks them in the command allocator associated with the list. When a command list is executed, the command queue information is set. After device removal is detected, the Direct3D 12 runtime links together the auto-breadcrumb nodes for any GPU work that is still outstanding.

## -struct-fields

### -field pCommandListDebugNameA

A pointer to the ANSI debug name of the outstanding command list (if any).

### -field pCommandListDebugNameW

A pointer to the wide debug name of the outstanding command list (if any).

### -field pCommandQueueDebugNameA

A pointer to the ANSI debug name of the outstanding command queue (if any).

### -field pCommandQueueDebugNameW

A pointer to the wide debug name of the outstanding command queue (if any).

### -field pCommandList

A pointer to the [ID3D12GraphicsCommandList interface](nn-d3d12-id3d12graphicscommandlist.md) representing the outstanding command list at the time of execution.

### -field pCommandQueue

A pointer to the [ID3D12CommandQueue interface](nn-d3d12-id3d12commandqueue.md) representing the outstanding command queue.

### -field BreadcrumbCount

A **UINT32** containing the count of [D3D12_AUTO_BREADCRUMB_OP](ne-d3d12-d3d12_auto_breadcrumb_op.md) values in the array pointed to by `pCommandHistory`.

### -field pLastBreadcrumbValue

A pointer to a constant **UINT32** containing the number of *pCommandHistory* breadcrumbs ops completed. As such, the last successfully completed breadcrumb op is at index `(*pLastBreadcrumbValue - 1)` in *pCommandHistory*.

### -field pCommandHistory

A pointer to a constant array of [D3D12_AUTO_BREADCRUMB_OP](ne-d3d12-d3d12_auto_breadcrumb_op.md) values representing all of the render/compute operations recorded into the associated command list.

### -field pNext

A pointer to a constant **D3D12_AUTO_BREADCRUMB_NODE** representing the next auto-breadcrumb node in the list, or `nullptr` if this is the last node.

## -see-also

* [Core structures](/windows/desktop/direct3d12/direct3d-12-structures)
* [Use DRED to diagnose GPU faults](/windows/desktop/direct3d12/use-dred)

