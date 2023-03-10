---
UID: NF:d3d12.ID3D12CommandQueue.Signal
title: ID3D12CommandQueue::Signal (d3d12.h)
description: Updates a fence to a specified value.
helpviewer_keywords: ["ID3D12CommandQueue interface","Signal method","ID3D12CommandQueue.Signal","ID3D12CommandQueue::Signal","Signal","Signal method","Signal method","ID3D12CommandQueue interface","d3d12/ID3D12CommandQueue::Signal","direct3d12.id3d12commandqueue_signal"]
old-location: direct3d12\id3d12commandqueue_signal.htm
tech.root: direct3d12
ms.assetid: 487E2DED-C741-4376-9EE2-3DDD2F4F76BB
ms.date: 12/05/2018
ms.keywords: ID3D12CommandQueue interface,Signal method, ID3D12CommandQueue.Signal, ID3D12CommandQueue::Signal, Signal, Signal method, Signal method,ID3D12CommandQueue interface, d3d12/ID3D12CommandQueue::Signal, direct3d12.id3d12commandqueue_signal
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
 - ID3D12CommandQueue::Signal
 - d3d12/ID3D12CommandQueue::Signal
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
 - ID3D12CommandQueue.Signal
---

# ID3D12CommandQueue::Signal


## -description

Updates a fence to a specified value.

## -parameters

### -param pFence

Type: <b><a href="/windows/win32/api/d3d12/nn-d3d12-id3d12fence">ID3D12Fence</a>*</b>

A pointer to the <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12fence">ID3D12Fence</a> object.

### -param Value

Type: <b><a href="/windows/win32/WinProg/windows-data-types">UINT64</a></b>

The value to set the fence to.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/win32/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -remarks

Use this method to set a fence value from the GPU side. Use <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal">ID3D12Fence::Signal</a> to set a fence from the CPU side.


#### Examples

Adds a signal to the command queue, then waits for the compute shader to complete the simulation, finally signal and increment the fence value.


```cpp
// Wait for the compute shader to complete the simulation.
UINT64 threadFenceValue = InterlockedIncrement(&m_threadFenceValues[threadIndex]);
ThrowIfFailed(pCommandQueue->Signal(pFence, threadFenceValue));
ThrowIfFailed(pFence->SetEventOnCompletion(threadFenceValue, m_threadFenceEvents[threadIndex]));
WaitForSingleObject(m_threadFenceEvents[threadIndex], INFINITE);

```

```cpp
// Add a signal command to the queue.
ThrowIfFailed(m_commandQueue->Signal(m_renderContextFence.Get(), m_renderContextFenceValue));

```

```cpp
// Signal and increment the fence value.
ThrowIfFailed(m_commandQueue->Signal(m_renderContextFence.Get(), m_renderContextFenceValue));
m_renderContextFenceValue++;

```


Refer to the <a href="/windows/win32/direct3d12/notes-on-example-code">Example Code in the D3D12 Reference</a>.

<div class="code"></div>

## -see-also

<a href="/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue">ID3D12CommandQueue</a>



<a href="/windows/win32/direct3d12/user-mode-heap-synchronization">Multi-engine synchronization</a>

