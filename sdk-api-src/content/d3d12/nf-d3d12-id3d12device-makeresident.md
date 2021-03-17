---
UID: NF:d3d12.ID3D12Device.MakeResident
title: ID3D12Device::MakeResident (d3d12.h)
description: Makes objects resident for the device.
helpviewer_keywords: ["ID3D12Device interface","MakeResident method","ID3D12Device.MakeResident","ID3D12Device::MakeResident","MakeResident","MakeResident method","MakeResident method","ID3D12Device interface","d3d12/ID3D12Device::MakeResident","direct3d12.id3d12device_makeresident"]
old-location: direct3d12\id3d12device_makeresident.htm
tech.root: direct3d12
ms.assetid: 2B3B97DC-5AA3-470E-8EED-3956B295BB94
ms.date: 12/05/2018
ms.keywords: ID3D12Device interface,MakeResident method, ID3D12Device.MakeResident, ID3D12Device::MakeResident, MakeResident, MakeResident method, MakeResident method,ID3D12Device interface, d3d12/ID3D12Device::MakeResident, direct3d12.id3d12device_makeresident
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
 - ID3D12Device::MakeResident
 - d3d12/ID3D12Device::MakeResident
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
 - ID3D12Device.MakeResident
---

# ID3D12Device::MakeResident


## -description

Makes objects resident for the device.

## -parameters

### -param NumObjects

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of objects  in the <i>ppObjects</i> array to make resident for the device.

### -param ppObjects [in]

Type: <b><a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12pageable">ID3D12Pageable</a>*</b>

A pointer to a memory block that contains an array of <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12pageable">ID3D12Pageable</a> interface pointers for the objects.
          

Even though most D3D12 objects inherit from <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12pageable">ID3D12Pageable</a>, residency changes are only supported on the following objects:
Descriptor Heaps, Heaps, Committed Resources, and Query Heaps

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -remarks

<b>MakeResident</b> loads the data associated with a resource from disk, and re-allocates the memory from the resource's appropriate memory pool. This method should be called on the object which owns the physical memory.


Use this method, and <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-evict">Evict</a>, to manage GPU video memory, noting that this was done automatically in D3D11, but now has to be done by the app in D3D12.

<b>MakeResident</b> and <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-evict">Evict</a> can help applications manage the residency budget on many adapters. <b>MakeResident</b> explicitly pages-in data and, then, precludes page-out so the GPU can access the data. <b>Evict</b> enables page-out.

Some GPU architectures do not benefit from residency manipulation, due to the lack of sufficient GPU virtual address space. Use <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support">D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT</a> and <a href="/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo">IDXGIAdapter3::QueryVideoMemoryInfo</a> to recognize when the maximum GPU VA space per-process is too small or roughly the same size as the residency budget. For such architectures, the residency budget will always be constrained by the amount of GPU virtual address space. <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-evict">Evict</a> will not free-up any residency budget on such systems.


Applications must handle <b>MakeResident</b> failures, even if there appears to be enough residency budget available. Physical memory fragmentation and adapter architecture quirks can preclude the utilization of large contiguous ranges. Applications should free up more residency budget before trying again.


<b>MakeResident</b> is ref-counted, such that <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-evict">Evict</a> must be called the same amount of times as <b>MakeResident</b> before <b>Evict</b> takes effect. Objects that support residency are made resident during creation, so a single <b>Evict</b> call will actually evict the object. 

Applications must use fences to ensure the GPU doesn't use non-resident objects. <b>MakeResident</b> must return before the GPU executes a command list that references the object. <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-evict">Evict</a> must be called after the GPU finishes executing a command list that references the object.

Evicted objects still consume the same GPU virtual address and same amount of GPU virtual address space. Therefore, resource descriptors and other GPU virtual address references are not invalidated after <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-evict">Evict</a>.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>