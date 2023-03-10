---
UID: NS:d3d12.D3D12_DEVICE_REMOVED_EXTENDED_DATA1
title: D3D12_DEVICE_REMOVED_EXTENDED_DATA1
description: Represents Device Removed Extended Data (DRED) version 1.1 data.
helpviewer_keywords: ["D3D12_DEVICE_REMOVED_EXTENDED_DATA1","D3D12_DEVICE_REMOVED_EXTENDED_DATA1 structure","d3d12/D3D12_DEVICE_REMOVED_EXTENDED_DATA1","direct3d12.d3d12_device_removed_extended_data1"]
tech.root: direct3d12
ms.date: 02/06/2019
ms.keywords: D3D12_DEVICE_REMOVED_EXTENDED_DATA1, D3D12_DEVICE_REMOVED_EXTENDED_DATA1 structure, d3d12/D3D12_DEVICE_REMOVED_EXTENDED_DATA1, direct3d12.d3d12_device_removed_extended_data1
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
req.typenames: D3D12_DEVICE_REMOVED_EXTENDED_DATA1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_DEVICE_REMOVED_EXTENDED_DATA1
 - d3d12/D3D12_DEVICE_REMOVED_EXTENDED_DATA1
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
 - D3D12_DEVICE_REMOVED_EXTENDED_DATA1
---

# D3D12_DEVICE_REMOVED_EXTENDED_DATA1 structure


## -description

Represents Device Removed Extended Data (DRED) version 1.1 device removal data, so that debuggers and debugger extensions can access DRED data. Also see [D3D12_VERSIONED_DEVICE_REMOVED_EXTENDED_DATA](ns-d3d12-d3d12_versioned_device_removed_extended_data.md).

This structure is not used by any interface methods, and it provides no runtime API access.

## -struct-fields

### -field DeviceRemovedReason

An [HRESULT](/windows/desktop/com/structure-of-com-error-codes) containing the reason the device was removed (matches the return value of [GetDeviceRemovedReason](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getdeviceremovedreason)). Also see [COM Error Codes (UI, Audio, DirectX, Codec)](/windows/desktop/com/com-error-codes-10).

### -field AutoBreadcrumbsOutput

A [D3D12_DRED_AUTO_BREADCRUMBS_OUTPUT](ns-d3d12-d3d12_auto_breadcrumb_node.md) value that contains the auto-breadcrumb state prior to device removal.

### -field pHeadAutoBreadcrumbNode

An output parameter of type pointer to [D3D12_AUTO_BREADCRUMB_NODE](ns-d3d12-d3d12_auto_breadcrumb_node.md) representing the returned auto-breadcrumb object(s). This is a pointer to the head of a linked list of auto-breadcrumb node objects. All of the nodes in the linked list represent potentially incomplete command list execution on the GPU at the time of the device-removal event.

### -field PageFaultOutput

A [D3D12_DRED_PAGE_FAULT_OUTPUT](ns-d3d12-d3d12_auto_breadcrumb_node.md) value that contains page fault data if device removal was the result of a GPU page fault.

## -see-also

* [Core structures](/windows/desktop/direct3d12/direct3d-12-structures)
* [D3D12_VERSIONED_DEVICE_REMOVED_EXTENDED_DATA](ns-d3d12-d3d12_versioned_device_removed_extended_data.md)
* [Use DRED to diagnose GPU faults](/windows/desktop/direct3d12/use-dred)

