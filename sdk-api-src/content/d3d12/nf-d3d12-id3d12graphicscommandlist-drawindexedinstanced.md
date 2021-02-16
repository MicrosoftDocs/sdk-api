---
UID: NF:d3d12.ID3D12GraphicsCommandList.DrawIndexedInstanced
title: ID3D12GraphicsCommandList::DrawIndexedInstanced (d3d12.h)
description: Draws indexed, instanced primitives.
helpviewer_keywords: ["DrawIndexedInstanced","DrawIndexedInstanced method","DrawIndexedInstanced method","ID3D12GraphicsCommandList interface","ID3D12GraphicsCommandList interface","DrawIndexedInstanced method","ID3D12GraphicsCommandList.DrawIndexedInstanced","ID3D12GraphicsCommandList::DrawIndexedInstanced","d3d12/ID3D12GraphicsCommandList::DrawIndexedInstanced","direct3d12.id3d12graphicscommandlist_drawindexedinstanced"]
old-location: direct3d12\id3d12graphicscommandlist_drawindexedinstanced.htm
tech.root: direct3d12
ms.assetid: 16333C88-81B7-44D8-A226-D707C8A9CCF4
ms.date: 12/05/2018
ms.keywords: DrawIndexedInstanced, DrawIndexedInstanced method, DrawIndexedInstanced method,ID3D12GraphicsCommandList interface, ID3D12GraphicsCommandList interface,DrawIndexedInstanced method, ID3D12GraphicsCommandList.DrawIndexedInstanced, ID3D12GraphicsCommandList::DrawIndexedInstanced, d3d12/ID3D12GraphicsCommandList::DrawIndexedInstanced, direct3d12.id3d12graphicscommandlist_drawindexedinstanced
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
 - ID3D12GraphicsCommandList::DrawIndexedInstanced
 - d3d12/ID3D12GraphicsCommandList::DrawIndexedInstanced
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
 - ID3D12GraphicsCommandList.DrawIndexedInstanced
---

# ID3D12GraphicsCommandList::DrawIndexedInstanced


## -description

Draws indexed, instanced primitives.

## -parameters

### -param IndexCountPerInstance [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of indices read from the index buffer for each instance.

### -param InstanceCount [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of instances to draw.

### -param StartIndexLocation [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The location of the first index read by the GPU from the index buffer.

### -param BaseVertexLocation [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

A value added to each index before reading a vertex from the vertex buffer.

### -param StartInstanceLocation [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A value added to each index before reading per-instance data from a vertex buffer.

## -remarks

A draw API submits work to the rendering pipeline.

Instancing might extend performance by reusing the same geometry to draw multiple objects in a scene. One example of instancing could be 
      to draw the same object with different positions and colors. Instancing requires multiple vertex buffers: at least one for per-vertex data 
      and a second buffer for per-instance data.


#### Examples

The <a href="/windows/desktop/direct3d12/working-samples">D3D12Bundles</a> sample uses <b>ID3D12GraphicsCommandList::DrawIndexedInstanced</b> as follows:
        


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


See <a href="/windows/desktop/direct3d12/notes-on-example-code">Example Code in the D3D12 Reference</a>.
        

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist">ID3D12GraphicsCommandList</a>