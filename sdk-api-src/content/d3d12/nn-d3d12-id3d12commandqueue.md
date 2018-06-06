---
UID: NN:d3d12.ID3D12CommandQueue
title: ID3D12CommandQueue
author: windows-sdk-content
description: Provides methods for submitting command lists, synchronizing command list execution, instrumenting the command queue, and updating resource tile mappings.
old-location: direct3d12\id3d12commandqueue.htm
old-project: direct3d12
ms.assetid: 88A4E8BA-02B9-48A1-8E46-2D2560544539
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: ID3D12CommandQueue, ID3D12CommandQueue interface, ID3D12CommandQueue interface,described, d3d12/ID3D12CommandQueue, direct3d12.id3d12commandqueue
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: D3D_SHADER_MODEL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12CommandQueue
product: Windows
targetos: Windows
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
---

# ID3D12CommandQueue interface


## -description


Provides methods for submitting command lists, synchronizing command list execution, instrumenting the command queue, and updating resource tile mappings.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12CommandQueue</b> interface inherits from <a href="https://msdn.microsoft.com/89DC88B4-9DFD-413D-8EB9-91087CC90D18">ID3D12Pageable</a>. <b>ID3D12CommandQueue</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/09586D24-6D52-49BA-B6C0-793219FAE80C">BeginEvent</a>
</td>
<td align="left" width="63%">

          Not intended to be called directly.  Use the
        <a href="https://blogs.msdn.microsoft.com/pix/winpixeventruntime/">PIX event runtime</a> to insert events into a command queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FAFA4B5C-EA3C-4209-AB8E-75F3B90F3745">CopyTileMappings</a>
</td>
<td align="left" width="63%">
Copies mappings from a source reserved resource to a destination reserved resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CA45061A-3DD6-4FFB-9723-ED33343052F3">EndEvent</a>
</td>
<td align="left" width="63%">

          Not intended to be called directly.  Use the
        <a href="https://blogs.msdn.microsoft.com/pix/winpixeventruntime/">PIX event runtime</a> to insert events into a command queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/653C15CD-0996-4B3B-A5F6-3E85CD0516AD">ExecuteCommandLists</a>
</td>
<td align="left" width="63%">
Submits an array of command lists for execution.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B8E0F8D4-D291-41B5-8E40-0C1FB3DCC253">GetClockCalibration</a>
</td>
<td align="left" width="63%">
This method samples the CPU and GPU timestamp counters at the same moment in time. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AEEE6B15-AEB0-47C5-A3F8-9957516BFBEE">GetDesc</a>
</td>
<td align="left" width="63%">

          Gets the description of the command queue.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90D79775-2898-453E-87FB-CD6850829E47">GetTimestampFrequency</a>
</td>
<td align="left" width="63%">
This method is used to determine the rate at which the GPU timestamp counter increments.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/993996E9-40B8-4FC6-B1CF-883829F8D1F5">SetMarker</a>
</td>
<td align="left" width="63%">

          Not intended to be called directly.  Use the
        <a href="https://blogs.msdn.microsoft.com/pix/winpixeventruntime/">PIX event runtime</a> to insert events into a command queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/487E2DED-C741-4376-9EE2-3DDD2F4F76BB">Signal</a>
</td>
<td align="left" width="63%">
Updates a fence to a specified value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8A8017E5-AB55-4660-855B-D6F93F69CB52">UpdateTileMappings</a>
</td>
<td align="left" width="63%">

          Updates mappings of tile locations in reserved resources to memory locations in a resource heap.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75D494D0-BCEC-453E-AB4F-E57CE2C9B318">Wait</a>
</td>
<td align="left" width="63%">
Waits until the specified fence reaches or exceeds the specified value.

</td>
</tr>
</table> 


## -remarks



Use <a href="https://msdn.microsoft.com/556D068C-9939-4B42-AFC2-4EBB2D7B553B">ID3D12Device::CreateCommandQueue</a> to create a command queue object. 


#### Examples


          The <a href="https://msdn.microsoft.com/4C4475D4-534F-484F-8D60-9ACEA09AC109">D3D12nBodyGravity</a> sample uses <b>ID3D12CommandQueue</b> as follows:
        

Header file declarations.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Compute objects.
ComPtr&lt;ID3D12CommandAllocator&gt; m_computeAllocator[ThreadCount];
ComPtr&lt;ID3D12CommandQueue&gt; m_computeCommandQueue[ThreadCount];
ComPtr&lt;ID3D12GraphicsCommandList&gt; m_computeCommandList[ThreadCount];
</pre>
</td>
</tr>
</table></span></div>
Asynchronous compute thread.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>DWORD D3D12nBodyGravity::AsyncComputeThreadProc(int threadIndex)
{
    ID3D12CommandQueue* pCommandQueue = m_computeCommandQueue[threadIndex].Get();
    ID3D12CommandAllocator* pCommandAllocator = m_computeAllocator[threadIndex].Get();
    ID3D12GraphicsCommandList* pCommandList = m_computeCommandList[threadIndex].Get();
    ID3D12Fence* pFence = m_threadFences[threadIndex].Get();

    while (0 == InterlockedGetValue(&amp;m_terminating))
    {
        // Run the particle simulation.
        Simulate(threadIndex);

        // Close and execute the command list.
        ThrowIfFailed(pCommandList-&gt;Close());
        ID3D12CommandList* ppCommandLists[] = { pCommandList };

        pCommandQueue-&gt;ExecuteCommandLists(1, ppCommandLists);

        // Wait for the compute shader to complete the simulation.
        UINT64 threadFenceValue = InterlockedIncrement(&amp;m_threadFenceValues[threadIndex]);
        ThrowIfFailed(pCommandQueue-&gt;Signal(pFence, threadFenceValue));
        ThrowIfFailed(pFence-&gt;SetEventOnCompletion(threadFenceValue, m_threadFenceEvents[threadIndex]));
        WaitForSingleObject(m_threadFenceEvents[threadIndex], INFINITE);

        // Wait for the render thread to be done with the SRV so that
        // the next frame in the simulation can run.
        UINT64 renderContextFenceValue = InterlockedGetValue(&amp;m_renderContextFenceValues[threadIndex]);
        if (m_renderContextFence-&gt;GetCompletedValue() &lt; renderContextFenceValue)
        {
            ThrowIfFailed(pCommandQueue-&gt;Wait(m_renderContextFence.Get(), renderContextFenceValue));
            InterlockedExchange(&amp;m_renderContextFenceValues[threadIndex], 0);
        }

        // Swap the indices to the SRV and UAV.
        m_srvIndex[threadIndex] = 1 - m_srvIndex[threadIndex];

        // Prepare for the next frame.
        ThrowIfFailed(pCommandAllocator-&gt;Reset());
        ThrowIfFailed(pCommandList-&gt;Reset(pCommandAllocator, m_computeState.Get()));
    }

    return 0;
}
</pre>
</td>
</tr>
</table></span></div>
Refer to the <a href="https://msdn.microsoft.com/C2323482-D06D-43B7-9BDE-BFB9A6A6B70D">Example Code in the D3D12 Reference</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/A9BD5910-8FF2-4540-BB8E-E8EA5C10528C">Core Interfaces</a>



<a href="https://msdn.microsoft.com/89DC88B4-9DFD-413D-8EB9-91087CC90D18">ID3D12Pageable</a>
 

 

