---
UID: NF:d3d12.ID3D12GraphicsCommandList.DrawInstanced
title: ID3D12GraphicsCommandList::DrawInstanced (d3d12.h)
description: Draws non-indexed, instanced primitives.
helpviewer_keywords: ["DrawInstanced","DrawInstanced method","DrawInstanced method","ID3D12GraphicsCommandList interface","ID3D12GraphicsCommandList interface","DrawInstanced method","ID3D12GraphicsCommandList.DrawInstanced","ID3D12GraphicsCommandList::DrawInstanced","d3d12/ID3D12GraphicsCommandList::DrawInstanced","direct3d12.id3d12graphicscommandlist_drawinstanced"]
old-location: direct3d12\id3d12graphicscommandlist_drawinstanced.htm
tech.root: direct3d12
ms.assetid: BB10C732-1F42-417D-ADDE-55E870AD5FE9
ms.date: 12/05/2018
ms.keywords: DrawInstanced, DrawInstanced method, DrawInstanced method,ID3D12GraphicsCommandList interface, ID3D12GraphicsCommandList interface,DrawInstanced method, ID3D12GraphicsCommandList.DrawInstanced, ID3D12GraphicsCommandList::DrawInstanced, d3d12/ID3D12GraphicsCommandList::DrawInstanced, direct3d12.id3d12graphicscommandlist_drawinstanced
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
 - ID3D12GraphicsCommandList::DrawInstanced
 - d3d12/ID3D12GraphicsCommandList::DrawInstanced
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
 - ID3D12GraphicsCommandList.DrawInstanced
---

# ID3D12GraphicsCommandList::DrawInstanced


## -description

Draws non-indexed, instanced primitives.

## -parameters

### -param VertexCountPerInstance [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of vertices to draw.

### -param InstanceCount [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of instances to draw.

### -param StartVertexLocation [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index of the first vertex.

### -param StartInstanceLocation [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A value added to each index before reading per-instance data from a vertex buffer.

## -remarks

A draw API submits work to the rendering pipeline.
        

Instancing might extend performance by reusing the same geometry to draw multiple objects in a scene. One example of instancing could be
          to draw the same object with different positions and colors.
        

The vertex data for an instanced draw call typically comes from a vertex buffer that is bound to the pipeline.
          But, you could also provide the vertex data from a shader that has instanced data identified with a system-value semantic (SV_InstanceID).
        


#### Examples

The <a href="/windows/desktop/direct3d12/working-samples">D3D12HelloTriangle</a> sample uses <b>ID3D12GraphicsCommandList::DrawInstanced</b> as follows:
        


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

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist">ID3D12GraphicsCommandList</a>