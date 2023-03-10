---
UID: NF:d3d12.ID3D12Device.Evict
title: ID3D12Device::Evict (d3d12.h)
description: Enables the page-out of data, which precludes GPU access of that data.
helpviewer_keywords: ["Evict","Evict method","Evict method","ID3D12Device interface","ID3D12Device interface","Evict method","ID3D12Device.Evict","ID3D12Device::Evict","d3d12/ID3D12Device::Evict","direct3d12.id3d12device_evict"]
old-location: direct3d12\id3d12device_evict.htm
tech.root: direct3d12
ms.assetid: 37F8ABA7-EDA3-4775-8B86-470FC4F95662
ms.date: 12/05/2018
ms.keywords: Evict, Evict method, Evict method,ID3D12Device interface, ID3D12Device interface,Evict method, ID3D12Device.Evict, ID3D12Device::Evict, d3d12/ID3D12Device::Evict, direct3d12.id3d12device_evict
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
 - ID3D12Device::Evict
 - d3d12/ID3D12Device::Evict
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
 - ID3D12Device.Evict
---

# ID3D12Device::Evict


## -description

Enables the page-out of data, which precludes GPU access of that data.

## -parameters

### -param NumObjects

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of objects in the <i>ppObjects</i> array to evict from the device.

### -param ppObjects [in]

Type: <b><a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12pageable">ID3D12Pageable</a>*</b>

A pointer to a memory block that contains an array of <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12pageable">ID3D12Pageable</a> interface pointers for the objects.
          

Even though most D3D12 objects inherit from <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12pageable">ID3D12Pageable</a>, residency changes are only supported on the following objects:
Descriptor Heaps, Heaps, Committed Resources, and Query Heaps

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -remarks

<b>Evict</b> persists the data associated with a resource to disk, and then removes the resource from the memory pool where it was located. This method should be called on the object which owns the physical memory: either a committed resource (which owns both virtual  and physical memory assignments) or a heap - noting that reserved resources do not have physical memory, and placed resources are borrowing memory from a heap.


Refer to the remarks for <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-makeresident">MakeResident</a>.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>