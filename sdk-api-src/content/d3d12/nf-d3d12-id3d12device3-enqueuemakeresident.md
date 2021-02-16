---
UID: NF:d3d12.ID3D12Device3.EnqueueMakeResident
title: ID3D12Device3::EnqueueMakeResident (d3d12.h)
description: Asynchronously makes objects resident for the device.
helpviewer_keywords: ["EnqueueMakeResident","EnqueueMakeResident method","EnqueueMakeResident method","ID3D12Device3 interface","ID3D12Device3 interface","EnqueueMakeResident method","ID3D12Device3.EnqueueMakeResident","ID3D12Device3::EnqueueMakeResident","d3d12/ID3D12Device3::EnqueueMakeResident","direct3d12.id3d12device3_enqueuemakeresident"]
old-location: direct3d12\id3d12device3_enqueuemakeresident.htm
tech.root: direct3d12
ms.assetid: A9F8D656-C09D-47D5-9D97-3C2A60422E96
ms.date: 12/05/2018
ms.keywords: EnqueueMakeResident, EnqueueMakeResident method, EnqueueMakeResident method,ID3D12Device3 interface, ID3D12Device3 interface,EnqueueMakeResident method, ID3D12Device3.EnqueueMakeResident, ID3D12Device3::EnqueueMakeResident, d3d12/ID3D12Device3::EnqueueMakeResident, direct3d12.id3d12device3_enqueuemakeresident
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
 - ID3D12Device3::EnqueueMakeResident
 - d3d12/ID3D12Device3::EnqueueMakeResident
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
 - ID3D12Device3.EnqueueMakeResident
---

# ID3D12Device3::EnqueueMakeResident


## -description

Asynchronously makes objects resident for the device.

## -parameters

### -param Flags

Type: <b><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_residency_flags">D3D12_RESIDENCY_FLAGS</a></b>

Controls whether the objects should be made resident if the application is over its memory budget.

### -param NumObjects

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of objects  in the <i>ppObjects</i> array to make resident for the device.

### -param ppObjects [in]

Type: <b><a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12pageable">ID3D12Pageable</a>*</b>

A pointer to a memory block; contains an array of <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12pageable">ID3D12Pageable</a> interface pointers for the objects.
          

Even though most D3D12 objects inherit from <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12pageable">ID3D12Pageable</a>, residency changes are only supported on the following: 

<ul>
<li>descriptor heaps</li>
<li>heaps</li>
<li>committed resources</li>
<li>query heaps</li>
</ul>

### -param pFenceToSignal [in]

Type: <b><a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12fence">ID3D12Fence</a>*</b>

A pointer to the fence used to signal when the work is done.

### -param FenceValueToSignal

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a></b>

An unsigned 64-bit value signaled to the fence when the work is done.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -remarks

<b>EnqueueMakeResident</b> performs the same actions as <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-makeresident">MakeResident</a>, but does not wait for the resources to be made resident. Instead, <b>EnqueueMakeResident</b> signals a fence when the work is done. 

The system will not allow work that references the resources that are being made resident by using <b>EnqueueMakeResident</b> before its fence is signaled. Instead, calls to this API are guaranteed to signal their corresponding fence in order, so the same fence can be used from call to call.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>



<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device3">ID3D12Device3</a>