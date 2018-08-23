---
UID: NN:d3d12.ID3D12GraphicsCommandList
title: ID3D12GraphicsCommandList
author: windows-sdk-content
description: Encapsulates a list of graphics commands for rendering. Includes APIs for instrumenting the command list execution, and for setting and clearing the pipeline state.
old-location: direct3d12\id3d12graphicscommandlist.htm
old-project: direct3d12
ms.assetid: 1BF282A7-F6D4-43A9-BDAD-D877564A1C6B
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: ID3D12GraphicsCommandList, ID3D12GraphicsCommandList interface, ID3D12GraphicsCommandList interface,described, d3d12/ID3D12GraphicsCommandList, direct3d12.id3d12graphicscommandlist
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d12.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D3D_SHADER_MODEL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12GraphicsCommandList
product: Windows
targetos: Windows
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
---

# ID3D12GraphicsCommandList interface


## -description


Encapsulates a list of graphics commands for rendering. Includes APIs for instrumenting the command list execution, and for setting and clearing the pipeline state.
<div class="alert"><b>Note</b>  The latest version of this interface is <a href="https://msdn.microsoft.com/E156C26B-0E51-4F43-9AB2-373E4C67A496">ID3D12GraphicsCommandList1</a> introduced in the Windows 10 Creators Update. Applications targetting Windows 10 Creators Update should use the <b>ID3D12GraphicsCommandList1</b> interface instead of <b>ID3D12GraphicsCommandList</b>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12GraphicsCommandList</b> interface inherits from <a href="https://msdn.microsoft.com/1E0359CC-0F53-4C82-9F1A-092F6F72EE20">ID3D12CommandList</a>. <b>ID3D12GraphicsCommandList</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/2A5292C0-ED9B-4E3C-87E4-88EA2FF09B28">BeginEvent</a>
</td>
<td align="left" width="63%">
Not intended to be called directly.  Use the
        <a href="https://blogs.msdn.microsoft.com/pix/winpixeventruntime/">PIX event runtime</a> to insert events into a command list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38011ED8-C867-4ECE-880F-3963A17790F7">BeginQuery</a>
</td>
<td align="left" width="63%">
Starts a query running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EF56EA6C-00DB-4231-B67D-B99811F51246">ClearDepthStencilView</a>
</td>
<td align="left" width="63%">
Clears the depth-stencil resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5AB13E36-A189-41B4-AEF8-B5C5831655DB">ClearRenderTargetView</a>
</td>
<td align="left" width="63%">
Sets all the elements in a render target to one value.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F7C230CE-0E28-466A-8A54-601ECEC6CDC9">ClearState</a>
</td>
<td align="left" width="63%">
Resets the state of a direct command list back to the state it was in when the command list was created.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6A19F429-D7B2-4A71-8904-31BFA1FD10C6">ClearUnorderedAccessViewFloat</a>
</td>
<td align="left" width="63%">
Sets all the elements in a unordered access view to the specified float values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A048BF0C-9141-4DDF-91F9-B53464033A44">ClearUnorderedAccessViewUint</a>
</td>
<td align="left" width="63%">
Sets all the elements in a unordered-access view to the specified integer values.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EA9F00AD-8506-4F3C-871E-A51ED69005BB">Close</a>
</td>
<td align="left" width="63%">
Indicates that recording to the command list has finished.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46F89B85-EDAA-4095-B6C6-4CC47F972F09">CopyBufferRegion</a>
</td>
<td align="left" width="63%">
Copies a region of a buffer from one resource to another.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EFC305CF-FBA9-4192-999B-6C6BFCDFF51F">CopyResource</a>
</td>
<td align="left" width="63%">
Copies the entire contents of the source resource to the destination resource.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2EAFC6B9-376C-4801-8E53-BF0DB08943AA">CopyTextureRegion</a>
</td>
<td align="left" width="63%">
This method uses the GPU to copy texture data between two locations. Both the source and the destination may reference texture data located within either a buffer resource or a texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F770CE6B-DD70-4102-BEFD-3E46B9957F5E">CopyTiles</a>
</td>
<td align="left" width="63%">
Copies tiles from buffer to tiled resource or vice versa.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2F4DBA5B-F586-4126-8867-BEE650F6D161">DiscardResource</a>
</td>
<td align="left" width="63%">
Discards a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/948EE430-6B34-473D-9B5F-1C78CECFBF6F">Dispatch</a>
</td>
<td align="left" width="63%">
Executes a command list from a thread group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16333C88-81B7-44D8-A226-D707C8A9CCF4">DrawIndexedInstanced</a>
</td>
<td align="left" width="63%">
Draws indexed, instanced primitives.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BB10C732-1F42-417D-ADDE-55E870AD5FE9">DrawInstanced</a>
</td>
<td align="left" width="63%">
Draws non-indexed, instanced primitives.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/24C40BE8-1080-4478-AB7C-D1FFCF6F5E3F">EndEvent</a>
</td>
<td align="left" width="63%">
Not intended to be called directly.  Use the
        <a href="https://blogs.msdn.microsoft.com/pix/winpixeventruntime/">PIX event runtime</a> to insert events into a command list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/591B277C-44C7-4C21-86B1-239F6A71308D">EndQuery</a>
