---
UID: NN:d3d12.ID3D12CommandAllocator
title: ID3D12CommandAllocator (d3d12.h)
description: Represents the allocations of storage for graphics processing unit (GPU) commands.
helpviewer_keywords: ["ID3D12CommandAllocator","ID3D12CommandAllocator interface","ID3D12CommandAllocator interface","described","d3d12/ID3D12CommandAllocator","direct3d12.id3d12commandallocator"]
old-location: direct3d12\id3d12commandallocator.htm
tech.root: direct3d12
ms.assetid: ADC494E6-1698-415D-90C5-F99FCD4C5309
ms.date: 12/05/2018
ms.keywords: ID3D12CommandAllocator, ID3D12CommandAllocator interface, ID3D12CommandAllocator interface,described, d3d12/ID3D12CommandAllocator, direct3d12.id3d12commandallocator
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
 - ID3D12CommandAllocator
 - d3d12/ID3D12CommandAllocator
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
 - ID3D12CommandAllocator
---

# ID3D12CommandAllocator interface


## -description

Represents the allocations of storage for graphics processing unit (GPU) commands.

## -inheritance

The <b>ID3D12CommandAllocator</b> interface inherits from <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12pageable">ID3D12Pageable</a>. <b>ID3D12CommandAllocator</b> also has these types of members:

## -remarks

Use <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandallocator">ID3D12Device::CreateCommandAllocator</a> to create a command allocator object. 

The command allocator object corresponds to the underlying allocations in which GPU commands are stored.  The command allocator object applies to both direct command lists and bundles.  You must use a command allocator object in a DirectX 12 app.


#### Examples

The <a href="/windows/desktop/direct3d12/working-samples">D3D12nBodyGravity</a> sample uses <b>ID3D12CommandAllocator</b> as follows:
        

Header file declarations.


```cpp
D3D12_VIEWPORT m_viewport;
D3D12_RECT m_scissorRect;
ComPtr<IDXGISwapChain3> m_swapChain;
ComPtr<ID3D12Device> m_device;
ComPtr<ID3D12Resource> m_renderTargets[FrameCount];
ComPtr<ID3D12CommandAllocator> m_commandAllocator;
ComPtr<ID3D12CommandQueue> m_commandQueue;
ComPtr<ID3D12RootSignature> m_rootSignature;
ComPtr<ID3D12DescriptorHeap> m_rtvHeap;
ComPtr<ID3D12PipelineState> m_pipelineState;
ComPtr<ID3D12GraphicsCommandList> m_commandList;
UINT m_rtvDescriptorSize;

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


Refer to the <a href="/windows/desktop/direct3d12/notes-on-example-code">Example Code in the D3D12 Reference</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-interfaces">Core Interfaces</a>



<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12pageable">ID3D12Pageable</a>
