---
UID: NF:d3d12.ID3D12Device.CopyDescriptorsSimple
title: ID3D12Device::CopyDescriptorsSimple (d3d12.h)
description: Copies descriptors from a source to a destination.helpviewer_keywords: ["CopyDescriptorsSimple","CopyDescriptorsSimple method","CopyDescriptorsSimple method","ID3D12Device interface","ID3D12Device interface","CopyDescriptorsSimple method","ID3D12Device.CopyDescriptorsSimple","ID3D12Device::CopyDescriptorsSimple","d3d12/ID3D12Device::CopyDescriptorsSimple","direct3d12.id3d12device_copydescriptorssimple"]
old-location: direct3d12\id3d12device_copydescriptorssimple.htm
tech.root: direct3d12
ms.assetid: 6DA1FCDA-042C-4727-9814-B8F57E14CD51
ms.date: 12/05/2018
ms.keywords: CopyDescriptorsSimple, CopyDescriptorsSimple method, CopyDescriptorsSimple method,ID3D12Device interface, ID3D12Device interface,CopyDescriptorsSimple method, ID3D12Device.CopyDescriptorsSimple, ID3D12Device::CopyDescriptorsSimple, d3d12/ID3D12Device::CopyDescriptorsSimple, direct3d12.id3d12device_copydescriptorssimple
f1_keywords:
- d3d12/ID3D12Device.CopyDescriptorsSimple
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D3D12.dll
api_name:
- ID3D12Device.CopyDescriptorsSimple
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12Device::CopyDescriptorsSimple


## -description


Copies descriptors from a source to a destination.
        


## -parameters




### -param NumDescriptors [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of descriptors to copy.
          


### -param DestDescriptorRangeStart [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle">D3D12_CPU_DESCRIPTOR_HANDLE</a></b>

A CPU_descriptor_handle that describes the destination descriptors to start to copy to.
          


### -param SrcDescriptorRangeStart [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle">D3D12_CPU_DESCRIPTOR_HANDLE</a></b>

A CPU_descriptor_handle that describes the source descriptors to start to copy from.
          


### -param DescriptorHeapsType [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type">D3D12_DESCRIPTOR_HEAP_TYPE</a></b>

The <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type">D3D12_DESCRIPTOR_HEAP_TYPE</a>-typed value that specifies the type of descriptor heap to copy with.
          


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/copying-descriptors">Copying Descriptors</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>
 

 

