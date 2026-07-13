---
UID: NF:d3d12.ID3D12Device3.OpenExistingHeapFromAddress
title: ID3D12Device3::OpenExistingHeapFromAddress (d3d12.h)
description: Creates a special-purpose diagnostic heap in system memory from an address. The created heap can persist even in the event of a GPU-fault or device-removed scenario.
helpviewer_keywords: ["ID3D12Device3.OpenExistingHeapFromAddress","ID3D12Device3::OpenExistingHeapFromAddress","Id3d12device3 interface","OpenExistingHeapFromAddress method","Id3d12device3::OpenExistingHeapFromAddress","OpenExistingHeapFromAddress","OpenExistingHeapFromAddress method","OpenExistingHeapFromAddress method","Id3d12device3 interface","d3d12/Id3d12device3::OpenExistingHeapFromAddress","direct3d12.id3d12device3_openexistingheapfromaddress"]
old-location: direct3d12\id3d12device3_openexistingheapfromaddress.htm
tech.root: direct3d12
ms.assetid: E2343759-FC36-4638-AE91-F6BF6D0BC3BA
ms.date: 08/10/2022
ms.keywords: ID3D12Device3.OpenExistingHeapFromAddress, ID3D12Device3::OpenExistingHeapFromAddress, Id3d12device3 interface,OpenExistingHeapFromAddress method, Id3d12device3::OpenExistingHeapFromAddress, OpenExistingHeapFromAddress, OpenExistingHeapFromAddress method, OpenExistingHeapFromAddress method,Id3d12device3 interface, d3d12/Id3d12device3::OpenExistingHeapFromAddress, direct3d12.id3d12device3_openexistingheapfromaddress
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
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12Device3::OpenExistingHeapFromAddress
 - d3d12/ID3D12Device3::OpenExistingHeapFromAddress
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - Id3d12device3.OpenExistingHeapFromAddress
---

## -description

Creates a special-purpose diagnostic heap in system memory from an address. The created heap can persist even in the event of a GPU-fault or device-removed scenario.

## -parameters

### -param pAddress [in]

Type: <b>const void*</b>

The address used to create the heap.

### -param riid

Type: <b>REFIID</b>

The globally unique identifier (<b>GUID</b>) for the heap interface (<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12heap">ID3D12Heap</a>).

The <b>REFIID</b>, or <b>GUID</b>, of the interface to the heap can be obtained by using the <b>__uuidof()</b> macro. For example, <b>__uuidof(ID3D12Heap)</b> will retrieve the <b>GUID</b> of the interface to a heap.

### -param ppvHeap [out]

Type: <b>void**</b>

<a href="/visualstudio/code-quality/annotating-function-parameters-and-return-values?view=vs-2015&preserve-view=true">SAL</a>: <code>_COM_Outptr_</code>

A pointer to a memory block. On success, the D3D12 runtime will write a pointer to the newly-opened heap into the memory block. The type of the pointer depends on the provided <b>riid</b> parameter.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns <b>E_OUTOFMEMORY</b> if there is insufficient memory to open the existing heap. See <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a> for other possible return values.

## -remarks

The heap is created in system memory and permits CPU access. It wraps the entire VirtualAlloc region.

Heaps can be used for placed and reserved resources, as orthogonally as other heaps. Restrictions may still exist based on the flags that cannot be app-chosen.

## -see-also

[ID3D12Device3 interface](./nn-d3d12-id3d12device3.md)