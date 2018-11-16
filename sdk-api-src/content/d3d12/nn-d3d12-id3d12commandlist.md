---
UID: NN:d3d12.ID3D12CommandList
title: ID3D12CommandList
author: windows-sdk-content
description: An interface from which ID3D12GraphicsCommandList inherits from. It represents an ordered set of commands that the GPU executes, while allowing for extension to support other command lists than just those for graphics (such as compute and copy).
old-location: direct3d12\id3d12commandlist.htm
tech.root: direct3d12
ms.assetid: 1E0359CC-0F53-4C82-9F1A-092F6F72EE20
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ID3D12CommandList, ID3D12CommandList interface, ID3D12CommandList interface,described, d3d12/ID3D12CommandList, direct3d12.id3d12commandlist
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ID3D12CommandList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12CommandList interface


## -description


An interface from which <a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a> inherits from. It represents an ordered set of commands that the GPU executes, while allowing for extension to support other command lists than just those for graphics (such as compute and copy).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12CommandList</b> interface inherits from <a href="https://msdn.microsoft.com/AED60281-A6E4-4AAD-A106-6CA6E9BAEB9A">ID3D12DeviceChild</a>. <b>ID3D12CommandList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12CommandList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39F9EF96-9761-410A-B5DD-A088F6863923">GetType</a>
</td>
<td align="left" width="63%">
Gets the type of the command list, such as direct, bundle, compute, or copy.
        

</td>
</tr>
</table> 


## -remarks



Use <a href="https://msdn.microsoft.com/4C615D7D-6DBC-4EDA-8D72-271EC53047BF">ID3D12Device::CreateCommandList</a> to create a command list object.
      

See also <a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a>, which derives from ID3D12CommandList.
      

A command list corresponds to a set of commands that the graphics processing unit (GPU) executes.  Commands set state, draw, clear, copy, and so on.  

Direct3D 12 command lists only support these 2 levels of indirection:
          

<ul>
<li>A direct command list corresponds to a command buffer that the GPU can execute.
          </li>
<li>A bundle can be executed only directly via a direct command list.
          </li>
</ul>

#### Examples

The <a href="https://msdn.microsoft.com/4C4475D4-534F-484F-8D60-9ACEA09AC109">D3D12nBodyGravity</a> sample uses <b>ID3D12CommandList</b> as follows:
        


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


Refer to the <a href="https://msdn.microsoft.com/C2323482-D06D-43B7-9BDE-BFB9A6A6B70D">Example Code in the D3D12 Reference</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/A9BD5910-8FF2-4540-BB8E-E8EA5C10528C">Core Interfaces</a>



<a href="https://msdn.microsoft.com/AED60281-A6E4-4AAD-A106-6CA6E9BAEB9A">ID3D12DeviceChild</a>



<a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a>



<a href="https://msdn.microsoft.com/F0FF3D7C-1DAC-48C3-B47D-0378BE369F37">Setting descriptor heaps</a>
 

 

