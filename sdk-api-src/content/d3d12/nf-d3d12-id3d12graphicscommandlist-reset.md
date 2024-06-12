---
UID: NF:d3d12.ID3D12GraphicsCommandList.Reset
title: ID3D12GraphicsCommandList::Reset (d3d12.h)
description: Resets a command list back to its initial state as if a new command list was just created. (ID3D12GraphicsCommandList.Reset)
helpviewer_keywords: ["ID3D12GraphicsCommandList interface","Reset method","ID3D12GraphicsCommandList.Reset","ID3D12GraphicsCommandList::Reset","Reset","Reset method","Reset method","ID3D12GraphicsCommandList interface","d3d12/ID3D12GraphicsCommandList::Reset","direct3d12.id3d12graphicscommandlist_reset"]
old-location: direct3d12\id3d12graphicscommandlist_reset.htm
tech.root: direct3d12
ms.assetid: 36726FB6-09DE-4723-A60E-75FCE55F2E35
ms.date: 12/05/2018
ms.keywords: ID3D12GraphicsCommandList interface,Reset method, ID3D12GraphicsCommandList.Reset, ID3D12GraphicsCommandList::Reset, Reset, Reset method, Reset method,ID3D12GraphicsCommandList interface, d3d12/ID3D12GraphicsCommandList::Reset, direct3d12.id3d12graphicscommandlist_reset
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
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12GraphicsCommandList::Reset
 - d3d12/ID3D12GraphicsCommandList::Reset
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12GraphicsCommandList.Reset
---

# ID3D12GraphicsCommandList::Reset


## -description

Resets a command list back to its initial state as if a new command list was just created.

## -parameters

### -param pAllocator [in]

Type: <b>ID3D12CommandAllocator*</b>

A pointer to the <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12commandallocator">ID3D12CommandAllocator</a> object that the device creates command lists from.

### -param pInitialState [in, optional]

Type: <b>ID3D12PipelineState*</b>

A pointer to the <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12pipelinestate">ID3D12PipelineState</a> object that contains the initial pipeline state for the command list.  This is optional and can be NULL.  If NULL, the runtime sets a dummy initial pipeline state so that drivers don't have to deal with undefined state.  The overhead for this is low, particularly for a command list, for which the overall cost of recording the command list likely dwarfs the cost of one initial state setting.  So there is little cost in  not setting the initial pipeline state parameter if it isn't convenient.  

For bundles on the other hand, it might make more sense to try to set the initial state parameter since bundles are likely smaller overall and can be reused frequently.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns <b>S_OK</b> if successful; otherwise, returns one of the following values:
              

<ul>
<li><b>E_FAIL</b> if the command list was not in the "closed" state when the <b>Reset</b> call was made, or the per-device limit would have been exceeded.
              </li>
<li><b>E_OUTOFMEMORY</b> if the operating system ran out of memory.
              </li>
<li><b>E_INVALIDARG</b> if the allocator is currently being used with another command list in the "recording" state or if the specified allocator was created with the wrong type.
              </li>
</ul>
See <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a> for other possible return values.

## -remarks

By using <b>Reset</b>, you can re-use command list tracking structures without any allocations. Unlike <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12commandallocator-reset">ID3D12CommandAllocator::Reset</a>, you can call <b>Reset</b> while the command list is still being executed.

You can use <b>Reset</b> for both direct command lists and bundles.
      

The command allocator passed to <b>Reset</b> cannot be associated with any other currently-recording command list.  The allocator type, direct command list or bundle, must match the type of command list that is being created.
      

If a bundle doesn't specify a resource heap, it can't make changes to which descriptor tables are bound. Either way, bundles can't change the resource heap within the bundle. If a heap is specified for a bundle, the heap must match the calling 'parent' command list’s heap.
      

<h3><a id="Runtime_validation"></a><a id="runtime_validation"></a><a id="RUNTIME_VALIDATION"></a>Runtime validation</h3>
Before an app calls <b>Reset</b>, the command list must be in the "closed" state.  <b>Reset</b> will fail if the command list isn't in the "closed" state.
          

<div class="alert"><b>Note</b>  If a call to <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close">ID3D12GraphicsCommandList::Close</a> fails, the command list can never be reset.  Calling <b>Reset</b> will result in the same error being returned that <b>ID3D12GraphicsCommandList::Close</b> returned.
          </div>
<div> </div>
After <b>Reset</b> succeeds, the command list is left in the "recording" state.  <b>Reset</b> will fail if it would cause the maximum concurrently recording command list limit, which is specified at device creation, to be exceeded.
          

Apps must specify a command list allocator.  The runtime will ensure that an allocator is never associated with more than one recording command list at the same time.
          

<b>Reset</b> fails for bundles that are referenced by a not yet submitted command list.
          

<h3><a id="Debug_layer"></a><a id="debug_layer"></a><a id="DEBUG_LAYER"></a>Debug layer</h3>
The debug layer will also track graphics processing unit (GPU) progress and issue an error if it can't prove that there are no outstanding executions of the command list.
          


#### Examples

The <a href="/windows/desktop/direct3d12/working-samples">D3D12HelloTriangle</a> sample uses <b>ID3D12GraphicsCommandList::Reset</b> as follows:
        


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



```cpp
void D3D12HelloTriangle::PopulateCommandList()
{
    // Command list allocators can only be reset when the associated 
    // command lists have finished execution on the GPU; apps should use 
    // fences to determine GPU execution progress.
    ThrowIfFailed(m_commandAllocator->Reset());

    // However, when ExecuteCommandList() is called on a particular command 
    // list, that command list can then be reset at any time and must be before 
    // re-recording.
    ThrowIfFailed(m_commandList->Reset(m_commandAllocator.Get(), m_pipelineState.Get()));

    // Set necessary state.
    m_commandList->SetGraphicsRootSignature(m_rootSignature.Get());
    m_commandList->RSSetViewports(1, &m_viewport);
    m_commandList->RSSetScissorRects(1, &m_scissorRect);

    // Indicate that the back buffer will be used as a render target.
    m_commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET));

    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_commandList->OMSetRenderTargets(1, &rtvHandle, FALSE, nullptr);

    // Record commands.
    const float clearColor[] = { 0.0f, 0.2f, 0.4f, 1.0f };
    m_commandList->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
    m_commandList->IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST);
    m_commandList->IASetVertexBuffers(0, 1, &m_vertexBufferView);
    m_commandList->DrawInstanced(3, 1, 0, 0);

    // Indicate that the back buffer will now be used to present.
    m_commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT));

    ThrowIfFailed(m_commandList->Close());
}

```


See <a href="/windows/desktop/direct3d12/notes-on-example-code">Example Code in the D3D12 Reference</a>.
        

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12commandallocator-reset">ID3D12CommandAllocator::Reset</a>



<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandlist">ID3D12Device::CreateCommandList</a>



<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist">ID3D12GraphicsCommandList</a>
