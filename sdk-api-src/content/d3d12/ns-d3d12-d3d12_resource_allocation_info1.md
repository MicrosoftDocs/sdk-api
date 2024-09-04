---
UID: NS:d3d12.D3D12_RESOURCE_ALLOCATION_INFO1
title: D3D12_RESOURCE_ALLOCATION_INFO1
description: Describes parameters needed to allocate resources, including offset.
helpviewer_keywords: ["D3D12_RESOURCE_ALLOCATION_INFO1","D3D12_RESOURCE_ALLOCATION_INFO1 structure","d3d12/D3D12_RESOURCE_ALLOCATION_INFO1","direct3d12.d3d12_resource_allocation_info1"]
tech.root: direct3d12
ms.date: 12/05/2018
ms.keywords: D3D12_RESOURCE_ALLOCATION_INFO1, D3D12_RESOURCE_ALLOCATION_INFO1 structure, d3d12/D3D12_RESOURCE_ALLOCATION_INFO1, direct3d12.d3d12_resource_allocation_info1
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
req.typenames: D3D12_RESOURCE_ALLOCATION_INFO1
req.redist: 
f1_keywords:
 - D3D12_RESOURCE_ALLOCATION_INFO1
 - d3d12/D3D12_RESOURCE_ALLOCATION_INFO1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_RESOURCE_ALLOCATION_INFO1
---

## -description

Describes parameters needed to allocate resources, including offset.

## -struct-fields

### -field Offset

Type: **[UINT64](/windows/win32/WinProg/windows-data-types)**

The offset, in bytes, of the resource.

### -field Alignment

Type: **[UINT64](/windows/win32/WinProg/windows-data-types)**

The alignment value for the resource; one of 4KB (4096), 64KB (65536), or 4MB (4194304) alignment.

### -field SizeInBytes

Type: **[UINT64](/windows/win32/WinProg/windows-data-types)**

The size, in bytes, of the resource.

## -remarks

This structure is used by the [ID3D12Device::GetResourceAllocationInfo1](./nf-d3d12-id3d12device4-getresourceallocationinfo1(uint_uint_constd3d12_resource_desc_d3d12_resource_allocation_info1).md) method.

## -see-also

[Core structures](/windows/win32/direct3d12/direct3d-12-structures)
