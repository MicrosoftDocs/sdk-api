---
UID: NN:d3d12.ID3D12GraphicsCommandList
title: ID3D12GraphicsCommandList (d3d12.h)
description: Encapsulates a list of graphics commands for rendering. Includes APIs for instrumenting the command list execution, and for setting and clearing the pipeline state.
helpviewer_keywords: ["ID3D12GraphicsCommandList","ID3D12GraphicsCommandList interface","ID3D12GraphicsCommandList interface","described","d3d12/ID3D12GraphicsCommandList","direct3d12.id3d12graphicscommandlist"]
old-location: direct3d12\id3d12graphicscommandlist.htm
tech.root: direct3d12
ms.assetid: 1BF282A7-F6D4-43A9-BDAD-D877564A1C6B
ms.date: 12/05/2018
ms.keywords: ID3D12GraphicsCommandList, ID3D12GraphicsCommandList interface, ID3D12GraphicsCommandList interface,described, d3d12/ID3D12GraphicsCommandList, direct3d12.id3d12graphicscommandlist
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
 - ID3D12GraphicsCommandList
 - d3d12/ID3D12GraphicsCommandList
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
 - ID3D12GraphicsCommandList
---

# ID3D12GraphicsCommandList interface


## -description

Encapsulates a list of graphics commands for rendering. Includes APIs for instrumenting the command list execution, and for setting and clearing the pipeline state.
<div class="alert"><b>Note</b>  The latest version of this interface is <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist1">ID3D12GraphicsCommandList1</a> introduced in the Windows 10 Creators Update. Applications targetting Windows 10 Creators Update should use the <b>ID3D12GraphicsCommandList1</b> interface instead of <b>ID3D12GraphicsCommandList</b>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12GraphicsCommandList</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist">ID3D12CommandList</a>. <b>ID3D12GraphicsCommandList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12GraphicsCommandList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginevent">BeginEvent</a>
</td>
<td align="left" width="63%">
Not intended to be called directly.  Use the
        <a href="https://devblogs.microsoft.com/pix/winpixeventruntime/">PIX event runtime</a> to insert events into a command list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery">BeginQuery</a>
</td>
<td align="left" width="63%">
Starts a query running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview">ClearDepthStencilView</a>
</td>
<td align="left" width="63%">
Clears the depth-stencil resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview">ClearRenderTargetView</a>
</td>
<td align="left" width="63%">
Sets all the elements in a render target to one value.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate">ClearState</a>
</td>
<td align="left" width="63%">
Resets the state of a direct command list back to the state it was in when the command list was created.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat">ClearUnorderedAccessViewFloat</a>
</td>
<td align="left" width="63%">
Sets all the elements in a unordered access view to the specified float values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint">ClearUnorderedAccessViewUint</a>
</td>
<td align="left" width="63%">
Sets all the elements in a unordered-access view to the specified integer values.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close">Close</a>
</td>
<td align="left" width="63%">
Indicates that recording to the command list has finished.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion">CopyBufferRegion</a>
</td>
<td align="left" width="63%">
Copies a region of a buffer from one resource to another.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource">CopyResource</a>
</td>
<td align="left" width="63%">
Copies the entire contents of the source resource to the destination resource.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion">CopyTextureRegion</a>
</td>
<td align="left" width="63%">
This method uses the GPU to copy texture data between two locations. Both the source and the destination may reference texture data located within either a buffer resource or a texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles">CopyTiles</a>
</td>
<td align="left" width="63%">
Copies tiles from buffer to tiled resource or vice versa.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource">DiscardResource</a>
</td>
<td align="left" width="63%">
Discards a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch">Dispatch</a>
</td>
<td align="left" width="63%">
Executes a command list from a thread group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced">DrawIndexedInstanced</a>
</td>
<td align="left" width="63%">
Draws indexed, instanced primitives.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced">DrawInstanced</a>
</td>
<td align="left" width="63%">
Draws non-indexed, instanced primitives.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endevent">EndEvent</a>
</td>
<td align="left" width="63%">
Not intended to be called directly.  Use the
        <a href="https://devblogs.microsoft.com/pix/winpixeventruntime/">PIX event runtime</a> to insert events into a command list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery">EndQuery</a>
