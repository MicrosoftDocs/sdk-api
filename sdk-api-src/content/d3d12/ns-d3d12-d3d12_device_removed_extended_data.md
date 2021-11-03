---
UID: NS:d3d12.D3D12_DEVICE_REMOVED_EXTENDED_DATA
title: D3D12_DEVICE_REMOVED_EXTENDED_DATA
description: Represents Device Removed Extended Data (DRED) version 1.0 data.
helpviewer_keywords: ["D3D12_DEVICE_REMOVED_EXTENDED_DATA","D3D12_DEVICE_REMOVED_EXTENDED_DATA structure","d3d12/D3D12_DEVICE_REMOVED_EXTENDED_DATA","direct3d12.d3d12_device_removed_extended_data"]
tech.root: direct3d12
ms.date: 02/06/2019
ms.keywords: D3D12_DEVICE_REMOVED_EXTENDED_DATA, D3D12_DEVICE_REMOVED_EXTENDED_DATA structure, d3d12/D3D12_DEVICE_REMOVED_EXTENDED_DATA, direct3d12.d3d12_device_removed_extended_data
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
req.typenames: D3D12_DEVICE_REMOVED_EXTENDED_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_DEVICE_REMOVED_EXTENDED_DATA
 - d3d12/D3D12_DEVICE_REMOVED_EXTENDED_DATA
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
 - D3D12_DEVICE_REMOVED_EXTENDED_DATA
---

# D3D12_DEVICE_REMOVED_EXTENDED_DATA structure


## -description

> [!NOTE]
> As of Windows 10, version 1903, **D3D12_DEVICE_REMOVED_EXTENDED_DATA** is deprecated, and it may not be available in future versions of Windows. Use [**D3D12_DEVICE_REMOVED_EXTENDED_DATA1**](ns-d3d12-d3d12_device_removed_extended_data1.md), instead.

Represents Device Removed Extended Data (DRED) version 1.0 data.

## -struct-fields

### -field Flags

An input parameter of type [D3D12_DRED_FLAGS](ne-d3d12-d3d12_dred_flags.md), specifying control flags for the Direct3D runtime.

### -field pHeadAutoBreadcrumbNode

An output parameter of type pointer to [D3D12_AUTO_BREADCRUMB_NODE](ns-d3d12-d3d12_auto_breadcrumb_node.md) representing the returned auto-breadcrumb object(s). This is a pointer to the head of a linked list of auto-breadcrumb objects. All of the nodes in the linked list represent potentially incomplete command list execution on the GPU at the time of the device-removal event.

## -see-also

* [Core structures](/windows/desktop/direct3d12/direct3d-12-structures)
* [Use DRED to diagnose GPU faults](/windows/desktop/direct3d12/use-dred)

