---
UID: NF:d3d12.ID3D12CommandQueue.Signal
title: ID3D12CommandQueue::Signal
author: windows-sdk-content
description: Updates a fence to a specified value.
old-location: direct3d12\id3d12commandqueue_signal.htm
tech.root: direct3d12
ms.assetid: 487E2DED-C741-4376-9EE2-3DDD2F4F76BB
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: ID3D12CommandQueue interface,Signal method, ID3D12CommandQueue.Signal, ID3D12CommandQueue::Signal, Signal, Signal method, Signal method,ID3D12CommandQueue interface, d3d12/ID3D12CommandQueue::Signal, direct3d12.id3d12commandqueue_signal
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12CommandQueue.Signal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12CommandQueue::Signal


## -description


Updates a fence to a specified value.


## -parameters




### -param pFence

Type: <b><a href="https://msdn.microsoft.com/2B388352-EF43-4D1E-851C-A670B4681F0F">ID3D12Fence</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/2B388352-EF43-4D1E-851C-A670B4681F0F">ID3D12Fence</a> object.
          


### -param Value

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a></b>

The value to set the fence to.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.
          




## -remarks



Use this method to set a fence value from the GPU side. Use <a href="https://msdn.microsoft.com/8AC955C1-37C9-47F3-B35C-980783C58390">ID3D12Fence::Signal</a> to set a fence from the CPU side.


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


Refer to the <a href="https://msdn.microsoft.com/C2323482-D06D-43B7-9BDE-BFB9A6A6B70D">Example Code in the D3D12 Reference</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/88A4E8BA-02B9-48A1-8E46-2D2560544539">ID3D12CommandQueue</a>



<a href="https://msdn.microsoft.com/93903F50-A6CA-41C2-863D-68D645586B4C">Synchronization and Multi-Engine</a>
 

 

