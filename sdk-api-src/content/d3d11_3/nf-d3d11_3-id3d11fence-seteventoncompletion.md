---
UID: NF:d3d11_3.ID3D11Fence.SetEventOnCompletion
title: ID3D11Fence::SetEventOnCompletion (d3d11_3.h)
description: Specifies an event that should be fired when the fence reaches a certain value. (ID3D11Fence.SetEventOnCompletion)
helpviewer_keywords: ["ID3D11Fence interface [Direct3D 11]","SetEventOnCompletion method","ID3D11Fence.SetEventOnCompletion","ID3D11Fence::SetEventOnCompletion","SetEventOnCompletion","SetEventOnCompletion method [Direct3D 11]","SetEventOnCompletion method [Direct3D 11]","ID3D11Fence interface","d3d11_3/ID3D11Fence::SetEventOnCompletion","direct3d11.id3d11fence_seteventoncompletion"]
old-location: direct3d11\id3d11fence_seteventoncompletion.htm
tech.root: direct3d11
ms.assetid: 255FF723-85FA-4230-B751-B5F52A6F8EBB
ms.date: 12/05/2018
ms.keywords: ID3D11Fence interface [Direct3D 11],SetEventOnCompletion method, ID3D11Fence.SetEventOnCompletion, ID3D11Fence::SetEventOnCompletion, SetEventOnCompletion, SetEventOnCompletion method [Direct3D 11], SetEventOnCompletion method [Direct3D 11],ID3D11Fence interface, d3d11_3/ID3D11Fence::SetEventOnCompletion, direct3d11.id3d11fence_seteventoncompletion
req.header: d3d11_3.h
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
req.lib: D3D11.lib
req.dll: D3D11.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11Fence::SetEventOnCompletion
 - d3d11_3/ID3D11Fence::SetEventOnCompletion
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.dll
api_name:
 - ID3D11Fence.SetEventOnCompletion
---

# ID3D11Fence::SetEventOnCompletion


## -description

Specifies an event that should be fired when the fence reaches a certain value.

This member function is equivalent to the Direct3D 12 <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion">ID3D12Fence::SetEventOnCompletion</a> member function, and applies between Direct3D 11 and Direct3D 12 in interop scenarios.

## -parameters

### -param Value

Type: <b><a href="/windows/win32/WinProg/windows-data-types">UINT64</a></b>

The fence value when the event is to be signaled.

### -param hEvent

Type: <b><a href="/windows/win32/WinProg/windows-data-types">HANDLE</a></b>

A handle to the event object.

## -returns

Type: <b>HRESULT</b>

This method returns <b>E_OUTOFMEMORY</b> if the kernel components don’t have sufficient memory to store the event in a list. See <a href="/windows/win32/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a> for other possible return values.

## -see-also

<a href="/windows/win32/api/d3d11_3/nn-d3d11_3-id3d11fence">ID3D11Fence</a>



<a href="/windows/win32/direct3d12/user-mode-heap-synchronization">Multi-engine synchronization</a>

