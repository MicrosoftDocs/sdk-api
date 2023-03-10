---
UID: NS:d3d12.D3D12_BUFFER_BARRIER
title: D3D12_BUFFER_BARRIER
description: Describes a buffer memory access barrier. Used by buffer barriers to indicate when resource memory must be made visible for a specific access type.
tech.root: direct3d12
ms.date: 11/01/2022
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: d3d12.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: D3D12_BUFFER_BARRIER
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - D3D12_BUFFER_BARRIER
 - d3d12/D3D12_BUFFER_BARRIER
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_BUFFER_BARRIER
prerelease: false
---

## -description

Describes a buffer memory access barrier. Used by buffer barriers to indicate when resource memory must be made visible for a specific access type.

## -struct-fields

### -field SyncBefore

Synchronization scope of all preceding GPU work that must be completed before executing the barrier.

### -field SyncAfter

Synchronization scope of all subsequent GPU work that must wait until the barrier execution is finished.

### -field AccessBefore

Access bits corresponding with resource usage since the preceding barrier, or the start of **ExecuteCommandLists** scope.

### -field AccessAfter

Access bits corresponding with resource usage after the barrier completes.

### -field pResource

Pointer to the buffer resource being using the barrier.

### -field Offset

Must be 0.

### -field Size

Must be either **UINT64_MAX** or the size of the buffer in bytes.

## -remarks

## -see-also
