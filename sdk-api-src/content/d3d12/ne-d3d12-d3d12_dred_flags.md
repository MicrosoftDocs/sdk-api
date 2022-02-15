---
UID: NE:d3d12.D3D12_DRED_FLAGS
title: D3D12_DRED_FLAGS
description: Defines constants used in the D3D12_DEVICE_REMOVED_EXTENDED_DATA structure to specify control flags for the Direct3D runtime.
tech.root: direct3d12
helpviewer_keywords: ["D3D12_DRED_FLAGS","D3D12_DRED_FLAGS enumeration","D3D12_DRED_FLAG_NONE","D3D12_DRED_FLAG_FORCE_ENABLE","D3D12_DRED_FLAG_DISABLE_AUTOBREADCRUMBS","d3d12/D3D12_DRED_FLAGS","d3d12/D3D12_DRED_FLAGS enumeration","d3d12/D3D12_DRED_FLAG_NONE","d3d12/D3D12_DRED_FLAG_FORCE_ENABLE","d3d12/D3D12_DRED_FLAG_DISABLE_AUTOBREADCRUMBS","direct3d12.d3d12_dred_flags"]
ms.date: 02/06/2019
ms.keywords: D3D12_DRED_FLAGS, D3D12_DRED_FLAGS enumeration, D3D12_DRED_FLAG_NONE, D3D12_DRED_FLAG_FORCE_ENABLE, D3D12_DRED_FLAG_DISABLE_AUTOBREADCRUMBS, d3d12/D3D12_DRED_FLAGS, d3d12/D3D12_DRED_FLAGS enumeration, d3d12/D3D12_DRED_FLAG_NONE, d3d12/D3D12_DRED_FLAG_FORCE_ENABLE, d3d12/D3D12_DRED_FLAG_DISABLE_AUTOBREADCRUMBS, direct3d12.d3d12_dred_flags
targetos: Windows
req.construct-type: enumeration
req.ddi-compliance: 
req.header: d3d12.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: D3D12_DRED_FLAGS
req.umdf-ver: 
ms.custom: 19H1
f1_keywords:
 - D3D12_DRED_FLAGS
 - d3d12/D3D12_DRED_FLAGS
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_DRED_FLAGS
---

# D3D12_DRED_FLAGS enumeration


## -description

> [!NOTE]
> As of Windows 10, version 1903, **D3D12_DRED_FLAGS** is deprecated, and it may not be available in future versions of Windows.

Defines constants used in the [D3D12_DEVICE_REMOVED_EXTENDED_DATA structure](ns-d3d12-d3d12_device_removed_extended_data.md) to specify control flags for the Direct3D runtime. Values can be bitwise OR'd together.

## -enum-fields

### -field D3D12_DRED_FLAG_NONE (0x0)

Typically specifies that Device Removed Extended Data (DRED) is disabled, except for when user-initiated feedback is used to produce a repro, or when otherwise enabled by Windows via automatic detection of process-instability issues. This is the default value.

### -field D3D12_DRED_FLAG_FORCE_ENABLE (0x1)

Forces DRED to be enabled, regardless of the system state.

### -field D3D12_DRED_FLAG_DISABLE_AUTOBREADCRUMBS (0x2)

Disables DRED auto breadcrumbs.

## -remarks

## -see-also

* [Core enumerations](/windows/desktop/direct3d12/direct3d-12-enumerations)
* [D3D12_DEVICE_REMOVED_EXTENDED_DATA structure](ns-d3d12-d3d12_device_removed_extended_data.md)
* [Use DRED to diagnose GPU faults](/windows/desktop/direct3d12/use-dred)

