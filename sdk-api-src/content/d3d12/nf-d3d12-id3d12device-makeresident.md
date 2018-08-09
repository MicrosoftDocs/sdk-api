---
UID: NF:d3d12.ID3D12Device.MakeResident
title: ID3D12Device::MakeResident
author: windows-sdk-content
description: Makes objects resident for the device.
old-location: direct3d12\id3d12device_makeresident.htm
old-project: direct3d12
ms.assetid: 2B3B97DC-5AA3-470E-8EED-3956B295BB94
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: ID3D12Device interface,MakeResident method, ID3D12Device.MakeResident, ID3D12Device::MakeResident, MakeResident, MakeResident method, MakeResident method,ID3D12Device interface, d3d12/ID3D12Device::MakeResident, direct3d12.id3d12device_makeresident
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: D3D_SHADER_MODEL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12Device.MakeResident
product: Windows
targetos: Windows
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
---

# ID3D12Device::MakeResident


## -description


Makes objects resident for the device.


## -parameters




### -param NumObjects

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of objects  in the <i>ppObjects</i> array to make resident for the device.
          


### -param ppObjects [in]

Type: <b><a href="https://msdn.microsoft.com/89DC88B4-9DFD-413D-8EB9-91087CC90D18">ID3D12Pageable</a>*</b>

A pointer to a memory block that contains an array of <a href="https://msdn.microsoft.com/89DC88B4-9DFD-413D-8EB9-91087CC90D18">ID3D12Pageable</a> interface pointers for the objects.
          

Even though most D3D12 objects inherit from <a href="https://msdn.microsoft.com/89DC88B4-9DFD-413D-8EB9-91087CC90D18">ID3D12Pageable</a>, residency changes are only supported on the following objects:
Descriptor Heaps, Heaps, Committed Resources, and Query Heaps


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.
          




## -remarks



<b>MakeResident</b> loads the data associated with a resource from disk, and re-allocates the memory from the resource's appropriate memory pool. This method should be called on the object which owns the physical memory.


Use this method, and <a href="https://msdn.microsoft.com/37F8ABA7-EDA3-4775-8B86-470FC4F95662">Evict</a>, to manage GPU video memory, noting that this was done automatically in D3D11, but now has to be done by the app in D3D12.

<b>MakeResident</b> and <a href="https://msdn.microsoft.com/37F8ABA7-EDA3-4775-8B86-470FC4F95662">Evict</a> can help applications manage the residency budget on many adapters. <b>MakeResident</b> explicitly pages-in data and, then, precludes page-out so the GPU can access the data. <b>Evict</b> enables page-out.

Some GPU architectures do not benefit from residency manipulation, due to the lack of sufficient GPU virtual address space. Use <a href="https://msdn.microsoft.com/2CBED491-A8B6-47AE-8371-2081BAF85B83">D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT</a> and <a href="https://msdn.microsoft.com/A2F95FE5-CF8D-4F17-8CC8-62AAA40B71FC">IDXGIAdapter3::QueryVideoMemoryInfo</a> to recognize when the maximum GPU VA space per-process is too small or roughly the same size as the residency budget. For such architectures, the residency budget will always be constrained by the amount of GPU virtual address space. <a href="https://msdn.microsoft.com/37F8ABA7-EDA3-4775-8B86-470FC4F95662">Evict</a> will not free-up any residency budget on such systems.


Applications must handle <b>MakeResident</b> failures, even if there appears to be enough residency budget available. Physical memory fragmentation and adapter architecture quirks can preclude the utilization of large contiguous ranges. Applications should free up more residency budget before trying again.


<b>MakeResident</b> is ref-counted, such that <a href="https://msdn.microsoft.com/37F8ABA7-EDA3-4775-8B86-470FC4F95662">Evict</a> must be called the same amount of times as <b>MakeResident</b> before <b>Evict</b> takes effect. Objects that support residency are made resident during creation, so a single <b>Evict</b> call will actually evict the object. 

Applications must use fences to ensure the GPU doesn't use non-resident objects. <b>MakeResident</b> must return before the GPU executes a command list that references the object. <a href="https://msdn.microsoft.com/37F8ABA7-EDA3-4775-8B86-470FC4F95662">Evict</a> must be called after the GPU finishes executing a command list that references the object.

Evicted objects still consume the same GPU virtual address and same amount of GPU virtual address space. Therefore, resource descriptors and other GPU virtual address references are not invalidated after <a href="https://msdn.microsoft.com/37F8ABA7-EDA3-4775-8B86-470FC4F95662">Evict</a>.




## -see-also




<a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>
 

 

