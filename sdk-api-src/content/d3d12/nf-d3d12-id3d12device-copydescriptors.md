---
UID: NF:d3d12.ID3D12Device.CopyDescriptors
title: ID3D12Device::CopyDescriptors (d3d12.h)
description: Copies descriptors from a source to a destination.
old-location: direct3d12\id3d12device_copydescriptors.htm
tech.root: direct3d12
ms.assetid: F995EF34-74FF-4FCA-A018-E2F48DF92450
ms.date: 12/05/2018
ms.keywords: CopyDescriptors, CopyDescriptors method, CopyDescriptors method,ID3D12Device interface, ID3D12Device interface,CopyDescriptors method, ID3D12Device.CopyDescriptors, ID3D12Device::CopyDescriptors, d3d12/ID3D12Device::CopyDescriptors, direct3d12.id3d12device_copydescriptors
f1_keywords:
- d3d12/ID3D12Device.CopyDescriptors
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
- ID3D12Device.CopyDescriptors
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12Device::CopyDescriptors


## -description


Copies descriptors from a source to a destination.
        


## -parameters




### -param NumDestDescriptorRanges [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of destination descriptor ranges to copy to.
          


### -param pDestDescriptorRangeStarts [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle">D3D12_CPU_DESCRIPTOR_HANDLE</a>*</b>

An array of CPU_descriptor_handle objects to copy to.
          


### -param pDestDescriptorRangeSizes [in, optional]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

An array of destination descriptor range sizes to copy to.
          


### -param NumSrcDescriptorRanges [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of source descriptor ranges to copy from.
          


### -param pSrcDescriptorRangeStarts [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle">D3D12_CPU_DESCRIPTOR_HANDLE</a>*</b>

An array of CPU_descriptor_handle objects to copy from.
          


### -param pSrcDescriptorRangeSizes [in, optional]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

An array of source descriptor range sizes to copy from.
          


### -param DescriptorHeapsType [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type">D3D12_DESCRIPTOR_HEAP_TYPE</a></b>

The <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type">D3D12_DESCRIPTOR_HEAP_TYPE</a>-typed value that specifies the type of descriptor heap to copy with.
          


## -returns



Returns nothing.
          




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/copying-descriptors">Copying Descriptors</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>
 

 