</td>
<td align="left" width="63%">
Ends a running query.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle">ExecuteBundle</a>
</td>
<td align="left" width="63%">
Executes a bundle.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect">ExecuteIndirect</a>
</td>
<td align="left" width="63%">
Apps perform indirect draws/dispatches using the <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect">ExecuteIndirect</a> method.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer">IASetIndexBuffer</a>
</td>
<td align="left" width="63%">
Sets the view for the index buffer.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology">IASetPrimitiveTopology</a>
</td>
<td align="left" width="63%">
Bind information about the primitive type, and data order that describes input data for the input assembler stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers">IASetVertexBuffers</a>
</td>
<td align="left" width="63%">
Sets a CPU descriptor handle for the vertex buffers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetblendfactor">OMSetBlendFactor</a>
</td>
<td align="left" width="63%">
Sets the blend factor that modulate values for a pixel shader, render target, or both.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets">OMSetRenderTargets</a>
</td>
<td align="left" width="63%">
Sets CPU descriptor handles for the render targets and depth stencil.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref">OMSetStencilRef</a>
</td>
<td align="left" width="63%">
Sets the reference value for depth stencil tests.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets a command list back to its initial state as if a new command list was just created.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata">ResolveQueryData</a>
</td>
<td align="left" width="63%">

Extracts data from a query. <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata">ResolveQueryData</a> works with all heap types (default, upload, and readback). 
            


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource">ResolveSubresource</a>
</td>
<td align="left" width="63%">
Copy a multi-sampled resource into a non-multi-sampled resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier">ResourceBarrier</a>
</td>
<td align="left" width="63%">
Notifies the driver that it needs to synchronize multiple accesses to resources.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects">RSSetScissorRects</a>
</td>
<td align="left" width="63%">
Binds an array of scissor rectangles to the rasterizer stage.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports">RSSetViewports</a>
</td>
<td align="left" width="63%">
Bind an array of viewports to the rasterizer stage of the pipeline.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant">SetComputeRoot32BitConstant</a>
</td>
<td align="left" width="63%">
Sets a constant in the compute root signature.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants">SetComputeRoot32BitConstants</a>
</td>
<td align="left" width="63%">
Sets a group of constants in the compute root signature.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview">SetComputeRootConstantBufferView</a>
</td>
<td align="left" width="63%">
Sets a CPU descriptor handle for the constant buffer in the compute root signature.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable">SetComputeRootDescriptorTable</a>
</td>
<td align="left" width="63%">
Sets a descriptor table into the compute root signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview">SetComputeRootShaderResourceView</a>
</td>
<td align="left" width="63%">
Sets a CPU descriptor handle for the shader resource in the compute root signature.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature">SetComputeRootSignature</a>
</td>
<td align="left" width="63%">
Sets the layout of the compute root signature.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview">SetComputeRootUnorderedAccessView</a>
</td>
<td align="left" width="63%">
Sets a CPU descriptor handle for the unordered-access-view resource in the compute root signature.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps">SetDescriptorHeaps</a>
</td>
<td align="left" width="63%">
Changes the currently bound descriptor heaps that are associated with a command list.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstant">SetGraphicsRoot32BitConstant</a>
</td>
<td align="left" width="63%">
Sets a constant in the graphics root signature.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstants">SetGraphicsRoot32BitConstants</a>
</td>
<td align="left" width="63%">
Sets a group of constants in the graphics root signature.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootconstantbufferview">SetGraphicsRootConstantBufferView</a>
</td>
<td align="left" width="63%">
Sets a CPU descriptor handle for the constant buffer in the graphics root signature.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable">SetGraphicsRootDescriptorTable</a>
</td>
<td align="left" width="63%">
Sets a descriptor table into the graphics root signature.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootshaderresourceview">SetGraphicsRootShaderResourceView</a>
</td>
<td align="left" width="63%">
Sets a CPU descriptor handle for the shader resource in the graphics root signature.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature">SetGraphicsRootSignature</a>
</td>
<td align="left" width="63%">
Sets the layout of the graphics root signature.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootunorderedaccessview">SetGraphicsRootUnorderedAccessView</a>
</td>
<td align="left" width="63%">
Sets a CPU descriptor handle for the unordered-access-view resource in the graphics root signature.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setmarker">SetMarker</a>
</td>
<td align="left" width="63%">
Not intended to be called directly.  Use the
        <a href="https://devblogs.microsoft.com/pix/winpixeventruntime/">PIX event runtime</a> to insert events into a command list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate">SetPipelineState</a>
