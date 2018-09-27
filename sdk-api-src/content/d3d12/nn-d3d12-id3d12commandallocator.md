---
UID: NN:d3d12.ID3D12CommandAllocator
title: ID3D12CommandAllocator
author: windows-sdk-content
description: Represents the allocations of storage for graphics processing unit (GPU) commands.
old-location: direct3d12\id3d12commandallocator.htm
tech.root: direct3d12
ms.assetid: ADC494E6-1698-415D-90C5-F99FCD4C5309
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ID3D12CommandAllocator, ID3D12CommandAllocator interface, ID3D12CommandAllocator interface,described, d3d12/ID3D12CommandAllocator, direct3d12.id3d12commandallocator
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
 - ID3D12CommandAllocator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12CommandAllocator interface


## -description


Represents the allocations of storage for graphics processing unit (GPU) commands.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12CommandAllocator</b> interface inherits from <a href="https://msdn.microsoft.com/89DC88B4-9DFD-413D-8EB9-91087CC90D18">ID3D12Pageable</a>. <b>ID3D12CommandAllocator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12CommandAllocator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B7477767-9110-45DE-962F-E56FDB635D17">Reset</a>
</td>
<td align="left" width="63%">
Indicates to re-use the memory that is associated with the command allocator.

</td>
</tr>
</table> 


## -remarks



Use <a href="https://msdn.microsoft.com/28DA0D59-3DB7-4652-B1EA-3360EA85A659">ID3D12Device::CreateCommandAllocator</a> to create a command allocator object. 

The command allocator object corresponds to the underlying allocations in which GPU commands are stored.  The command allocator object applies to both direct command lists and bundles.  You must use a command allocator object in a DirectX 12 app.


#### Examples

The <a href="https://msdn.microsoft.com/4C4475D4-534F-484F-8D60-9ACEA09AC109">D3D12nBodyGravity</a> sample uses <b>ID3D12CommandAllocator</b> as follows:
        

Header file declarations.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>D3D12_VIEWPORT m_viewport;
D3D12_RECT m_scissorRect;
ComPtr&lt;IDXGISwapChain3&gt; m_swapChain;
ComPtr&lt;ID3D12Device&gt; m_device;
ComPtr&lt;ID3D12Resource&gt; m_renderTargets[FrameCount];
ComPtr&lt;ID3D12CommandAllocator&gt; m_commandAllocator;
ComPtr&lt;ID3D12CommandQueue&gt; m_commandQueue;
ComPtr&lt;ID3D12RootSignature&gt; m_rootSignature;
ComPtr&lt;ID3D12DescriptorHeap&gt; m_rtvHeap;
ComPtr&lt;ID3D12PipelineState&gt; m_pipelineState;
ComPtr&lt;ID3D12GraphicsCommandList&gt; m_commandList;
UINT m_rtvDescriptorSize;
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
 

 

