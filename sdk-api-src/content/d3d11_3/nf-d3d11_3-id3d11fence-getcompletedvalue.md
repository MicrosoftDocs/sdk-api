---
UID: NF:d3d11_3.ID3D11Fence.GetCompletedValue
title: ID3D11Fence::GetCompletedValue (d3d11_3.h)
description: Gets the current value of the fence. (ID3D11Fence.GetCompletedValue)
helpviewer_keywords: ["GetCompletedValue","GetCompletedValue method [Direct3D 11]","GetCompletedValue method [Direct3D 11]","ID3D11Fence interface","ID3D11Fence interface [Direct3D 11]","GetCompletedValue method","ID3D11Fence.GetCompletedValue","ID3D11Fence::GetCompletedValue","d3d11_3/ID3D11Fence::GetCompletedValue","direct3d11.id3d11fence_getcompletedvalue"]
old-location: direct3d11\id3d11fence_getcompletedvalue.htm
tech.root: direct3d11
ms.assetid: 57D5BDEE-1E14-4187-9F32-CF3609F4BBBB
ms.date: 12/05/2018
ms.keywords: GetCompletedValue, GetCompletedValue method [Direct3D 11], GetCompletedValue method [Direct3D 11],ID3D11Fence interface, ID3D11Fence interface [Direct3D 11],GetCompletedValue method, ID3D11Fence.GetCompletedValue, ID3D11Fence::GetCompletedValue, d3d11_3/ID3D11Fence::GetCompletedValue, direct3d11.id3d11fence_getcompletedvalue
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
 - ID3D11Fence::GetCompletedValue
 - d3d11_3/ID3D11Fence::GetCompletedValue
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
 - ID3D11Fence.GetCompletedValue
---

# ID3D11Fence::GetCompletedValue


## -description

Gets the current value of the fence.

This member function is equivalent to the Direct3D 12 <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue">ID3D12Fence::GetCompletedValue</a> member function, and applies between Direct3D 11 and Direct3D 12 in interop scenarios.



## -returns

Type: <b><a href="/windows/win32/WinProg/windows-data-types">UINT64</a></b>

Returns the current value of the fence.

## -see-also

<a href="/windows/win32/api/d3d11_3/nn-d3d11_3-id3d11fence">ID3D11Fence</a>



<a href="/windows/win32/direct3d12/user-mode-heap-synchronization">Multi-engine synchronization</a>

