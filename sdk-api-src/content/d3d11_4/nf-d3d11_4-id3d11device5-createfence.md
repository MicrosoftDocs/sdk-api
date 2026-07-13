---
UID: NF:d3d11_4.ID3D11Device5.CreateFence
title: ID3D11Device5::CreateFence (d3d11_4.h)
description: Creates a fence object. (ID3D11Device5.CreateFence)
helpviewer_keywords: ["CreateFence","CreateFence method [Direct3D 11]","CreateFence method [Direct3D 11]","ID3D11Device5 interface","ID3D11Device5 interface [Direct3D 11]","CreateFence method","ID3D11Device5.CreateFence","ID3D11Device5::CreateFence","d3d11_4/ID3D11Device5::CreateFence","direct3d11.id3d11device5_createfence"]
old-location: direct3d11\id3d11device5_createfence.htm
tech.root: direct3d11
ms.assetid: B4AA9E0D-AAF4-4632-A98F-A3212764D5E1
ms.date: 12/05/2018
ms.keywords: CreateFence, CreateFence method [Direct3D 11], CreateFence method [Direct3D 11],ID3D11Device5 interface, ID3D11Device5 interface [Direct3D 11],CreateFence method, ID3D11Device5.CreateFence, ID3D11Device5::CreateFence, d3d11_4/ID3D11Device5::CreateFence, direct3d11.id3d11device5_createfence
req.header: d3d11_4.h
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
req.lib: D3d11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11Device5::CreateFence
 - d3d11_4/ID3D11Device5::CreateFence
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.lib
 - d3d11.dll
api_name:
 - ID3D11Device5.CreateFence
---

# ID3D11Device5::CreateFence


## -description

Creates a fence object.

This member function is equivalent to the Direct3D 12 <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createfence">ID3D12Device::CreateFence</a> member function, and applies between Direct3D 11 and Direct3D 12 in interop scenarios.

## -parameters

### -param InitialValue

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a></b>

The initial value for the fence.

### -param Flags

Type: <b><a href="/windows/desktop/api/d3d11_3/ne-d3d11_3-d3d11_fence_flag">D3D11_FENCE_FLAG</a></b>

A combination of <a href="/windows/desktop/api/d3d11_3/ne-d3d11_3-d3d11_fence_flag">D3D11_FENCE_FLAG</a>-typed values that are combined by using a bitwise OR operation. 
            The resulting value specifies options for the fence.

### -param ReturnedInterface

Type: <b>REFIID</b>

The globally unique identifier (<b>GUID</b>) for the fence interface (<a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11fence">ID3D11Fence</a>).
            The <b>REFIID</b>, or <b>GUID</b>, of the interface to the fence can be obtained by using the __uuidof() macro.
            For example, __uuidof(ID3D11Fence) will get the <b>GUID</b> of the interface to a fence.

### -param ppFence [out]

Type: <b>void**</b>

A pointer to a memory block that receives a pointer to the <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11fence">ID3D11Fence</a> interface that is used to access the fence.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns <b>S_OK</b> if successful; otherwise, returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5">ID3D11Device5</a>



<a href="/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-unregisterdeviceremoved">UnregisterDeviceRemoved</a>
