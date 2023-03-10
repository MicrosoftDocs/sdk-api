---
UID: NF:d3d11_3.ID3D11DeviceContext4.Wait
title: ID3D11DeviceContext4::Wait (d3d11_3.h)
description: Waits until the specified fence reaches or exceeds the specified value before future work can begin.
helpviewer_keywords: ["ID3D11DeviceContext4 interface [Direct3D 11]","Wait method","ID3D11DeviceContext4.Wait","ID3D11DeviceContext4::Wait","Wait","Wait method [Direct3D 11]","Wait method [Direct3D 11]","ID3D11DeviceContext4 interface","d3d11_3/ID3D11DeviceContext4::Wait","direct3d11.id3d11devicecontext4_wait"]
old-location: direct3d11\id3d11devicecontext4_wait.htm
tech.root: direct3d11
ms.assetid: 91576E2D-A28F-43A8-B9FE-5888779877F9
ms.date: 12/05/2018
ms.keywords: ID3D11DeviceContext4 interface [Direct3D 11],Wait method, ID3D11DeviceContext4.Wait, ID3D11DeviceContext4::Wait, Wait, Wait method [Direct3D 11], Wait method [Direct3D 11],ID3D11DeviceContext4 interface, d3d11_3/ID3D11DeviceContext4::Wait, direct3d11.id3d11devicecontext4_wait
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
 - ID3D11DeviceContext4::Wait
 - d3d11_3/ID3D11DeviceContext4::Wait
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
 - ID3D11DeviceContext4.Wait
---

# ID3D11DeviceContext4::Wait


## -description

Waits until the specified fence reaches or exceeds the specified value before future work can begin.

This member function is equivalent to the Direct3D 12 <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait">ID3D12CommandQueue::Wait</a> member function, and applies between Direct3D 11 and Direct3D 12 in interop scenarios.
<div class="alert"><b>Note</b>  This method only applies to immediate-mode contexts.</div><div> </div>

## -parameters

### -param pFence

Type: <b><a href="/windows/win32/api/d3d11_3/nn-d3d11_3-id3d11fence">ID3D11Fence</a>*</b>

A pointer to the <a href="/windows/win32/api/d3d11_3/nn-d3d11_3-id3d11fence">ID3D11Fence</a> object.

### -param Value

Type: <b><a href="/windows/win32/WinProg/windows-data-types">UINT64</a></b>

The value that the device context is waiting for the fence to reach or exceed.  So when  <a href="/windows/win32/api/d3d11_3/nf-d3d11_3-id3d11fence-getcompletedvalue">ID3D11Fence::GetCompletedValue</a> is greater than or equal to <i>Value</i>, the wait is terminated.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/win32/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -see-also

<a href="/windows/win32/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4">ID3D11DeviceContext4</a>



<a href="/windows/win32/direct3d12/user-mode-heap-synchronization">Multi-engine synchronization</a>

