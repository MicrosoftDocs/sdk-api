---
UID: NF:d3d12.ID3D12Device3.EnqueueMakeResident
title: ID3D12Device3::EnqueueMakeResident
author: windows-sdk-content
description: Asynchronously makes objects resident for the device.
old-location: direct3d12\id3d12device3_enqueuemakeresident.htm
old-project: direct3d12
ms.assetid: A9F8D656-C09D-47D5-9D97-3C2A60422E96
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: EnqueueMakeResident, EnqueueMakeResident method, EnqueueMakeResident method,ID3D12Device3 interface, ID3D12Device3 interface,EnqueueMakeResident method, ID3D12Device3.EnqueueMakeResident, ID3D12Device3::EnqueueMakeResident, d3d12/ID3D12Device3::EnqueueMakeResident, direct3d12.id3d12device3_enqueuemakeresident
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
req.typenames: D3D_SHADER_MODEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D12.dll
api_name:
-	ID3D12Device3.EnqueueMakeResident
product: Windows
targetos: Windows
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
---

# ID3D12Device3::EnqueueMakeResident


## -description


Asynchronously makes objects resident for the device.


## -parameters




### -param Flags

Type: <b><a href="https://msdn.microsoft.com/87AC193A-4754-4E92-A08C-082C3C1513D6">D3D12_RESIDENCY_FLAGS</a></b>


            Controls whether the objects should be made resident if the application is over its memory budget.
          


### -param NumObjects

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


            The number of objects  in the <i>ppObjects</i> array to make resident for the device.
          


### -param ppObjects [in]

Type: <b><a href="https://msdn.microsoft.com/89DC88B4-9DFD-413D-8EB9-91087CC90D18">ID3D12Pageable</a>*</b>

A pointer to a memory block; contains an array of <a href="https://msdn.microsoft.com/89DC88B4-9DFD-413D-8EB9-91087CC90D18">ID3D12Pageable</a> interface pointers for the objects.
          

Even though most D3D12 objects inherit from <a href="https://msdn.microsoft.com/89DC88B4-9DFD-413D-8EB9-91087CC90D18">ID3D12Pageable</a>, residency changes are only supported on the following: 

<ul>
<li>descriptor heaps</li>
<li>heaps</li>
<li>committed resources</li>
<li>query heaps</li>
</ul>

### -param pFenceToSignal [in]

Type: <b><a href="https://msdn.microsoft.com/2B388352-EF43-4D1E-851C-A670B4681F0F">ID3D12Fence</a>*</b>

A pointer to the fence used to signal when the work is done.


### -param FenceValueToSignal

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a></b>

An unsigned 64-bit value signaled to the fence when the work is done.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>


            This method returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.
          




## -remarks



<b>EnqueueMakeResident</b> performs the same actions as <a href="https://msdn.microsoft.com/2B3B97DC-5AA3-470E-8EED-3956B295BB94">MakeResident</a>, but does not wait for the resources to be made resident. Instead, <b>EnqueueMakeResident</b> signals a fence when the work is done. 

The system will not allow work that references the resources that are being made resident by using <b>EnqueueMakeResident</b> before its fence is signaled. Instead, calls to this API are guaranteed to signal their corresponding fence in order, so the same fence can be used from call to call.




## -see-also




<a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>



<a href="https://msdn.microsoft.com/038E546C-4000-401A-8A11-7A83F391676E">ID3D12Device3</a>
 

 

