---
UID: NS:d3d12.D3D12_VERSIONED_DEVICE_REMOVED_EXTENDED_DATA
title: D3D12_VERSIONED_DEVICE_REMOVED_EXTENDED_DATA
description: Represents versioned Device Removed Extended Data (DRED) data.
helpviewer_keywords: ["D3D12_VERSIONED_DEVICE_REMOVED_EXTENDED_DATA","D3D12_VERSIONED_DEVICE_REMOVED_EXTENDED_DATA structure","d3d12/D3D12_VERSIONED_DEVICE_REMOVED_EXTENDED_DATA","direct3d12.d3d12_versioned_device_removed_extended_data"]
tech.root: direct3d12
ms.date: 02/06/2019
ms.keywords: D3D12_VERSIONED_DEVICE_REMOVED_EXTENDED_DATA, D3D12_VERSIONED_DEVICE_REMOVED_EXTENDED_DATA structure, d3d12/D3D12_VERSIONED_DEVICE_REMOVED_EXTENDED_DATA, direct3d12.d3d12_versioned_device_removed_extended_data
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
req.typenames: D3D12_VERSIONED_DEVICE_REMOVED_EXTENDED_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_VERSIONED_DEVICE_REMOVED_EXTENDED_DATA
 - d3d12/D3D12_VERSIONED_DEVICE_REMOVED_EXTENDED_DATA
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
 - D3D12_VERSIONED_DEVICE_REMOVED_EXTENDED_DATA
---

# D3D12_VERSIONED_DEVICE_REMOVED_EXTENDED_DATA structure


## -description

Represents versioned Device Removed Extended Data (DRED) data, so that debuggers and debugger extensions can access DRED data.

## -struct-fields

### -field Version

A [D3D12_DRED_VERSION](ne-d3d12-d3d12_dred_version.md) value, specifying a DRED version. This value determines which inner data member (of the union) is active.

### -field Dred_1_0

A [D3D12_DEVICE_REMOVED_EXTENDED_DATA](ns-d3d12-d3d12_device_removed_extended_data.md) value, containing DRED version 1.0 data.

### -field Dred_1_1

A [D3D12_DEVICE_REMOVED_EXTENDED_DATA1](ns-d3d12-d3d12_device_removed_extended_data1.md) value, containing DRED version 1.1 data.

## -see-also

* [Core structures](/windows/desktop/direct3d12/direct3d-12-structures)
* [Use DRED to diagnose GPU faults](/windows/desktop/direct3d12/use-dred)

