---
UID: NF:d3d12.ID3D12GraphicsCommandList.Close
title: ID3D12GraphicsCommandList::Close
author: windows-sdk-content
description: Indicates that recording to the command list has finished.
old-location: direct3d12\id3d12graphicscommandlist_close.htm
old-project: direct3d12
ms.assetid: EA9F00AD-8506-4F3C-871E-A51ED69005BB
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: Close, Close method, Close method,ID3D12GraphicsCommandList interface, ID3D12GraphicsCommandList interface,Close method, ID3D12GraphicsCommandList.Close, ID3D12GraphicsCommandList::Close, d3d12/ID3D12GraphicsCommandList::Close, direct3d12.id3d12graphicscommandlist_close
ms.prod: windows
ms.technology: windows-sdk
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
 - ID3D12GraphicsCommandList.Close
product: Windows
targetos: Windows
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
---

# ID3D12GraphicsCommandList::Close


## -description



          Indicates that recording to the command list has finished.
        


## -parameters






## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>


                Returns <b>S_OK</b> if successful; otherwise, returns one of the following values:
              

<ul>
<li><b>E_FAIL</b> if the command list has already been closed, or an invalid API was called during command list recording.
              </li>
<li><b>E_OUTOFMEMORY</b> if the operating system ran out of memory during recording.
              </li>
<li><b>E_INVALIDARG</b> if an invalid argument was passed to the command list API during recording.
              </li>
</ul>

              See <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a> for other possible return values.
            




## -remarks




        The runtime will validate that the command list has not previously been closed.  If an error was encountered during recording, the error code is returned here.  The runtime won't call the close device driver interface (DDI) in this case.
      


