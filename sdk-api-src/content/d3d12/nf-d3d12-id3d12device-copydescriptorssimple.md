---
UID: NF:d3d12.ID3D12Device.CopyDescriptorsSimple
title: ID3D12Device::CopyDescriptorsSimple (d3d12.h)
description: Copies descriptors from a source to a destination. (ID3D12Device.CopyDescriptorsSimple)
helpviewer_keywords: ["CopyDescriptorsSimple","CopyDescriptorsSimple method","CopyDescriptorsSimple method","ID3D12Device interface","ID3D12Device interface","CopyDescriptorsSimple method","ID3D12Device.CopyDescriptorsSimple","ID3D12Device::CopyDescriptorsSimple","d3d12/ID3D12Device::CopyDescriptorsSimple","direct3d12.id3d12device_copydescriptorssimple"]
old-location: direct3d12\id3d12device_copydescriptorssimple.htm
tech.root: direct3d12
ms.assetid: 6DA1FCDA-042C-4727-9814-B8F57E14CD51
ms.date: 12/05/2018
ms.keywords: CopyDescriptorsSimple, CopyDescriptorsSimple method, CopyDescriptorsSimple method,ID3D12Device interface, ID3D12Device interface,CopyDescriptorsSimple method, ID3D12Device.CopyDescriptorsSimple, ID3D12Device::CopyDescriptorsSimple, d3d12/ID3D12Device::CopyDescriptorsSimple, direct3d12.id3d12device_copydescriptorssimple
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
 - ID3D12Device::CopyDescriptorsSimple
 - d3d12/ID3D12Device::CopyDescriptorsSimple
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
 - ID3D12Device.CopyDescriptorsSimple
---

# ID3D12Device::CopyDescriptorsSimple


## -description

Copies descriptors from a source to a destination.

## -parameters

### -param NumDescriptors [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of descriptors to copy.

### -param DestDescriptorRangeStart [in]

Type: <b><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle">D3D12_CPU_DESCRIPTOR_HANDLE</a></b>

A <b><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle">D3D12_CPU_DESCRIPTOR_HANDLE</a></b> that describes the destination descriptors to start to copy to.

The destination and source descriptors must be in heaps of the same [D3D12_DESCRIPTOR_HEAP_TYPE](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type).

### -param SrcDescriptorRangeStart [in]

Type: <b><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle">D3D12_CPU_DESCRIPTOR_HANDLE</a></b>

A <b><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle">D3D12_CPU_DESCRIPTOR_HANDLE</a></b> that describes the source descriptors to start to copy from.

> [!IMPORTANT]
> The *SrcDescriptorRangeStart* parameter must be in a non shader-visible descriptor heap. This is because shader-visible descriptor heaps may be created in **WRITE_COMBINE** memory or GPU local memory, which is prohibitively slow to read from. If your application manages descriptor heaps via copying the descriptors required for a given pass or frame from local "storage" descriptor heaps to the GPU-bound descriptor heap, then use shader-opaque heaps for the storage heaps and copy into the GPU-visible heap as required.

### -param DescriptorHeapsType [in]

Type: <b><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type">D3D12_DESCRIPTOR_HEAP_TYPE</a></b>

The <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type">D3D12_DESCRIPTOR_HEAP_TYPE</a>-typed value that specifies the type of descriptor heap to copy with. This is required as different descriptor types may have different sizes.

Both the source and destination descriptor heaps must have the same type, else the debug layer will emit an error.

## -remarks

Where applicable, prefer this method to [**ID3D12Device::CopyDescriptors**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptors). It can have a better CPU cache miss rate due to the linear nature of the copy.

## -see-also

<a href="/windows/desktop/direct3d12/copying-descriptors">Copying Descriptors</a>



<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>
