---
UID: NS:d3d12.D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT
title: D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT (d3d12.h)
description: Details the adapter's GPU virtual address space limitations, including maximum address bits per resource and per process.
helpviewer_keywords: ["D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT","D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT structure","d3d12/D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT","direct3d12.d3d12_feature_data_gpu_virtual_address_support"]
old-location: direct3d12\d3d12_feature_data_gpu_virtual_address_support.htm
tech.root: direct3d12
ms.assetid: 2CBED491-A8B6-47AE-8371-2081BAF85B83
ms.date: 12/05/2018
ms.keywords: D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT, D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT structure, d3d12/D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT, direct3d12.d3d12_feature_data_gpu_virtual_address_support
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
req.typenames: D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT
 - d3d12/D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT
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
 - D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT
---

# D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT structure


## -description

Details the adapter's GPU virtual address space limitations, including maximum address bits per resource and per process.

## -struct-fields

### -field MaxGPUVirtualAddressBitsPerResource

The maximum GPU virtual address bits per resource.

Some adapters have significantly less bits available per resource than per process, while other adapters have significantly greater bits available per resource than per process. The latter scenario tends to happen in less common scenarios, like when running a 32-bit process on certain UMA adapters.
When per resource capabilities are greater than per process, the greater per resource capabilities can only be leveraged by reserved resources or NULL mapped pages.

### -field MaxGPUVirtualAddressBitsPerProcess

The maximum GPU virtual address bits per process.

When this value is nearly equal to the available residency budget, <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-evict">Evict</a> will not be a feasible option to manage residency. See <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-makeresident">MakeResident</a> for more details.

## -remarks

See the enumeration constant D3D12_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT in the <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature">D3D12_FEATURE</a> enumeration.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>



<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature">D3D12_FEATURE</a>