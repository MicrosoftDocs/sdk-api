---
UID: NN:d3d12.ID3D12PipelineState
title: ID3D12PipelineState (d3d12.h)
description: Represents the state of all currently set shaders as well as certain fixed function state objects.
helpviewer_keywords: ["ID3D12PipelineState","ID3D12PipelineState interface","ID3D12PipelineState interface","described","d3d12/ID3D12PipelineState","direct3d12.id3d12pipelinestate"]
old-location: direct3d12\id3d12pipelinestate.htm
tech.root: direct3d12
ms.assetid: DD922194-8AD2-4ADF-9AC2-46C903C56AE6
ms.date: 12/05/2018
ms.keywords: ID3D12PipelineState, ID3D12PipelineState interface, ID3D12PipelineState interface,described, d3d12/ID3D12PipelineState, direct3d12.id3d12pipelinestate
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12PipelineState
 - d3d12/ID3D12PipelineState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12PipelineState
---

# ID3D12PipelineState interface


## -description

Represents the state of all currently set shaders as well as certain fixed function state objects.

## -inheritance

The <b>ID3D12PipelineState</b> interface inherits from <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12pageable">ID3D12Pageable</a>. <b>ID3D12PipelineState</b> also has these types of members:

## -remarks

Use <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate">ID3D12Device::CreateGraphicsPipelineState</a> or  <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate">ID3D12Device::CreateComputePipelineState</a> to create a pipeline state object (PSO). 

A pipeline state object corresponds to a significant portion of the state of the graphics processing unit (GPU).  This state includes all currently set shaders and certain fixed function state objects.  The only way to change states contained within the pipeline object is to change the currently bound pipeline object.


#### Examples

The <a href="/windows/desktop/direct3d12/working-samples">D3D12DynamicIndexing</a> sample uses <b>ID3D12PipelineState</b> as follows:
        

Declare the pipeline objects.


```cpp
// Asset objects.
ComPtr<ID3D12PipelineState> m_pipelineState;
ComPtr<ID3D12PipelineState> m_computeState;
ComPtr<ID3D12GraphicsCommandList> m_commandList;
ComPtr<ID3D12Resource> m_vertexBuffer;
ComPtr<ID3D12Resource> m_vertexBufferUpload;
D3D12_VERTEX_BUFFER_VIEW m_vertexBufferView;
ComPtr<ID3D12Resource> m_particleBuffer0[ThreadCount];
ComPtr<ID3D12Resource> m_particleBuffer1[ThreadCount];
ComPtr<ID3D12Resource> m_particleBuffer0Upload[ThreadCount];
ComPtr<ID3D12Resource> m_particleBuffer1Upload[ThreadCount];
ComPtr<ID3D12Resource> m_constantBufferGS;
UINT8* m_pConstantBufferGSData;
ComPtr<ID3D12Resource> m_constantBufferCS;

```


Initializing a bundle.


```cpp
void FrameResource::InitBundle(ID3D12Device* pDevice, ID3D12PipelineState* pPso,
    UINT frameResourceIndex, UINT numIndices, D3D12_INDEX_BUFFER_VIEW* pIndexBufferViewDesc, D3D12_VERTEX_BUFFER_VIEW* pVertexBufferViewDesc,
    ID3D12DescriptorHeap* pCbvSrvDescriptorHeap, UINT cbvSrvDescriptorSize, ID3D12DescriptorHeap* pSamplerDescriptorHeap, ID3D12RootSignature* pRootSignature)
{
    ThrowIfFailed(pDevice->CreateCommandList(0, D3D12_COMMAND_LIST_TYPE_BUNDLE, m_bundleAllocator.Get(), pPso, IID_PPV_ARGS(&m_bundle)));

    PopulateCommandList(m_bundle.Get(), pPso, frameResourceIndex, numIndices, pIndexBufferViewDesc,
        pVertexBufferViewDesc, pCbvSrvDescriptorHeap, cbvSrvDescriptorSize, pSamplerDescriptorHeap, pRootSignature);

    ThrowIfFailed(m_bundle->Close());
}

```


The <a href="/windows/desktop/direct3d12/working-samples">D3D12Bundles</a> sample uses <b>ID3D12PipelineState</b> as follows:
        

Populating the command lists, note the alternating PSO.


```cpp
void FrameResource::PopulateCommandList(ID3D12GraphicsCommandList* pCommandList, ID3D12PipelineState* pPso1, ID3D12PipelineState* pPso2,
    UINT frameResourceIndex, UINT numIndices, D3D12_INDEX_BUFFER_VIEW* pIndexBufferViewDesc, D3D12_VERTEX_BUFFER_VIEW* pVertexBufferViewDesc,
    ID3D12DescriptorHeap* pCbvSrvDescriptorHeap, UINT cbvSrvDescriptorSize, ID3D12DescriptorHeap* pSamplerDescriptorHeap, ID3D12RootSignature* pRootSignature)
{
    // If the root signature matches the root signature of the caller, then
    // bindings are inherited, otherwise the bind space is reset.
    pCommandList->SetGraphicsRootSignature(pRootSignature);

    ID3D12DescriptorHeap* ppHeaps[] = { pCbvSrvDescriptorHeap, pSamplerDescriptorHeap };
    pCommandList->SetDescriptorHeaps(_countof(ppHeaps), ppHeaps);
    pCommandList->IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST);

    pCommandList->IASetIndexBuffer(pIndexBufferViewDesc);

    pCommandList->IASetVertexBuffers(0, 1, pVertexBufferViewDesc);

    pCommandList->SetGraphicsRootDescriptorTable(0, pCbvSrvDescriptorHeap->GetGPUDescriptorHandleForHeapStart());
    pCommandList->SetGraphicsRootDescriptorTable(1, pSamplerDescriptorHeap->GetGPUDescriptorHandleForHeapStart());

    // Calculate the descriptor offset due to multiple frame resources.
    // 1 SRV + how many CBVs we have currently.
    UINT frameResourceDescriptorOffset = 1 + (frameResourceIndex * m_cityRowCount * m_cityColumnCount);
    CD3DX12_GPU_DESCRIPTOR_HANDLE cbvSrvHandle(pCbvSrvDescriptorHeap->GetGPUDescriptorHandleForHeapStart(), frameResourceDescriptorOffset, cbvSrvDescriptorSize);

    BOOL usePso1 = TRUE;
    for (UINT i = 0; i < m_cityRowCount; i++)
    {
        for (UINT j = 0; j < m_cityColumnCount; j++)
        {
            // Alternate which PSO to use; the pixel shader is different on 
            // each just as a PSO setting demonstration.
            pCommandList->SetPipelineState(usePso1 ? pPso1 : pPso2);
            usePso1 = !usePso1;

            // Set this city's CBV table and move to the next descriptor.
            pCommandList->SetGraphicsRootDescriptorTable(2, cbvSrvHandle);
            cbvSrvHandle.Offset(cbvSrvDescriptorSize);

            pCommandList->DrawIndexedInstanced(numIndices, 1, 0, 0, 0);
        }
    }
}

```


Refer to the <a href="/windows/desktop/direct3d12/notes-on-example-code">Example Code in the D3D12 Reference</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-interfaces">Core Interfaces</a>



<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12pageable">ID3D12Pageable</a>
