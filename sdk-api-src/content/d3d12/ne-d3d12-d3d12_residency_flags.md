---
UID: NE:d3d12.D3D12_RESIDENCY_FLAGS
title: D3D12_RESIDENCY_FLAGS (d3d12.h)
description: Used with the EnqueuMakeResident function to choose how residency operations proceed when the memory budget is exceeded.
helpviewer_keywords: ["D3D12_RESIDENCY_FLAGS","D3D12_RESIDENCY_FLAGS enumeration","D3D12_RESIDENCY_FLAG_DENY_OVERBUDGET","D3D12_RESIDENCY_FLAG_NONE","d3d12/D3D12_RESIDENCY_FLAGS","d3d12/D3D12_RESIDENCY_FLAG_DENY_OVERBUDGET","d3d12/D3D12_RESIDENCY_FLAG_NONE","direct3d12.d3d12_residency_flags"]
old-location: direct3d12\d3d12_residency_flags.htm
tech.root: direct3d12
ms.assetid: 87AC193A-4754-4E92-A08C-082C3C1513D6
ms.date: 12/05/2018
ms.keywords: D3D12_RESIDENCY_FLAGS, D3D12_RESIDENCY_FLAGS enumeration, D3D12_RESIDENCY_FLAG_DENY_OVERBUDGET, D3D12_RESIDENCY_FLAG_NONE, d3d12/D3D12_RESIDENCY_FLAGS, d3d12/D3D12_RESIDENCY_FLAG_DENY_OVERBUDGET, d3d12/D3D12_RESIDENCY_FLAG_NONE, direct3d12.d3d12_residency_flags
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: D3D12_RESIDENCY_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_RESIDENCY_FLAGS
 - d3d12/D3D12_RESIDENCY_FLAGS
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
 - D3D12_RESIDENCY_FLAGS
---

# D3D12_RESIDENCY_FLAGS enumeration


## -description

Used with the EnqueuMakeResident function to choose how residency operations proceed when the memory budget is exceeded.

## -enum-fields

### -field D3D12_RESIDENCY_FLAG_NONE:0

Specifies the default residency policy, which allows residency operations to succeed regardless of the application's current memory budget. EnqueueMakeResident returns E_OUTOFMEMORY only when there is no memory available.

### -field D3D12_RESIDENCY_FLAG_DENY_OVERBUDGET:0x1

Specifies that the EnqueueMakeResident function should return E_OUTOFMEMORY when the residency operation would exceed the application's current memory budget.

## -remarks

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
