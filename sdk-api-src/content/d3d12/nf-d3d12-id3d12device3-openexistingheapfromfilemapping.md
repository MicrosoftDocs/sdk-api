---
UID: NF:d3d12.ID3D12Device3.OpenExistingHeapFromFileMapping
title: ID3D12Device3::OpenExistingHeapFromFileMapping
description: Creates a special-purpose diagnostic heap in system memory from a file mapping object. The created heap can persist even in the event of a GPU-fault or device-removed scenario.
helpviewer_keywords: ["ID3D12Device3::OpenExistingHeapFromFileMapping"]
tech.root: direct3d12
ms.date: 08/10/2022
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
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
f1_keywords:
 - ID3D12Device3::OpenExistingHeapFromFileMapping
 - d3d12/ID3D12Device3::OpenExistingHeapFromFileMapping
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
 - ID3D12Device3::OpenExistingHeapFromFileMapping
---

## -description

Creates a special-purpose diagnostic heap in system memory from a file mapping object. The created heap can persist even in the event of a GPU-fault or device-removed scenario.

## -parameters

### -param hFileMapping

Type: **[HANDLE](/windows/win32/winprog/windows-data-types)**

The handle to the file mapping object to use to create the heap.

### -param riid

Type: **REFIID**

The globally unique identifier (**GUID**) for the heap interface (<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12heap">ID3D12Heap</a>).

The **REFIID**, or **GUID**, of the interface to the heap can be obtained by using the **__uuidof()** macro. For example, **__uuidof(ID3D12Heap)** will retrieve the **GUID** of the interface to a heap.

### -param ppvHeap [out]

Type: **void\*\***

<a href="/visualstudio/code-quality/annotating-function-parameters-and-return-values?view=vs-2015&preserve-view=true">SAL</a>: <code>_COM_Outptr_</code>

A pointer to a memory block. On success, the D3D12 runtime will write a pointer to the newly-opened heap into the memory block. The type of the pointer depends on the provided **riid** parameter.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

This method returns **E_OUTOFMEMORY** if there is insufficient memory to open the existing heap. See <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a> for other possible return values.

## -remarks

The heap is created in system memory, and it permits CPU access. It wraps the entire VirtualAlloc region.

Heaps can be used for placed and reserved resources, as orthogonally as other heaps. Restrictions may still exist based on the flags that cannot be app-chosen.

## -see-also

[ID3D12Device3 interface](./nn-d3d12-id3d12device3.md)
