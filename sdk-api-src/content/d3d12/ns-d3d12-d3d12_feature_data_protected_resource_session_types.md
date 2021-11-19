---
UID: NS:d3d12.D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_TYPES
title: D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_TYPES
description: Indicates a list of protected resource session types.
tech.root: direct3d12
ms.date: 07/26/2021
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
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_TYPES
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_TYPES
 - d3d12/D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_TYPES
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_TYPES
---

## -description

Indicates a list of protected resource session types.

## -struct-fields

### -field NodeIndex

Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

An input parameter which, in multi-adapter operation, indicates which physical adapter of the device this operation applies to.

### -field Count

Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

An input parameter indicating the size of the *pTypes* array. This must match the count returned through the [D3D12_FEATURE_PROTECTED_RESOURCE_SESSION_TYPE_COUNT](ne-d3d12-d3d12_feature.md) query.

### -field pTypes

Type: **[GUID](/windows/desktop/winprog/windows-data-types)\***

An output parameter containing an array populated with the supported protected resource session types.

## -remarks

## -see-also
