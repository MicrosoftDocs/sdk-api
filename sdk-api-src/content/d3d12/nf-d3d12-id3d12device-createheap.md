---
UID: NF:d3d12.ID3D12Device.CreateHeap
title: ID3D12Device::CreateHeap
author: windows-sdk-content
description: Creates a heap that can be used with placed resources and reserved resources.
old-location: direct3d12\id3d12device_createheap.htm
old-project: direct3d12
ms.assetid: DB5DF4B2-4673-4B8D-BDED-9F672A41E7F6
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: CreateHeap, CreateHeap method, CreateHeap method,ID3D12Device interface, ID3D12Device interface,CreateHeap method, ID3D12Device.CreateHeap, ID3D12Device::CreateHeap, d3d12/ID3D12Device::CreateHeap, direct3d12.id3d12device_createheap
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
-	ID3D12Device.CreateHeap
product: Windows
targetos: Windows
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
---

# ID3D12Device::CreateHeap


## -description



          Creates a heap that can be used with placed resources and reserved resources.
        


## -parameters




### -param pDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/3A473476-F37E-4F01-B121-87E998EE9411">D3D12_HEAP_DESC</a>*</b>


            A pointer to a <a href="https://msdn.microsoft.com/3A473476-F37E-4F01-B121-87E998EE9411">D3D12_HEAP_DESC</a> structure that describes the heap.
          


### -param riid

Type: <b><b>REFIID</b></b>


            The globally unique identifier (<b>GUID</b>) for the heap interface.
            This is an input parameter.
            The <b>REFIID</b>, or <b>GUID</b>, of the interface to the heap can be obtained by using the __uuidof() macro.
            For example, __uuidof(<a href="https://msdn.microsoft.com/3791C64F-76D7-4580-A444-F2CEA3EB10CE">ID3D12Heap</a>) will get the <b>GUID</b> of the interface to a heap.
            <i>riid</i> is, most commonly, the GUID for <b>ID3D12Heap</b>, but it may be any GUID for any interface.
            If the resource object does not support the interface for the specified GUID, creation will fail with E_NOINTERFACE.
          


### -param ppvHeap [out, optional]

Type: <b><b>void</b>**</b>


            A pointer to a memory block that receives a pointer to the heap.
            <i>ppvHeap</i> can be NULL, to enable capability testing.
            When <i>ppvHeap</i> is NULL, no object will be created and S_FALSE will be returned when <i>pDesc</i> is valid.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>


            This method returns <b>E_OUTOFMEMORY</b> if there is insufficient memory to create the heap.
            See <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a> for other possible return values.
          




## -remarks



<b>CreateHeap</b> creates a heap that can be used with placed resources and reserved resources.
          Before releasing the final reference on the heap, the application must ensure that the GPU will no longer read or write to this heap.
          Placed resource objects will hold a reference on the heap they are created on, but reserved resources will not hold a reference for each mapping made to a heap.
        




## -see-also




<a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>



<a href="https://msdn.microsoft.com/67C6B1D4-BF76-45A9-BADC-7C9520C900EB">Shared Heaps</a>
 

 

