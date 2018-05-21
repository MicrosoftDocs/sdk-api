---
UID: NF:d3d12.ID3D12GraphicsCommandList.DrawInstanced
title: ID3D12GraphicsCommandList::DrawInstanced
author: windows-driver-content
description: Draws non-indexed, instanced primitives.
old-location: direct3d12\id3d12graphicscommandlist_drawinstanced.htm
old-project: direct3d12
ms.assetid: BB10C732-1F42-417D-ADDE-55E870AD5FE9
ms.author: windowsdriverdev
ms.date: 5/11/2018
ms.keywords: DrawInstanced, DrawInstanced method, DrawInstanced method,ID3D12GraphicsCommandList interface, ID3D12GraphicsCommandList interface,DrawInstanced method, ID3D12GraphicsCommandList.DrawInstanced, ID3D12GraphicsCommandList::DrawInstanced, d3d12/ID3D12GraphicsCommandList::DrawInstanced, direct3d12.id3d12graphicscommandlist_drawinstanced
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
req.typenames: D3D_SHADER_MODEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3d12.dll
api_name:
-	ID3D12GraphicsCommandList.DrawInstanced
product: Windows
targetos: Windows
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
---

# ID3D12GraphicsCommandList::DrawInstanced


## -description



          Draws non-indexed, instanced primitives.
        


## -parameters




### -param VertexCountPerInstance [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


            Number of vertices to draw.
          


### -param InstanceCount [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


            Number of instances to draw.
          


### -param StartVertexLocation [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


            Index of the first vertex.
          


### -param StartInstanceLocation [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


            A value added to each index before reading per-instance data from a vertex buffer.
          


## -returns



Returns nothing




## -remarks




          A draw API submits work to the rendering pipeline.
        


          Instancing might extend performance by reusing the same geometry to draw multiple objects in a scene. One example of instancing could be
          to draw the same object with different positions and colors.
        


          The vertex data for an instanced draw call typically comes from a vertex buffer that is bound to the pipeline.
          But, you could also provide the vertex data from a shader that has instanced data identified with a system-value semantic (SV_InstanceID).
        


#### Examples


          The <a href="https://msdn.microsoft.com/4C4475D4-534F-484F-8D60-9ACEA09AC109">D3D12HelloTriangle</a> sample uses <b>ID3D12GraphicsCommandList::DrawInstanced</b> as follows:
        

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
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>void D3D12HelloTriangle::PopulateCommandList()
{
    // Command list allocators can only be reset when the associated 
    // command lists have finished execution on the GPU; apps should use 
    // fences to determine GPU execution progress.
    ThrowIfFailed(m_commandAllocator-&gt;Reset());

    // However, when ExecuteCommandList() is called on a particular command 
    // list, that command list can then be reset at any time and must be before 
    // re-recording.
    ThrowIfFailed(m_commandList-&gt;Reset(m_commandAllocator.Get(), m_pipelineState.Get()));

    // Set necessary state.
    m_commandList-&gt;SetGraphicsRootSignature(m_rootSignature.Get());
    m_commandList-&gt;RSSetViewports(1, &amp;m_viewport);
    m_commandList-&gt;RSSetScissorRects(1, &amp;m_scissorRect);

    // Indicate that the back buffer will be used as a render target.
    m_commandList-&gt;ResourceBarrier(1, &amp;CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET));

    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap-&gt;GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_commandList-&gt;OMSetRenderTargets(1, &amp;rtvHandle, FALSE, nullptr);

    // Record commands.
    const float clearColor[] = { 0.0f, 0.2f, 0.4f, 1.0f };
    m_commandList-&gt;ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
    m_commandList-&gt;IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST);
    m_commandList-&gt;IASetVertexBuffers(0, 1, &amp;m_vertexBufferView);
    m_commandList-&gt;DrawInstanced(3, 1, 0, 0);

    // Indicate that the back buffer will now be used to present.
    m_commandList-&gt;ResourceBarrier(1, &amp;CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT));

    ThrowIfFailed(m_commandList-&gt;Close());
}
</pre>
</td>
</tr>
</table></span></div>

          See <a href="https://msdn.microsoft.com/C2323482-D06D-43B7-9BDE-BFB9A6A6B70D">Example Code in the D3D12 Reference</a>.
        

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a>
 

 

