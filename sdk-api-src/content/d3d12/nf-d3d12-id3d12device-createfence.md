---
UID: NF:d3d12.ID3D12Device.CreateFence
title: ID3D12Device::CreateFence (d3d12.h)
description: Creates a fence object. (ID3D12Device.CreateFence)
helpviewer_keywords: ["CreateFence","CreateFence method","CreateFence method","ID3D12Device interface","ID3D12Device interface","CreateFence method","ID3D12Device.CreateFence","ID3D12Device::CreateFence","d3d12/ID3D12Device::CreateFence","direct3d12.id3d12device_createfence"]
old-location: direct3d12\id3d12device_createfence.htm
tech.root: direct3d12
ms.assetid: 731A60CA-644A-4FC2-8461-DDD686363BED
ms.date: 12/05/2018
ms.keywords: CreateFence, CreateFence method, CreateFence method,ID3D12Device interface, ID3D12Device interface,CreateFence method, ID3D12Device.CreateFence, ID3D12Device::CreateFence, d3d12/ID3D12Device::CreateFence, direct3d12.id3d12device_createfence
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
 - ID3D12Device::CreateFence
 - d3d12/ID3D12Device::CreateFence
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
 - ID3D12Device.CreateFence
---

# ID3D12Device::CreateFence


## -description

Creates a fence object.

## -parameters

### -param InitialValue

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a></b>

The initial value for the fence.

### -param Flags

Type: <b><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_fence_flags">D3D12_FENCE_FLAGS</a></b>

A combination of <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_fence_flags">D3D12_FENCE_FLAGS</a>-typed values that are combined by using a bitwise OR operation. 
            The resulting value specifies options for the fence.

### -param riid

Type: <b>REFIID</b>

The globally unique identifier (<b>GUID</b>) for the fence interface (<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12fence">ID3D12Fence</a>).
            The <b>REFIID</b>, or <b>GUID</b>, of the interface to the fence can be obtained by using the __uuidof() macro.
            For example, __uuidof(ID3D12Fence) will get the <b>GUID</b> of the interface to a fence.

### -param ppFence [out]

Type: <b>void**</b>

A pointer to a memory block that receives a pointer to the <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12fence">ID3D12Fence</a> interface that is used to access the fence.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns <b>S_OK</b> if successful; otherwise, returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>
