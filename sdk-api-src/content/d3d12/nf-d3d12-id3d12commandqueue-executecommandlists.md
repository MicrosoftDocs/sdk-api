---
UID: NF:d3d12.ID3D12CommandQueue.ExecuteCommandLists
title: ID3D12CommandQueue::ExecuteCommandLists (d3d12.h)
description: Submits an array of command lists for execution.
helpviewer_keywords: ["ExecuteCommandLists","ExecuteCommandLists method","ExecuteCommandLists method","ID3D12CommandQueue interface","ID3D12CommandQueue interface","ExecuteCommandLists method","ID3D12CommandQueue.ExecuteCommandLists","ID3D12CommandQueue::ExecuteCommandLists","d3d12/ID3D12CommandQueue::ExecuteCommandLists","direct3d12.id3d12commandqueue_executecommandlists"]
old-location: direct3d12\id3d12commandqueue_executecommandlists.htm
tech.root: direct3d12
ms.assetid: 653C15CD-0996-4B3B-A5F6-3E85CD0516AD
ms.date: 12/05/2018
ms.keywords: ExecuteCommandLists, ExecuteCommandLists method, ExecuteCommandLists method,ID3D12CommandQueue interface, ID3D12CommandQueue interface,ExecuteCommandLists method, ID3D12CommandQueue.ExecuteCommandLists, ID3D12CommandQueue::ExecuteCommandLists, d3d12/ID3D12CommandQueue::ExecuteCommandLists, direct3d12.id3d12commandqueue_executecommandlists
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12CommandQueue::ExecuteCommandLists
 - d3d12/ID3D12CommandQueue::ExecuteCommandLists
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.h
api_name:
 - ID3D12CommandQueue.ExecuteCommandLists
---

## -description

Submits an array of command lists for execution.

## -parameters

### -param NumCommandLists [in]

The number of command lists to be executed.

### -param ppCommandLists [in]

The array of <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist">ID3D12CommandList</a> command lists to be executed.

## -remarks

Calling **ExecuteCommandLists** twice in succession (from the same thread, or different threads) guarantees that the first workload (A) finishes before the second workload (B). Calling **ExecuteCommandLists** with *two* command lists allows the driver to merge the two command lists such that the second command list (D) may begin executing work before all work from the first (C) has finished. Specifically, your application is allowed to insert a fence signal or wait between A and B, and the driver has no visibility into this, so the driver must ensure that everything in A is complete before the fence operation. There is no such opportunity in a single call to the API, so the driver is able to optimize that scenario.

The driver is free to patch the submitted command lists. It is the calling application’s responsibility to ensure that the graphics processing unit (GPU) is not currently reading the any of the submitted command lists from a previous execution.

Applications are encouraged to batch together command list executions to reduce fixed costs associated with submitted commands to the GPU.

### Runtime validation

Bundles can't be submitted to a command queue directly. If a bundle is passed to this method, the runtime will drop the call. The runtime will also drop the call if the <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close">Close</a> function has not been called on one or more of the command lists.

The runtime will detect if the command allocators associated with the command lists have been reset after <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close">Close</a> was called.  The runtime will drop the call and remove the device in this situation.

The runtime will drop the call and remove the device if the command queue fence indicates that a previous execution of any of the command lists has not yet completed.

The runtime will validate the "before" and "after" states of resource transition barriers inside of <b>ExecuteCommandLists</b>.  If the “before” state of a transition does not match up with the “after” state of a previous transition, then the runtime will drop the call and remove the device.

The runtime will validate the “before” and “after” states of queries used by the command lists.  If an error is detected, then the runtime will drop the call and remove the device.

### Debug layer

The debug layer issues errors for all cases where the runtime would drop the call.

The debug layer issues an error if it detects that any resource referenced by the command lists, including queries, has been destroyed.

## Examples

Renders a scene.

```cpp
// Pipeline objects.
D3D12_VIEWPORT m_viewport;
ComPtr<IDXGISwapChain3> m_swapChain;
ComPtr<ID3D11DeviceContext> m_d3d11DeviceContext;
ComPtr<ID3D11On12Device> m_d3d11On12Device;
ComPtr<ID3D12Device> m_d3d12Device;
ComPtr<IDWriteFactory> m_dWriteFactory;
ComPtr<ID2D1Factory3> m_d2dFactory;
ComPtr<ID2D1Device2> m_d2dDevice;
ComPtr<ID2D1DeviceContext2> m_d2dDeviceContext;
ComPtr<ID3D12Resource> m_renderTargets[FrameCount];
ComPtr<ID3D11Resource> m_wrappedBackBuffers[FrameCount];
ComPtr<ID2D1Bitmap1> m_d2dRenderTargets[FrameCount];
ComPtr<ID3D12CommandAllocator> m_commandAllocators[FrameCount];
ComPtr<ID3D12CommandQueue> m_commandQueue;
ComPtr<ID3D12RootSignature> m_rootSignature;
ComPtr<ID3D12DescriptorHeap> m_rtvHeap;
ComPtr<ID3D12PipelineState> m_pipelineState;
ComPtr<ID3D12GraphicsCommandList> m_commandList;
D3D12_RECT m_scissorRect;
```

```cpp
// Render the scene.
void D3D1211on12::OnRender()
{
    // Record all the commands we need to render the scene into the command list.
    PopulateCommandList();

    // Execute the command list.
    ID3D12CommandList* ppCommandLists[] = { m_commandList.Get() };
    m_commandQueue->ExecuteCommandLists(_countof(ppCommandLists), ppCommandLists);

    RenderUI();

    // Present the frame.
    ThrowIfFailed(m_swapChain->Present(1, 0));

    MoveToNextFrame();
}
```

Refer to the <a href="/windows/desktop/direct3d12/notes-on-example-code">Example Code in the D3D12 Reference</a>.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue">ID3D12CommandQueue</a>
