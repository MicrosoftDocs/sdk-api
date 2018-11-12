---
UID: NF:d3d12.ID3D12GraphicsCommandList.RSSetViewports
title: ID3D12GraphicsCommandList::RSSetViewports
author: windows-sdk-content
description: Bind an array of viewports to the rasterizer stage of the pipeline.
old-location: direct3d12\id3d12graphicscommandlist_rssetviewports.htm
tech.root: direct3d12
ms.assetid: 1ACFD260-1CE5-484C-83DD-021E8D895EBB
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ID3D12GraphicsCommandList interface,RSSetViewports method, ID3D12GraphicsCommandList.RSSetViewports, ID3D12GraphicsCommandList::RSSetViewports, RSSetViewports, RSSetViewports method, RSSetViewports method,ID3D12GraphicsCommandList interface, d3d12/ID3D12GraphicsCommandList::RSSetViewports, direct3d12.id3d12graphicscommandlist_rssetviewports
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
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12GraphicsCommandList.RSSetViewports
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12GraphicsCommandList::RSSetViewports


## -description


Bind an array of viewports to the rasterizer stage of the pipeline.
        


## -parameters




### -param NumViewports [in]

Type: <b>UINT</b>

Number of viewports to bind.
            The range of valid values is (0, D3D12_VIEWPORT_AND_SCISSORRECT_OBJECT_COUNT_PER_PIPELINE).
          


### -param pViewports [in]

Type: <b>const <a href="https://msdn.microsoft.com/BD23FEF6-8231-45C6-8A6B-F0E42FE88A9F">D3D12_VIEWPORT</a>*</b>

An array of <a href="https://msdn.microsoft.com/BD23FEF6-8231-45C6-8A6B-F0E42FE88A9F">D3D12_VIEWPORT</a> structures to bind to the device.
          


## -returns



This method does not return a value.
          




## -remarks



All viewports must be set atomically as one operation. Any viewports not defined by the call are disabled.
        

Which viewport to use is determined by the <a href="https://msdn.microsoft.com/6f5c504c-1940-4d1c-b594-a2132599376b">SV_ViewportArrayIndex</a> semantic output by a geometry shader; if a geometry shader does not specify the semantic, Direct3D will use the first viewport in the array.
        

<div class="alert"><b>Note</b>  Even though you specify float values to the members of the <a href="https://msdn.microsoft.com/BD23FEF6-8231-45C6-8A6B-F0E42FE88A9F">D3D12_VIEWPORT</a> structure for the <i>pViewports</i> array in a call to  <b>RSSetViewports</b> for <a href="https://msdn.microsoft.com/5ad0525c-249f-452d-950b-df8fa2addde2">feature levels</a> 9_x, <b>RSSetViewports</b> uses DWORDs internally. Because of this behavior, when you use a negative top left corner for the viewport, the call to  <b>RSSetViewports</b> for feature levels 9_x fails. This failure occurs because <b>RSSetViewports</b> for 9_x casts the floating point values into unsigned integers without validation, which results in integer overflow.
      </div>
<div> </div>

#### Examples

The <a href="https://msdn.microsoft.com/4C4475D4-534F-484F-8D60-9ACEA09AC109">D3D12HelloTriangle</a> sample uses <b>ID3D12GraphicsCommandList::RSSetViewports</b> as follows:
        


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


See <a href="https://msdn.microsoft.com/C2323482-D06D-43B7-9BDE-BFB9A6A6B70D">Example Code in the D3D12 Reference</a>.
        

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a>
 

 

