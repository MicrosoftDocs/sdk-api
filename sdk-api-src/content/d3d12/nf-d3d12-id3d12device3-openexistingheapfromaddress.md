---
UID: NF:d3d12.ID3D12Device3.OpenExistingHeapFromAddress
title: ID3D12Device3::OpenExistingHeapFromAddress
author: windows-driver-content
description: Creates a special-purpose diagnostic heap in system memory from an address. The created heap can persist even in the event of a GPU-fault or device-removed scenario.
old-location: direct3d12\id3d12device3_openexistingheapfromaddress.htm
old-project: direct3d12
ms.assetid: E2343759-FC36-4638-AE91-F6BF6D0BC3BA
ms.author: windowsdriverdev
ms.date: 5/11/2018
ms.keywords: ID3D12Device3.OpenExistingHeapFromAddress, ID3D12Device3::OpenExistingHeapFromAddress, Id3d12device3 interface,OpenExistingHeapFromAddress method, Id3d12device3::OpenExistingHeapFromAddress, OpenExistingHeapFromAddress, OpenExistingHeapFromAddress method, OpenExistingHeapFromAddress method,Id3d12device3 interface, d3d12/Id3d12device3::OpenExistingHeapFromAddress, direct3d12.id3d12device3_openexistingheapfromaddress
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	d3d12.dll
api_name:
-	Id3d12device3.OpenExistingHeapFromAddress
product: Windows
targetos: Windows
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
---

# ID3D12Device3::OpenExistingHeapFromAddress


## -description


Creates a special-purpose diagnostic heap in system memory from an address. The created heap can persist even in the event of a GPU-fault or device-removed scenario.


## -parameters




### -param pAddress [in]

Type: <b>const void*</b>

The address used to create the heap.


### -param riid

Type: <b>REFIID</b>

The globally unique identifier (<b>GUID</b>) for the heap interface (<a href="https://msdn.microsoft.com/3791C64F-76D7-4580-A444-F2CEA3EB10CE">ID3D12Heap</a>).

The <b>REFIID</b>, or <b>GUID</b>, of the interface to the heap can be obtained by using the <b>__uuidof()</b> macro. For example, <b>__uuidof(ID3D12Heap)</b> will retrieve the <b>GUID</b> of the interface to a heap.


### -param ppvHeap [out]

Type: <b>void**</b>

<a href="https://msdn.microsoft.com/en-us/library/hh916382.aspx">SAL</a>: <code>_COM_Outptr_</code>

A pointer to a memory block; on success, returns a pointer to the <a href="https://msdn.microsoft.com/3791C64F-76D7-4580-A444-F2CEA3EB10CE">ID3D12Heap</a> interface for the pipeline state object.

The pipeline state object is an immutable state object. It contains no methods.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns <b>E_OUTOFMEMORY</b> if there is insufficient memory to create the pipeline state object. See <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a> for other possible return values.




## -remarks



The heap is created in system memory and permits CPU access. It wraps the entire VirtualAlloc region.

Heaps can be used for placed and reserved resources, as orthogonally as other heaps. Restrictions may still exist based on the flags that cannot be app-chosen.




## -see-also




<a href="https://msdn.microsoft.com/038E546C-4000-401A-8A11-7A83F391676E">Id3d12device3</a>
 

 

