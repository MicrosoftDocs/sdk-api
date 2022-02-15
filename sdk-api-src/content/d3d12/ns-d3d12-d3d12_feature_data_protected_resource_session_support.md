---
UID: NS:d3d12.D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT
title: D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT
description: Indicates the level of support for protected resource sessions.
helpviewer_keywords: ["D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT"]
tech.root: direct3d12
ms.date: 05/20/2019
ms.keywords: D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT
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
req.typenames: D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT
 - d3d12/D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT
---

## -description

Indicates the level of support for protected resource sessions.

## -struct-fields

### -field NodeIndex

Type: **[UINT](/windows/desktop/WinProg/windows-data-types)**

An input field, indicating the adapter index to query.

### -field SharingTier

Type: **[D3D12_PROTECTED_RESOURCE_SESSION_SUPPORT_FLAGS](/windows/desktop/api/d3d12/ne-d3d12-d3d12_protected_resource_session_support_flags)**

An output field indicating the type of protected resource session support.

## -remarks

## -see-also

