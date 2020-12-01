---
UID: NF:d3d12.ID3D12GraphicsCommandList.Dispatch
title: ID3D12GraphicsCommandList::Dispatch (d3d12.h)
description: Executes a compute shader on a thread group.
helpviewer_keywords: ["Dispatch","Dispatch method","Dispatch method","ID3D12GraphicsCommandList interface","ID3D12GraphicsCommandList interface","Dispatch method","ID3D12GraphicsCommandList.Dispatch","ID3D12GraphicsCommandList::Dispatch","d3d12/ID3D12GraphicsCommandList::Dispatch","direct3d12.id3d12graphicscommandlist_dispatch"]
old-location: direct3d12\id3d12graphicscommandlist_dispatch.htm
tech.root: direct3d12
ms.assetid: 948EE430-6B34-473D-9B5F-1C78CECFBF6F
ms.date: 12/05/2018
ms.keywords: Dispatch, Dispatch method, Dispatch method,ID3D12GraphicsCommandList interface, ID3D12GraphicsCommandList interface,Dispatch method, ID3D12GraphicsCommandList.Dispatch, ID3D12GraphicsCommandList::Dispatch, d3d12/ID3D12GraphicsCommandList::Dispatch, direct3d12.id3d12graphicscommandlist_dispatch
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
 - ID3D12GraphicsCommandList::Dispatch
 - d3d12/ID3D12GraphicsCommandList::Dispatch
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
 - ID3D12GraphicsCommandList.Dispatch
---

# ID3D12GraphicsCommandList::Dispatch


## -description

Executes a command list from a thread group.

## -parameters

### -param ThreadGroupCountX [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of groups dispatched in the x direction. <i>ThreadGroupCountX</i> must be less than or equal to D3D11_CS_DISPATCH_MAX_THREAD_GROUPS_PER_DIMENSION (65535).

### -param ThreadGroupCountY [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of groups dispatched in the y direction. <i>ThreadGroupCountY</i> must be less than or equal to D3D11_CS_DISPATCH_MAX_THREAD_GROUPS_PER_DIMENSION (65535).

### -param ThreadGroupCountZ [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of groups dispatched in the z direction.  <i>ThreadGroupCountZ</i> must be less than or equal to D3D11_CS_DISPATCH_MAX_THREAD_GROUPS_PER_DIMENSION (65535).
            In feature level 10 the value for <i>ThreadGroupCountZ</i> must be 1.

## -remarks

You call the <b>Dispatch</b> method to execute commands in a compute shader. A compute shader can be run on many threads in parallel, within a thread group. Index a particular thread, within a thread group using a 3D vector
          given by (x,y,z).
        


#### Examples

The <a href="/windows/desktop/direct3d12/working-samples">D3D12nBodyGravity</a> sample uses <b>ID3D12GraphicsCommandList::Dispatch</b> as follows:
        


```cpp
// Run the particle simulation using the compute shader.
void D3D12nBodyGravity::Simulate(UINT threadIndex)
{
    ID3D12GraphicsCommandList* pCommandList = m_computeCommandList[threadIndex].Get();

    UINT srvIndex;
    UINT uavIndex;
    ID3D12Resource *pUavResource;
    if (m_srvIndex[threadIndex] == 0)
    {
        srvIndex = SrvParticlePosVelo0;
        uavIndex = UavParticlePosVelo1;
        pUavResource = m_particleBuffer1[threadIndex].Get();
    }
    else
    {
        srvIndex = SrvParticlePosVelo1;
        uavIndex = UavParticlePosVelo0;
        pUavResource = m_particleBuffer0[threadIndex].Get();
    }

    pCommandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(pUavResource, D3D12_RESOURCE_STATE_NON_PIXEL_SHADER_RESOURCE, D3D12_RESOURCE_STATE_UNORDERED_ACCESS));

    pCommandList->SetPipelineState(m_computeState.Get());
    pCommandList->SetComputeRootSignature(m_computeRootSignature.Get());

    ID3D12DescriptorHeap* ppHeaps[] = { m_srvUavHeap.Get() };
    pCommandList->SetDescriptorHeaps(_countof(ppHeaps), ppHeaps);

    CD3DX12_GPU_DESCRIPTOR_HANDLE srvHandle(m_srvUavHeap->GetGPUDescriptorHandleForHeapStart(), srvIndex + threadIndex, m_srvUavDescriptorSize);
    CD3DX12_GPU_DESCRIPTOR_HANDLE uavHandle(m_srvUavHeap->GetGPUDescriptorHandleForHeapStart(), uavIndex + threadIndex, m_srvUavDescriptorSize);

    pCommandList->SetComputeRootConstantBufferView(RootParameterCB, m_constantBufferCS->GetGPUVirtualAddress());
    pCommandList->SetComputeRootDescriptorTable(RootParameterSRV, srvHandle);
    pCommandList->SetComputeRootDescriptorTable(RootParameterUAV, uavHandle);

    pCommandList->Dispatch(static_cast<int>(ceil(ParticleCount / 128.0f)), 1, 1);

    pCommandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(pUavResource, D3D12_RESOURCE_STATE_UNORDERED_ACCESS, D3D12_RESOURCE_STATE_NON_PIXEL_SHADER_RESOURCE));
}

```


See <a href="/windows/desktop/direct3d12/notes-on-example-code">Example Code in the D3D12 Reference</a>.
        

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist">ID3D12GraphicsCommandList</a>