</td>
<td align="left" width="63%">
Sets all shaders and programs most of the fixed-function state of the GPU pipeline.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication">SetPredication</a>
</td>
<td align="left" width="63%">
Sets a rendering predicate.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets">SOSetTargets</a>
</td>
<td align="left" width="63%">
Sets the stream output buffer views.
        

</td>
</tr>
</table>

## -remarks

This interface is new to D3D12, encapsulating much of the functionality of the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11commandlist">ID3D11CommandList</a> interface, and including the new functionality described in <a href="https://docs.microsoft.com/windows/desktop/direct3d12/rendering">Rendering</a>.
        


#### Examples

The <a href="https://docs.microsoft.com/windows/desktop/direct3d12/working-samples">D3D12nBodyGravity</a> sample uses <b>ID3D12GraphicsCommandList</b> as follows:

Declare the pipeline objects.


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


Populating command lists.


```cpp
// Fill the command list with all the render commands and dependent state.
void D3D12nBodyGravity::PopulateCommandList()
{
    // Command list allocators can only be reset when the associated
    // command lists have finished execution on the GPU; apps should use
    // fences to determine GPU execution progress.
    ThrowIfFailed(m_commandAllocators[m_frameIndex]->Reset());

    // However, when ExecuteCommandList() is called on a particular command
    // list, that command list can then be reset at any time and must be before
    // re-recording.
    ThrowIfFailed(m_commandList->Reset(m_commandAllocators[m_frameIndex].Get(), m_pipelineState.Get()));

    // Set necessary state.
    m_commandList->SetPipelineState(m_pipelineState.Get());
    m_commandList->SetGraphicsRootSignature(m_rootSignature.Get());

    m_commandList->SetGraphicsRootConstantBufferView(RootParameterCB, m_constantBufferGS->GetGPUVirtualAddress() + m_frameIndex * sizeof(ConstantBufferGS));

    ID3D12DescriptorHeap* ppHeaps[] = { m_srvUavHeap.Get() };
    m_commandList->SetDescriptorHeaps(_countof(ppHeaps), ppHeaps);

    m_commandList->IASetVertexBuffers(0, 1, &m_vertexBufferView);
    m_commandList->IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_POINTLIST);
    m_commandList->RSSetScissorRects(1, &m_scissorRect);

    // Indicate that the back buffer will be used as a render target.
    m_commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET));

    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_commandList->OMSetRenderTargets(1, &rtvHandle, FALSE, nullptr);

    // Record commands.
    const float clearColor[] = { 0.0f, 0.0f, 0.1f, 0.0f };
    m_commandList->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);

    // Render the particles.
    float viewportHeight = static_cast<float>(static_cast<UINT>(m_viewport.Height) / m_heightInstances);
    float viewportWidth = static_cast<float>(static_cast<UINT>(m_viewport.Width) / m_widthInstances);
    for (UINT n = 0; n < ThreadCount; n++)
    {
        const UINT srvIndex = n + (m_srvIndex[n] == 0 ? SrvParticlePosVelo0 : SrvParticlePosVelo1);

        D3D12_VIEWPORT viewport;
        viewport.TopLeftX = (n % m_widthInstances) * viewportWidth;
        viewport.TopLeftY = (n / m_widthInstances) * viewportHeight;
        viewport.Width = viewportWidth;
        viewport.Height = viewportHeight;
        viewport.MinDepth = D3D12_MIN_DEPTH;
        viewport.MaxDepth = D3D12_MAX_DEPTH;
        m_commandList->RSSetViewports(1, &viewport);

        CD3DX12_GPU_DESCRIPTOR_HANDLE srvHandle(m_srvUavHeap->GetGPUDescriptorHandleForHeapStart(), srvIndex, m_srvUavDescriptorSize);
        m_commandList->SetGraphicsRootDescriptorTable(RootParameterSRV, srvHandle);

        m_commandList->DrawInstanced(ParticleCount, 1, 0, 0);
    }

    m_commandList->RSSetViewports(1, &m_viewport);

    // Indicate that the back buffer will now be used to present.
    m_commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT));

    ThrowIfFailed(m_commandList->Close());
}

```


Refer to the <a href="https://docs.microsoft.com/windows/desktop/direct3d12/notes-on-example-code">Example Code in the D3D12 Reference</a>.

<div class="code"></div>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-interfaces">Core Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist">ID3D12CommandList</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist1">ID3D12GraphicsCommandList1</a>

