---
UID: NF:d3d11_3.ID3D11DeviceContext4.Signal
title: ID3D11DeviceContext4::Signal (d3d11_3.h)
description: Updates a fence to a specified value after all previous work has completed.
helpviewer_keywords: ["ID3D11DeviceContext4 interface [Direct3D 11]","Signal method","ID3D11DeviceContext4.Signal","ID3D11DeviceContext4::Signal","Signal","Signal method [Direct3D 11]","Signal method [Direct3D 11]","ID3D11DeviceContext4 interface","d3d11_3/ID3D11DeviceContext4::Signal","direct3d11.id3d11devicecontext4_signal"]
old-location: direct3d11\id3d11devicecontext4_signal.htm
tech.root: direct3d11
ms.assetid: 5B308187-27B1-40B8-B9B7-CD8A8223A0EE
ms.date: 12/05/2018
ms.keywords: ID3D11DeviceContext4 interface [Direct3D 11],Signal method, ID3D11DeviceContext4.Signal, ID3D11DeviceContext4::Signal, Signal, Signal method [Direct3D 11], Signal method [Direct3D 11],ID3D11DeviceContext4 interface, d3d11_3/ID3D11DeviceContext4::Signal, direct3d11.id3d11devicecontext4_signal
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11DeviceContext4::Signal
 - d3d11_3/ID3D11DeviceContext4::Signal
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext4.Signal
---

# ID3D11DeviceContext4::Signal


## -description

Updates a fence to a specified value after all previous work has completed.

This member function is equivalent to the Direct3D 12 <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal">ID3D12CommandQueue::Signal</a> member function, and applies between Direct3D 11 and Direct3D 12 in interop scenarios.
<div class="alert"><b>Note</b>  This method only applies to immediate-mode contexts.</div><div> </div>

## -parameters

### -param pFence

Type: <b><a href="/windows/win32/api/d3d11_3/nn-d3d11_3-id3d11fence">ID3D11Fence</a>*</b>

A pointer to the <a href="/windows/win32/api/d3d11_3/nn-d3d11_3-id3d11fence">ID3D11Fence</a> object.

### -param Value

Type: <b><a href="/windows/win32/WinProg/windows-data-types">UINT64</a></b>

The value to set the fence to.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/win32/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -see-also

<a href="/windows/win32/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4">ID3D11DeviceContext4</a>



<a href="/windows/win32/direct3d12/user-mode-heap-synchronization">Multi-engine synchronization</a>

