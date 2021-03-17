---
UID: NF:d3d12.ID3D12GraphicsCommandList.ClearRenderTargetView
title: ID3D12GraphicsCommandList::ClearRenderTargetView (d3d12.h)
description: Sets all the elements in a render target to one value.
helpviewer_keywords: ["ClearRenderTargetView","ClearRenderTargetView method","ClearRenderTargetView method","ID3D12GraphicsCommandList interface","ID3D12GraphicsCommandList interface","ClearRenderTargetView method","ID3D12GraphicsCommandList.ClearRenderTargetView","ID3D12GraphicsCommandList::ClearRenderTargetView","d3d12/ID3D12GraphicsCommandList::ClearRenderTargetView","direct3d12.id3d12graphicscommandlist_clearrendertargetview"]
old-location: direct3d12\id3d12graphicscommandlist_clearrendertargetview.htm
tech.root: direct3d12
ms.assetid: 5AB13E36-A189-41B4-AEF8-B5C5831655DB
ms.date: 12/05/2018
ms.keywords: ClearRenderTargetView, ClearRenderTargetView method, ClearRenderTargetView method,ID3D12GraphicsCommandList interface, ID3D12GraphicsCommandList interface,ClearRenderTargetView method, ID3D12GraphicsCommandList.ClearRenderTargetView, ID3D12GraphicsCommandList::ClearRenderTargetView, d3d12/ID3D12GraphicsCommandList::ClearRenderTargetView, direct3d12.id3d12graphicscommandlist_clearrendertargetview
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
 - ID3D12GraphicsCommandList::ClearRenderTargetView
 - d3d12/ID3D12GraphicsCommandList::ClearRenderTargetView
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
 - ID3D12GraphicsCommandList.ClearRenderTargetView
---

# ID3D12GraphicsCommandList::ClearRenderTargetView


## -description

Sets all the elements in a render target to one value.

## -parameters

### -param RenderTargetView [in]

Type: <b><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle">D3D12_CPU_DESCRIPTOR_HANDLE</a></b>

Specifies a D3D12_CPU_DESCRIPTOR_HANDLE structure that describes the CPU descriptor handle that represents the start of the heap for the render target to be cleared.

### -param ColorRGBA [in]

Type: <b>const FLOAT[4]</b>

A 4-component array that represents the color to fill the render target with.

### -param NumRects [in]

Type: <b>UINT</b>

The number of rectangles in the array that the <i>pRects</i> parameter specifies.

### -param pRects [in]

Type: <b>const D3D12_RECT*</b>

An array of <b>D3D12_RECT</b> structures for the rectangles in the resource view to clear. If <b>NULL</b>, <b>ClearRenderTargetView</b> clears the entire resource view.

## -remarks

<b>ClearRenderTargetView</b> may be used to initialize resources which alias the same heap memory. See <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource">CreatePlacedResource</a> for more details.

<h3><a id="Runtime_validation"></a><a id="runtime_validation"></a><a id="RUNTIME_VALIDATION"></a>Runtime validation</h3>
For floating-point inputs, the runtime will set denormalized values to 0 (while preserving NANs).  

Validation failure will result in the call to <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close">Close</a> returning <b>E_INVALIDARG</b>.
          

<h3><a id="Debug_layer"></a><a id="debug_layer"></a><a id="DEBUG_LAYER"></a>Debug layer</h3>
The debug layer will issue errors if the input colors are denormalized.

The debug layer will issue an error if the subresources referenced by the view are not in the appropriate state.
            For <b>ClearRenderTargetView</b>, the state must be <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states">D3D12_RESOURCE_STATE_RENDER_TARGET</a>.
          


#### Examples

The <a href="/windows/desktop/direct3d12/working-samples">D3D12HelloTriangle</a> sample uses <b>ID3D12GraphicsCommandList::ClearRenderTargetView</b> as follows:
        


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


The <a href="/windows/desktop/direct3d12/working-samples">D3D12Multithreading</a> sample uses <b>ID3D12GraphicsCommandList::ClearRenderTargetView</b> as follows:


```cpp
// Frame resources.
FrameResource* m_frameResources[FrameCount];
FrameResource* m_pCurrentFrameResource;
int m_currentFrameResourceIndex;

```



```cpp
// Assemble the CommandListPre command list.
void D3D12Multithreading::BeginFrame()
{
    m_pCurrentFrameResource->Init();

    // Indicate that the back buffer will be used as a render target.
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET));

    // Clear the render target and depth stencil.
    const float clearColor[] = { 0.0f, 0.0f, 0.0f, 1.0f };
    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ClearDepthStencilView(m_dsvHeap->GetCPUDescriptorHandleForHeapStart(), D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListPre]->Close());
}

// Assemble the CommandListMid command list.
void D3D12Multithreading::MidFrame()
{
    // Transition our shadow map from the shadow pass to readable in the scene pass.
    m_pCurrentFrameResource->SwapBarriers();

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListMid]->Close());
}

```


See <a href="/windows/desktop/direct3d12/notes-on-example-code">Example Code in the D3D12 Reference</a>.
        

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist">ID3D12GraphicsCommandList</a>