#### Examples


          The <a href="https://msdn.microsoft.com/4C4475D4-534F-484F-8D60-9ACEA09AC109">D3D12HelloTriangle</a> sample uses <b>ID3D12GraphicsCommandList::Close</b> as follows:
        

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
<pre>void D3D12HelloTriangle::LoadAssets()
{
    // Create an empty root signature.
    {
        CD3DX12_ROOT_SIGNATURE_DESC rootSignatureDesc;
        rootSignatureDesc.Init(0, nullptr, 0, nullptr, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT);

        ComPtr&lt;ID3DBlob&gt; signature;
        ComPtr&lt;ID3DBlob&gt; error;
        ThrowIfFailed(D3D12SerializeRootSignature(&amp;rootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &amp;signature, &amp;error));
        ThrowIfFailed(m_device-&gt;CreateRootSignature(0, signature-&gt;GetBufferPointer(), signature-&gt;GetBufferSize(), IID_PPV_ARGS(&amp;m_rootSignature)));
    }

    // Create the pipeline state, which includes compiling and loading shaders.
    {
        ComPtr&lt;ID3DBlob&gt; vertexShader;
        ComPtr&lt;ID3DBlob&gt; pixelShader;

#if defined(_DEBUG)
        // Enable better shader debugging with the graphics debugging tools.
        UINT compileFlags = D3DCOMPILE_DEBUG | D3DCOMPILE_SKIP_OPTIMIZATION;
#else
        UINT compileFlags = 0;
#endif

        ThrowIfFailed(D3DCompileFromFile(GetAssetFullPath(L"shaders.hlsl").c_str(), nullptr, nullptr, "VSMain", "vs_5_0", compileFlags, 0, &amp;vertexShader, nullptr));
        ThrowIfFailed(D3DCompileFromFile(GetAssetFullPath(L"shaders.hlsl").c_str(), nullptr, nullptr, "PSMain", "ps_5_0", compileFlags, 0, &amp;pixelShader, nullptr));

        // Define the vertex input layout.
        D3D12_INPUT_ELEMENT_DESC inputElementDescs[] =
        {
            { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 0, D3D12_INPUT_CLASSIFICATION_PER_VERTEX_DATA, 0 },
            { "COLOR", 0, DXGI_FORMAT_R32G32B32A32_FLOAT, 0, 12, D3D12_INPUT_CLASSIFICATION_PER_VERTEX_DATA, 0 }
        };

        // Describe and create the graphics pipeline state object (PSO).
        D3D12_GRAPHICS_PIPELINE_STATE_DESC psoDesc = {};
        psoDesc.InputLayout = { inputElementDescs, _countof(inputElementDescs) };
        psoDesc.pRootSignature = m_rootSignature.Get();
        psoDesc.VS = { reinterpret_cast&lt;UINT8*&gt;(vertexShader-&gt;GetBufferPointer()), vertexShader-&gt;GetBufferSize() };
        psoDesc.PS = { reinterpret_cast&lt;UINT8*&gt;(pixelShader-&gt;GetBufferPointer()), pixelShader-&gt;GetBufferSize() };
        psoDesc.RasterizerState = CD3DX12_RASTERIZER_DESC(D3D12_DEFAULT);
        psoDesc.BlendState = CD3DX12_BLEND_DESC(D3D12_DEFAULT);
        psoDesc.DepthStencilState.DepthEnable = FALSE;
        psoDesc.DepthStencilState.StencilEnable = FALSE;
        psoDesc.SampleMask = UINT_MAX;
        psoDesc.PrimitiveTopologyType = D3D12_PRIMITIVE_TOPOLOGY_TYPE_TRIANGLE;
        psoDesc.NumRenderTargets = 1;
        psoDesc.RTVFormats[0] = DXGI_FORMAT_R8G8B8A8_UNORM;
        psoDesc.SampleDesc.Count = 1;
        ThrowIfFailed(m_device-&gt;CreateGraphicsPipelineState(&amp;psoDesc, IID_PPV_ARGS(&amp;m_pipelineState)));
    }

    // Create the command list.
    ThrowIfFailed(m_device-&gt;CreateCommandList(0, D3D12_COMMAND_LIST_TYPE_DIRECT, m_commandAllocator.Get(), m_pipelineState.Get(), IID_PPV_ARGS(&amp;m_commandList)));

    // Command lists are created in the recording state, but there is nothing
    // to record yet. The main loop expects it to be closed, so close it now.
    ThrowIfFailed(m_commandList-&gt;Close());

    // Create the vertex buffer.
    {
        // Define the geometry for a triangle.
        Vertex triangleVertices[] =
        {
            { { 0.0f, 0.25f * m_aspectRatio, 0.0f }, { 1.0f, 0.0f, 0.0f, 1.0f } },
            { { 0.25f, -0.25f * m_aspectRatio, 0.0f }, { 0.0f, 1.0f, 0.0f, 1.0f } },
            { { -0.25f, -0.25f * m_aspectRatio, 0.0f }, { 0.0f, 0.0f, 1.0f, 1.0f } }
        };

        const UINT vertexBufferSize = sizeof(triangleVertices);

        // Note: using upload heaps to transfer static data like vert buffers is not 
        // recommended. Every time the GPU needs it, the upload heap will be marshalled 
        // over. Please read up on Default Heap usage. An upload heap is used here for 
        // code simplicity and because there are very few verts to actually transfer.
        ThrowIfFailed(m_device-&gt;CreateCommittedResource(
            &amp;CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &amp;CD3DX12_RESOURCE_DESC::Buffer(vertexBufferSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&amp;m_vertexBuffer)));

        // Copy the triangle data to the vertex buffer.
        UINT8* pVertexDataBegin;
        CD3DX12_RANGE readRange(0, 0);        // We do not intend to read from this resource on the CPU.
        ThrowIfFailed(m_vertexBuffer-&gt;Map(0, &amp;readRange, reinterpret_cast&lt;void**&gt;(&amp;pVertexDataBegin)));
        memcpy(pVertexDataBegin, triangleVertices, sizeof(triangleVertices));
        m_vertexBuffer-&gt;Unmap(0, nullptr);

        // Initialize the vertex buffer view.
        m_vertexBufferView.BufferLocation = m_vertexBuffer-&gt;GetGPUVirtualAddress();
        m_vertexBufferView.StrideInBytes = sizeof(Vertex);
        m_vertexBufferView.SizeInBytes = vertexBufferSize;
    }

    // Create synchronization objects and wait until assets have been uploaded to the GPU.
    {
        ThrowIfFailed(m_device-&gt;CreateFence(0, D3D12_FENCE_FLAG_NONE, IID_PPV_ARGS(&amp;m_fence)));
        m_fenceValue = 1;

        // Create an event handle to use for frame synchronization.
        m_fenceEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);
        if (m_fenceEvent == nullptr)
        {
            ThrowIfFailed(HRESULT_FROM_WIN32(GetLastError()));
        }

        // Wait for the command list to execute; we are reusing the same command 
        // list in our main loop but for now, we just want to wait for setup to 
        // complete before continuing.
        WaitForPreviousFrame();
    }
}
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
 

 

