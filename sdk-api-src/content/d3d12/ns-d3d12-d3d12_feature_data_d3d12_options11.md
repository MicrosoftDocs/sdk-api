---
UID: NS:d3d12.D3D12_FEATURE_DATA_D3D12_OPTIONS11
title: D3D12_FEATURE_DATA_D3D12_OPTIONS11
description: Indicates whether or not 64-bit integer atomics on resources in descriptor heaps are supported.
tech.root: direct3d12
ms.date: 07/21/2021
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
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.typenames: D3D12_FEATURE_DATA_D3D12_OPTIONS11
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - D3D12_FEATURE_DATA_D3D12_OPTIONS11
 - d3d12/D3D12_FEATURE_DATA_D3D12_OPTIONS11
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_FEATURE_DATA_D3D12_OPTIONS11
prerelease: false
---

## -description

Indicates whether or not 64-bit integer atomics on resources in descriptor heaps are supported.

## -struct-fields

### -field AtomicInt64OnDescriptorHeapResourceSupported

Type: \_Out\_ **[BOOL](/windows/desktop/winprog/windows-data-types)**

Indicates whether or not 64-bit integer atomics on resources in descriptor heaps are supported. `true` if supported, otherwise `false`.

## -remarks

## -see-also
