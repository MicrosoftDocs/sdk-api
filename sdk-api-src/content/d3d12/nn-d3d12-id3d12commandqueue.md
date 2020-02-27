---
UID: NN:d3d12.ID3D12CommandQueue
title: ID3D12CommandQueue (d3d12.h)
description: Provides methods for submitting command lists, synchronizing command list execution, instrumenting the command queue, and updating resource tile mappings.
old-location: direct3d12\id3d12commandqueue.htm
tech.root: direct3d12
ms.assetid: 88A4E8BA-02B9-48A1-8E46-2D2560544539
ms.date: 12/05/2018
ms.keywords: ID3D12CommandQueue, ID3D12CommandQueue interface, ID3D12CommandQueue interface,described, d3d12/ID3D12CommandQueue, direct3d12.id3d12commandqueue
f1_keywords:
- d3d12/ID3D12CommandQueue
dev_langs:
- c++
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
- ID3D12CommandQueue
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12CommandQueue interface


## -description


Provides methods for submitting command lists, synchronizing command list execution, instrumenting the command queue, and updating resource tile mappings.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12CommandQueue</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12pageable">ID3D12Pageable</a>. <b>ID3D12CommandQueue</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12CommandQueue</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-beginevent">BeginEvent</a>
</td>
<td align="left" width="63%">
Not intended to be called directly.  Use the
        <a href="https://devblogs.microsoft.com/pix/winpixeventruntime/">PIX event runtime</a> to insert events into a command queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings">CopyTileMappings</a>
</td>
<td align="left" width="63%">
Copies mappings from a source reserved resource to a destination reserved resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-endevent">EndEvent</a>
</td>
<td align="left" width="63%">
Not intended to be called directly.  Use the
        <a href="https://devblogs.microsoft.com/pix/winpixeventruntime/">PIX event runtime</a> to insert events into a command queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists">ExecuteCommandLists</a>
</td>
<td align="left" width="63%">
Submits an array of command lists for execution.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration">GetClockCalibration</a>
</td>
<td align="left" width="63%">
This method samples the CPU and GPU timestamp counters at the same moment in time. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Gets the description of the command queue.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency">GetTimestampFrequency</a>
</td>
<td align="left" width="63%">
This method is used to determine the rate at which the GPU timestamp counter increments.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-setmarker">SetMarker</a>
</td>
<td align="left" width="63%">
Not intended to be called directly.  Use the
        <a href="https://devblogs.microsoft.com/pix/winpixeventruntime/">PIX event runtime</a> to insert events into a command queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-signal">Signal</a>
</td>
<td align="left" width="63%">
Updates a fence to a specified value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings">UpdateTileMappings</a>
</td>
<td align="left" width="63%">
Updates mappings of tile locations in reserved resources to memory locations in a resource heap.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-wait">Wait</a>
</td>
<td align="left" width="63%">
Waits until the specified fence reaches or exceeds the specified value.

</td>
</tr>
</table> 


## -remarks



Use <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandqueue">ID3D12Device::CreateCommandQueue</a> to create a command queue object. 


#### Examples

The <a href="https://docs.microsoft.com/windows/desktop/direct3d12/working-samples">D3D12nBodyGravity</a> sample uses <b>ID3D12CommandQueue</b> as follows:
        

Header file declarations.


```cpp
// Compute objects.
ComPtr<ID3D12CommandAllocator> m_computeAllocator[ThreadCount];
ComPtr<ID3D12CommandQueue> m_computeCommandQueue[ThreadCount];
ComPtr<ID3D12GraphicsCommandList> m_computeCommandList[ThreadCount];

```


Asynchronous compute thread.


```cpp
DWORD D3D12nBodyGravity::AsyncComputeThreadProc(int threadIndex)
{
    ID3D12CommandQueue* pCommandQueue = m_computeCommandQueue[threadIndex].Get();
    ID3D12CommandAllocator* pCommandAllocator = m_computeAllocator[threadIndex].Get();
    ID3D12GraphicsCommandList* pCommandList = m_computeCommandList[threadIndex].Get();
    ID3D12Fence* pFence = m_threadFences[threadIndex].Get();

    while (0 == InterlockedGetValue(&m_terminating))
    {
        // Run the particle simulation.
        Simulate(threadIndex);

        // Close and execute the command list.
        ThrowIfFailed(pCommandList->Close());
        ID3D12CommandList* ppCommandLists[] = { pCommandList };

        pCommandQueue->ExecuteCommandLists(1, ppCommandLists);

        // Wait for the compute shader to complete the simulation.
        UINT64 threadFenceValue = InterlockedIncrement(&m_threadFenceValues[threadIndex]);
        ThrowIfFailed(pCommandQueue->Signal(pFence, threadFenceValue));
        ThrowIfFailed(pFence->SetEventOnCompletion(threadFenceValue, m_threadFenceEvents[threadIndex]));
        WaitForSingleObject(m_threadFenceEvents[threadIndex], INFINITE);

        // Wait for the render thread to be done with the SRV so that
        // the next frame in the simulation can run.
        UINT64 renderContextFenceValue = InterlockedGetValue(&m_renderContextFenceValues[threadIndex]);
        if (m_renderContextFence->GetCompletedValue() < renderContextFenceValue)
        {
            ThrowIfFailed(pCommandQueue->Wait(m_renderContextFence.Get(), renderContextFenceValue));
            InterlockedExchange(&m_renderContextFenceValues[threadIndex], 0);
        }

        // Swap the indices to the SRV and UAV.
        m_srvIndex[threadIndex] = 1 - m_srvIndex[threadIndex];

        // Prepare for the next frame.
        ThrowIfFailed(pCommandAllocator->Reset());
        ThrowIfFailed(pCommandList->Reset(pCommandAllocator, m_computeState.Get()));
    }

    return 0;
}

```


Refer to the <a href="https://docs.microsoft.com/windows/desktop/direct3d12/notes-on-example-code">Example Code in the D3D12 Reference</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-interfaces">Core Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12pageable">ID3D12Pageable</a>
 

 

