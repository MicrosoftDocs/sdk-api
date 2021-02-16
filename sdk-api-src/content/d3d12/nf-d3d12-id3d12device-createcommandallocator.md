---
UID: NF:d3d12.ID3D12Device.CreateCommandAllocator
title: ID3D12Device::CreateCommandAllocator (d3d12.h)
description: Creates a command allocator object.
helpviewer_keywords: ["CreateCommandAllocator","CreateCommandAllocator method","CreateCommandAllocator method","ID3D12Device interface","ID3D12Device interface","CreateCommandAllocator method","ID3D12Device.CreateCommandAllocator","ID3D12Device::CreateCommandAllocator","d3d12/ID3D12Device::CreateCommandAllocator","direct3d12.id3d12device_createcommandallocator"]
old-location: direct3d12\id3d12device_createcommandallocator.htm
tech.root: direct3d12
ms.assetid: 28DA0D59-3DB7-4652-B1EA-3360EA85A659
ms.date: 12/05/2018
ms.keywords: CreateCommandAllocator, CreateCommandAllocator method, CreateCommandAllocator method,ID3D12Device interface, ID3D12Device interface,CreateCommandAllocator method, ID3D12Device.CreateCommandAllocator, ID3D12Device::CreateCommandAllocator, d3d12/ID3D12Device::CreateCommandAllocator, direct3d12.id3d12device_createcommandallocator
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
 - ID3D12Device::CreateCommandAllocator
 - d3d12/ID3D12Device::CreateCommandAllocator
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
 - ID3D12Device.CreateCommandAllocator
---

# ID3D12Device::CreateCommandAllocator


## -description

Creates a command allocator object.

## -parameters

### -param type [in]

Type: <b><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type">D3D12_COMMAND_LIST_TYPE</a></b>

A <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type">D3D12_COMMAND_LIST_TYPE</a>-typed value that specifies the type of command allocator to create.
            The type of command allocator can be the type that records either direct command lists or bundles.

### -param riid

Type: <b>REFIID</b>

The globally unique identifier (<b>GUID</b>) for the command allocator interface (<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12commandallocator">ID3D12CommandAllocator</a>).
            The <b>REFIID</b>, or <b>GUID</b>, of the interface to the command allocator can be obtained by using the __uuidof() macro.
            For example, __uuidof(ID3D12CommandAllocator) will get the <b>GUID</b> of the interface to a command allocator.

### -param ppCommandAllocator [out]

Type: <b>void**</b>

A pointer to a memory block that receives a pointer to the <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12commandallocator">ID3D12CommandAllocator</a> interface for the command allocator.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns <b>E_OUTOFMEMORY</b> if there is insufficient memory to create the command allocator.
              See <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a> for other possible return values.

## -remarks

The device creates command lists from the command allocator.
      


#### Examples

The <a href="/windows/desktop/direct3d12/working-samples">D3D12Bundles</a> sample uses <b>ID3D12Device::CreateCommandAllocator</b> as follows:
        


```cpp
ThrowIfFailed(pDevice->CreateCommandAllocator(D3D12_COMMAND_LIST_TYPE_DIRECT, IID_PPV_ARGS(&m_commandAllocator)));
ThrowIfFailed(pDevice->CreateCommandAllocator(D3D12_COMMAND_LIST_TYPE_BUNDLE, IID_PPV_ARGS(&m_bundleAllocator)));

```


Refer to the <a href="/windows/desktop/direct3d12/notes-on-example-code">Example Code in the D3D12 Reference</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>