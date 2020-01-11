---
UID: NS:d3d12.D3D12_RESOURCE_ALLOCATION_INFO
title: D3D12_RESOURCE_ALLOCATION_INFO
description: Describes parameters needed to allocate resources.
old-location: direct3d12\d3d12_resource_allocation_info.htm
tech.root: direct3d12
ms.assetid: ADBF5402-C1B5-4A10-92DF-E9F5706F52A1
ms.date: 12/05/2018
ms.keywords: D3D12_RESOURCE_ALLOCATION_INFO, D3D12_RESOURCE_ALLOCATION_INFO structure, d3d12/D3D12_RESOURCE_ALLOCATION_INFO, direct3d12.d3d12_resource_allocation_info
f1_keywords:
- d3d12/D3D12_RESOURCE_ALLOCATION_INFO
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- D3D12.h
api_name:
- D3D12_RESOURCE_ALLOCATION_INFO
targetos: Windows
req.typenames: D3D12_RESOURCE_ALLOCATION_INFO
req.redist: 
ms.custom: 19H1
---

## -description

Describes parameters needed to allocate resources.

## -struct-fields

### -field SizeInBytes

Type: **[UINT64](/windows/win32/WinProg/windows-data-types)**

The size, in bytes, of the resource.

### -field Alignment

Type: **[UINT64](/windows/win32/WinProg/windows-data-types)**

The alignment value for the resource; one of 4KB (4096), 64KB (65536), or 4MB (4194304) alignment.

## -remarks

This structure is used by the [ID3D12Device::GetResourceAllocationInfo](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo) and [ID3D12Device::GetResourceAllocationInfo1](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-getresourceallocationinfo1) methods.

## -see-also

[CD3DX12_RESOURCE_ALLOCATION_INFO](/windows/win32/direct3d12/cd3dx12-resource-allocation-info)

[Core structures](/windows/win32/direct3d12/direct3d-12-structures)