</td>
<td align="left" width="63%">
Ends a running query.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B8AE4448-041D-47F6-9F0F-AE74FFEF6E41">ExecuteBundle</a>
</td>
<td align="left" width="63%">
Executes a bundle.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99FB088D-F3EB-4BAD-A945-51A1ED6F9288">ExecuteIndirect</a>
</td>
<td align="left" width="63%">
Apps perform indirect draws/dispatches using the <a href="https://msdn.microsoft.com/99FB088D-F3EB-4BAD-A945-51A1ED6F9288">ExecuteIndirect</a> method.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EB776EC7-42F2-47D3-A1FA-771EC6C4E3AB">IASetIndexBuffer</a>
</td>
<td align="left" width="63%">
Sets the view for the index buffer.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/743C48DF-C67E-48A0-B027-B2776E65968F">IASetPrimitiveTopology</a>
</td>
<td align="left" width="63%">
Bind information about the primitive type, and data order that describes input data for the input assembler stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AADD6CEF-376D-43AB-86E6-37B5D7DD0B25">IASetVertexBuffers</a>
</td>
<td align="left" width="63%">
Sets a CPU descriptor handle for the vertex buffers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/344FD8B5-7225-4BEC-9D1F-C9CEDFE8C60F">OMSetBlendFactor</a>
</td>
<td align="left" width="63%">
Sets the blend factor that modulate values for a pixel shader, render target, or both.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FE565AA2-FA34-4824-870E-9C4C7C19C93C">OMSetRenderTargets</a>
</td>
<td align="left" width="63%">
Sets CPU descriptor handles for the render targets and depth stencil.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/96C5C209-71A2-4096-A86C-D376AC1AB46C">OMSetStencilRef</a>
</td>
<td align="left" width="63%">
Sets the reference value for depth stencil tests.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36726FB6-09DE-4723-A60E-75FCE55F2E35">Reset</a>
</td>
<td align="left" width="63%">
Resets a command list back to its initial state as if a new command list was just created.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E3154DB7-DDA9-4480-A918-19C3A62944F2">ResolveQueryData</a>
</td>
<td align="left" width="63%">

