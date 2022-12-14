---
UID: NF:d3d12.ID3D12Device.CopyDescriptors
title: ID3D12Device::CopyDescriptors (d3d12.h)
description: Copies descriptors from a source to a destination. (ID3D12Device.CopyDescriptors)
helpviewer_keywords: ["CopyDescriptors","CopyDescriptors method","CopyDescriptors method","ID3D12Device interface","ID3D12Device interface","CopyDescriptors method","ID3D12Device.CopyDescriptors","ID3D12Device::CopyDescriptors","d3d12/ID3D12Device::CopyDescriptors","direct3d12.id3d12device_copydescriptors"]
old-location: direct3d12\id3d12device_copydescriptors.htm
tech.root: direct3d12
ms.assetid: F995EF34-74FF-4FCA-A018-E2F48DF92450
ms.date: 12/05/2018
ms.keywords: CopyDescriptors, CopyDescriptors method, CopyDescriptors method,ID3D12Device interface, ID3D12Device interface,CopyDescriptors method, ID3D12Device.CopyDescriptors, ID3D12Device::CopyDescriptors, d3d12/ID3D12Device::CopyDescriptors, direct3d12.id3d12device_copydescriptors
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12Device::CopyDescriptors
 - d3d12/ID3D12Device::CopyDescriptors
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12Device.CopyDescriptors
---

## -description

Copies descriptors from a source to a destination.

## -parameters

### -param NumDestDescriptorRanges [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of destination descriptor ranges to copy to.

### -param pDestDescriptorRangeStarts [in]

Type: <b>const <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle">D3D12_CPU_DESCRIPTOR_HANDLE</a>*</b>

An array of <b><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle">D3D12_CPU_DESCRIPTOR_HANDLE</a></b> objects to copy to.

All the destination and source descriptors must be in heaps of the same [D3D12_DESCRIPTOR_HEAP_TYPE](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type).

### -param pDestDescriptorRangeSizes [in, optional]

Type: <b>const <a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

An array of destination descriptor range sizes to copy to.

### -param NumSrcDescriptorRanges [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of source descriptor ranges to copy from.

### -param pSrcDescriptorRangeStarts [in]

Type: <b>const <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle">D3D12_CPU_DESCRIPTOR_HANDLE</a>*</b>

An array of <b><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle">D3D12_CPU_DESCRIPTOR_HANDLE</a></b> objects to copy from.

> [!IMPORTANT]
> All elements in the *pSrcDescriptorRangeStarts* parameter must be in a non shader-visible descriptor heap. This is because shader-visible descriptor heaps may be created in **WRITE_COMBINE** memory or GPU local memory, which is prohibitively slow to read from. If your application manages descriptor heaps via copying the descriptors required for a given pass or frame from local "storage" descriptor heaps to the GPU-bound descriptor heap, use shader-opaque heaps for the storage heaps and copy into the GPU-visible heap as required.

### -param pSrcDescriptorRangeSizes [in, optional]

Type: <b>const <a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

An array of source descriptor range sizes to copy from.

### -param DescriptorHeapsType [in]

Type: <b><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type">D3D12_DESCRIPTOR_HEAP_TYPE</a></b>

The <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type">D3D12_DESCRIPTOR_HEAP_TYPE</a>-typed value that specifies the type of descriptor heap to copy with. This is required as different descriptor types may have different sizes.

Both the source and destination descriptor heaps must have the same type, else the debug layer will emit an error.

## -remarks

Where applicable, prefer [**ID3D12Device::CopyDescriptorsSimple**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) to this method. It can have a better CPU cache miss rate due to the linear nature of the copy.

## -see-also

<a href="/windows/desktop/direct3d12/copying-descriptors">Copying Descriptors</a>



<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>
