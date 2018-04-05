---
UID: NF:d3d12.ID3D12CommandAllocator.Reset
title: ID3D12CommandAllocator::Reset method
author: windows-driver-content
description: Indicates to re-use the memory that is associated with the command allocator.
old-location: direct3d12\id3d12commandallocator_reset.htm
old-project: direct3d12
ms.assetid: B7477767-9110-45DE-962F-E56FDB635D17
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: ID3D12CommandAllocator, ID3D12CommandAllocator interface, Reset method, ID3D12CommandAllocator::Reset, Reset method, Reset method, ID3D12CommandAllocator interface, Reset,ID3D12CommandAllocator.Reset, d3d12/ID3D12CommandAllocator::Reset, direct3d12.id3d12commandallocator_reset
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
-	D3D12.dll
api_name:
-	ID3D12CommandAllocator.Reset
product: Windows
targetos: Windows
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
---

# ID3D12CommandAllocator::Reset method


## -description


Indicates to re-use the memory that is associated with the command allocator.


## -parameters






## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns <b>E_FAIL</b> if there is an actively recording command list referencing the command allocator.  The debug layer will also issue an error in this case.  
        See <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a> for other possible return values.




## -remarks



Apps call <b>Reset</b> to re-use the memory that is associated with a command allocator.  From this call to <b>Reset</b>, the runtime and driver determine that the graphics processing unit (GPU) is no longer executing any command lists that have recorded commands with the command allocator.

Unlike <a href="https://msdn.microsoft.com/36726FB6-09DE-4723-A60E-75FCE55F2E35">ID3D12GraphicsCommandList::Reset</a>, it is not recommended that you call <b>Reset</b>  on the command allocator while a command list is still being executed. 

The debug layer will issue a warning if it can't prove that there are no pending GPU references to command lists that have recorded commands in the allocator.

The debug layer will issue an error if <b>Reset</b> is called concurrently by multiple threads (on the same allocator object).


#### Examples


          The <a href="https://msdn.microsoft.com/4C4475D4-534F-484F-8D60-9ACEA09AC109">D3D12HelloTriangle</a> sample uses <b>ID3D12CommandAllocator::Reset</b> as follows:
        

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
<pre>// Command list allocators can only be reset when the associated 
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
</pre>
</td>
</tr>
</table></span></div>
Refer to the <a href="https://msdn.microsoft.com/C2323482-D06D-43B7-9BDE-BFB9A6A6B70D">Example Code in the D3D12 Reference</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/ADC494E6-1698-415D-90C5-F99FCD4C5309">ID3D12CommandAllocator</a>
 

 