Extracts data from a query. <a href="https://msdn.microsoft.com/E3154DB7-DDA9-4480-A918-19C3A62944F2">ResolveQueryData</a> works with all heap types (default, upload, and readback). 
            


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F1D4BAD1-B08E-47D0-9D2B-41873D6B4456">ResolveSubresource</a>
</td>
<td align="left" width="63%">
Copy a multi-sampled resource into a non-multi-sampled resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AA788F94-122B-4132-BED5-162EAC683676">ResourceBarrier</a>
</td>
<td align="left" width="63%">
Notifies the driver that it needs to synchronize multiple accesses to resources.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5A636CCB-34EB-4642-B588-4107D79F46F5">RSSetScissorRects</a>
</td>
<td align="left" width="63%">
Binds an array of scissor rectangles to the rasterizer stage.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ACFD260-1CE5-484C-83DD-021E8D895EBB">RSSetViewports</a>
</td>
<td align="left" width="63%">
Bind an array of viewports to the rasterizer stage of the pipeline.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A250052F-A24A-4234-8A39-0995A00B6E01">SetComputeRoot32BitConstant</a>
</td>
<td align="left" width="63%">
Sets a constant in the compute root signature.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A4623522-4748-4999-80EC-E6AC8934136A">SetComputeRoot32BitConstants</a>
</td>
<td align="left" width="63%">
Sets a group of constants in the compute root signature.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AEAB392F-365F-4EDB-AC57-FFAC40C800C0">SetComputeRootConstantBufferView</a>
</td>
<td align="left" width="63%">
Sets a CPU descriptor handle for the constant buffer in the compute root signature.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DC05D64A-39D0-4EF2-A9FE-956B499386F2">SetComputeRootDescriptorTable</a>
</td>
<td align="left" width="63%">
Sets a descriptor table into the compute root signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31BA8D5B-FAC3-4A4A-B2F2-76EC6399EFED">SetComputeRootShaderResourceView</a>
</td>
<td align="left" width="63%">
Sets a CPU descriptor handle for the shader resource in the compute root signature.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5DF04D51-DC09-4B02-8A82-ED68E049D392">SetComputeRootSignature</a>
</td>
<td align="left" width="63%">
Sets the layout of the compute root signature.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7C91B305-ABB2-4355-AA4B-3E1641ACF9E0">SetComputeRootUnorderedAccessView</a>
</td>
<td align="left" width="63%">
Sets a CPU descriptor handle for the unordered-access-view resource in the compute root signature.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EE475B68-1DCA-44D4-994E-717D40F47DFA">SetDescriptorHeaps</a>
</td>
<td align="left" width="63%">
Changes the currently bound descriptor heaps that are associated with a command list.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F53090CC-05E9-4892-B6BF-0A849A5D98EF">SetGraphicsRoot32BitConstant</a>
</td>
<td align="left" width="63%">
Sets a constant in the graphics root signature.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/509B8AA0-8128-4216-A9E2-67C027488E4A">SetGraphicsRoot32BitConstants</a>
</td>
<td align="left" width="63%">
Sets a group of constants in the graphics root signature.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59F6E33A-9BD8-4ED3-8CA7-235E2A0C2686">SetGraphicsRootConstantBufferView</a>
</td>
<td align="left" width="63%">
Sets a CPU descriptor handle for the constant buffer in the graphics root signature.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AF182E9D-6A85-42B2-ADE4-490756AEDCE7">SetGraphicsRootDescriptorTable</a>
</td>
<td align="left" width="63%">
Sets a descriptor table into the graphics root signature.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F16C8511-FF42-4DB3-81F7-9735FB1AADD7">SetGraphicsRootShaderResourceView</a>
</td>
<td align="left" width="63%">
Sets a CPU descriptor handle for the shader resource in the graphics root signature.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D2ACB026-A9E0-41BC-A3C2-6D0F55506519">SetGraphicsRootSignature</a>
</td>
<td align="left" width="63%">
Sets the layout of the graphics root signature.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7EF90634-0A33-42F5-880D-8E22910FAB47">SetGraphicsRootUnorderedAccessView</a>
</td>
<td align="left" width="63%">
Sets a CPU descriptor handle for the unordered-access-view resource in the graphics root signature.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/521844B8-0EF8-4F09-ABCE-E8C96129F548">SetMarker</a>
</td>
<td align="left" width="63%">
Not intended to be called directly.  Use the
        <a href="https://blogs.msdn.microsoft.com/pix/winpixeventruntime/">PIX event runtime</a> to insert events into a command list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/751E09A4-D8FE-4DEA-86D9-1C84265F2F21">SetPipelineState</a>
</td>
<td align="left" width="63%">
Sets all shaders and programs most of the fixed-function state of the GPU pipeline.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/21526012-A675-40E8-A11C-4CBA5C12B9CF">SetPredication</a>
</td>
<td align="left" width="63%">
Sets a rendering predicate.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40683FD6-5B9F-411C-AC0A-6641E0A3D688">SOSetTargets</a>
</td>
<td align="left" width="63%">
Sets the stream output buffer views.
        

</td>
</tr>
</table> 


## -remarks



This interface is new to D3D12, encapsulating much of the functionality of the <a href="https://msdn.microsoft.com/432f1d21-bf13-4569-9c8f-04f5d2845150">ID3D11CommandList</a> interface, and including the new functionality described in <a href="https://msdn.microsoft.com/5BF1440E-E4D8-43C8-BF0E-F02FEFE79C93">Rendering</a>.
        


#### Examples

The <a href="https://msdn.microsoft.com/4C4475D4-534F-484F-8D60-9ACEA09AC109">D3D12nBodyGravity</a> sample uses <b>ID3D12GraphicsCommandList</b> as follows:

Declare the pipeline objects.

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
Populating command lists.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Fill the command list with all the render commands and dependent state.
void D3D12nBodyGravity::PopulateCommandList()
{
    // Command list allocators can only be reset when the associated
    // command lists have finished execution on the GPU; apps should use
    // fences to determine GPU execution progress.
    ThrowIfFailed(m_commandAllocators[m_frameIndex]-&gt;Reset());

    // However, when ExecuteCommandList() is called on a particular command
    // list, that command list can then be reset at any time and must be before
    // re-recording.
    ThrowIfFailed(m_commandList-&gt;Reset(m_commandAllocators[m_frameIndex].Get(), m_pipelineState.Get()));

    // Set necessary state.
    m_commandList-&gt;SetPipelineState(m_pipelineState.Get());
    m_commandList-&gt;SetGraphicsRootSignature(m_rootSignature.Get());

    m_commandList-&gt;SetGraphicsRootConstantBufferView(RootParameterCB, m_constantBufferGS-&gt;GetGPUVirtualAddress() + m_frameIndex * sizeof(ConstantBufferGS));

    ID3D12DescriptorHeap* ppHeaps[] = { m_srvUavHeap.Get() };
    m_commandList-&gt;SetDescriptorHeaps(_countof(ppHeaps), ppHeaps);

    m_commandList-&gt;IASetVertexBuffers(0, 1, &amp;m_vertexBufferView);
    m_commandList-&gt;IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_POINTLIST);
    m_commandList-&gt;RSSetScissorRects(1, &amp;m_scissorRect);

    // Indicate that the back buffer will be used as a render target.
    m_commandList-&gt;ResourceBarrier(1, &amp;CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET));

    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap-&gt;GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_commandList-&gt;OMSetRenderTargets(1, &amp;rtvHandle, FALSE, nullptr);

    // Record commands.
    const float clearColor[] = { 0.0f, 0.0f, 0.1f, 0.0f };
    m_commandList-&gt;ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);

    // Render the particles.
    float viewportHeight = static_cast&lt;float&gt;(static_cast&lt;UINT&gt;(m_viewport.Height) / m_heightInstances);
    float viewportWidth = static_cast&lt;float&gt;(static_cast&lt;UINT&gt;(m_viewport.Width) / m_widthInstances);
    for (UINT n = 0; n &lt; ThreadCount; n++)
    {
        const UINT srvIndex = n + (m_srvIndex[n] == 0 ? SrvParticlePosVelo0 : SrvParticlePosVelo1);

        D3D12_VIEWPORT viewport;
        viewport.TopLeftX = (n % m_widthInstances) * viewportWidth;
        viewport.TopLeftY = (n / m_widthInstances) * viewportHeight;
        viewport.Width = viewportWidth;
        viewport.Height = viewportHeight;
        viewport.MinDepth = D3D12_MIN_DEPTH;
        viewport.MaxDepth = D3D12_MAX_DEPTH;
        m_commandList-&gt;RSSetViewports(1, &amp;viewport);

        CD3DX12_GPU_DESCRIPTOR_HANDLE srvHandle(m_srvUavHeap-&gt;GetGPUDescriptorHandleForHeapStart(), srvIndex, m_srvUavDescriptorSize);
        m_commandList-&gt;SetGraphicsRootDescriptorTable(RootParameterSRV, srvHandle);

        m_commandList-&gt;DrawInstanced(ParticleCount, 1, 0, 0);
    }

    m_commandList-&gt;RSSetViewports(1, &amp;m_viewport);

    // Indicate that the back buffer will now be used to present.
    m_commandList-&gt;ResourceBarrier(1, &amp;CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT));

    ThrowIfFailed(m_commandList-&gt;Close());
}
</pre>
</td>
</tr>
</table></span></div>
Refer to the <a href="https://msdn.microsoft.com/C2323482-D06D-43B7-9BDE-BFB9A6A6B70D">Example Code in the D3D12 Reference</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/A9BD5910-8FF2-4540-BB8E-E8EA5C10528C">Core Interfaces</a>



<a href="https://msdn.microsoft.com/1E0359CC-0F53-4C82-9F1A-092F6F72EE20">ID3D12CommandList</a>



<a href="https://msdn.microsoft.com/E156C26B-0E51-4F43-9AB2-373E4C67A496">ID3D12GraphicsCommandList1</a>
 

 

