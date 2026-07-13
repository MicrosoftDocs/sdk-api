---
UID: NF:d3d12.ID3D12CommandQueue.Wait
title: ID3D12CommandQueue::Wait (d3d12.h)
description: Queues a GPU-side wait, and returns immediately. A GPU-side wait is where the GPU waits until the specified fence reaches or exceeds the specified value.
helpviewer_keywords: ["ID3D12CommandQueue interface","Wait method","ID3D12CommandQueue.Wait","ID3D12CommandQueue::Wait","Wait","Wait method","Wait method","ID3D12CommandQueue interface","d3d12/ID3D12CommandQueue::Wait","direct3d12.id3d12commandqueue_wait"]
old-location: direct3d12\id3d12commandqueue_wait.htm
tech.root: direct3d12
ms.assetid: 75D494D0-BCEC-453E-AB4F-E57CE2C9B318
ms.date: 12/05/2018
ms.keywords: ID3D12CommandQueue interface,Wait method, ID3D12CommandQueue.Wait, ID3D12CommandQueue::Wait, Wait, Wait method, Wait method,ID3D12CommandQueue interface, d3d12/ID3D12CommandQueue::Wait, direct3d12.id3d12commandqueue_wait
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
 - ID3D12CommandQueue::Wait
 - d3d12/ID3D12CommandQueue::Wait
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
 - ID3D12CommandQueue.Wait
---

## -description

Queues a GPU-side wait, and returns immediately. A GPU-side wait is where the GPU waits until the specified fence reaches or exceeds the specified value.

## -parameters

### -param pFence

Type: <b><a href="/windows/win32/api/d3d12/nn-d3d12-id3d12fence">ID3D12Fence</a>*</b>

A pointer to the <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12fence">ID3D12Fence</a> object.

### -param Value

Type: <b><a href="/windows/win32/WinProg/windows-data-types">UINT64</a></b>

The value that the command queue is waiting for the fence to reach or exceed.  So when  <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue">ID3D12Fence::GetCompletedValue</a> is greater than or equal to <i>Value</i>, the wait is terminated.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/win32/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -remarks

Because a wait is being queued, the API returns immediately. It's the command queue that waits (during which time no work is executed) until the fence specified reaches the requested value.
	
If you want to perform a CPU-side wait (where the calling thread blocks until a fence reaches a particular value), then you should use the [**ID3D12Fence::SetEventOnCompletion**](./nf-d3d12-id3d12fence-seteventoncompletion.md) API in conjunction with [**WaitForSingleObject**](../synchapi/nf-synchapi-waitforsingleobject.md) (or a similar API).

## -see-also

<a href="/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue">ID3D12CommandQueue</a>



<a href="/windows/win32/direct3d12/user-mode-heap-synchronization">Multi-engine synchronization</a>