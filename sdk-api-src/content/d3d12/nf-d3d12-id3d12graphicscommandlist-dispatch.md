---
UID: NF:d3d12.ID3D12GraphicsCommandList.Dispatch
title: ID3D12GraphicsCommandList::Dispatch
author: windows-sdk-content
description: Executes a command list from a thread group.
old-location: direct3d12\id3d12graphicscommandlist_dispatch.htm
old-project: direct3d12
ms.assetid: 948EE430-6B34-473D-9B5F-1C78CECFBF6F
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: Dispatch, Dispatch method, Dispatch method,ID3D12GraphicsCommandList interface, ID3D12GraphicsCommandList interface,Dispatch method, ID3D12GraphicsCommandList.Dispatch, ID3D12GraphicsCommandList::Dispatch, d3d12/ID3D12GraphicsCommandList::Dispatch, direct3d12.id3d12graphicscommandlist_dispatch
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
 - ID3D12GraphicsCommandList.Dispatch
product: Windows
targetos: Windows
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
---

# ID3D12GraphicsCommandList::Dispatch


## -description


Executes a command list from a thread group.


## -parameters




### -param ThreadGroupCountX [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of groups dispatched in the x direction. <i>ThreadGroupCountX</i> must be less than or equal to D3D11_CS_DISPATCH_MAX_THREAD_GROUPS_PER_DIMENSION (65535).
          


### -param ThreadGroupCountY [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of groups dispatched in the y direction. <i>ThreadGroupCountY</i> must be less than or equal to D3D11_CS_DISPATCH_MAX_THREAD_GROUPS_PER_DIMENSION (65535).
          


### -param ThreadGroupCountZ [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of groups dispatched in the z direction.  <i>ThreadGroupCountZ</i> must be less than or equal to D3D11_CS_DISPATCH_MAX_THREAD_GROUPS_PER_DIMENSION (65535).
            In feature level 10 the value for <i>ThreadGroupCountZ</i> must be 1.
          


## -returns



Returns nothing.




## -remarks



You call the <b>Dispatch</b> method to execute commands in a compute shader. A compute shader can be run on many threads in parallel, within a thread group. Index a particular thread, within a thread group using a 3D vector
          given by (x,y,z).
        


#### Examples

The <a href="https://msdn.microsoft.com/4C4475D4-534F-484F-8D60-9ACEA09AC109">D3D12nBodyGravity</a> sample uses <b>ID3D12GraphicsCommandList::Dispatch</b> as follows:
        

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Run the particle simulation using the compute shader.
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

    pCommandList-&gt;ResourceBarrier(1, &amp;CD3DX12_RESOURCE_BARRIER::Transition(pUavResource, D3D12_RESOURCE_STATE_NON_PIXEL_SHADER_RESOURCE, D3D12_RESOURCE_STATE_UNORDERED_ACCESS));

    pCommandList-&gt;SetPipelineState(m_computeState.Get());
    pCommandList-&gt;SetComputeRootSignature(m_computeRootSignature.Get());

    ID3D12DescriptorHeap* ppHeaps[] = { m_srvUavHeap.Get() };
    pCommandList-&gt;SetDescriptorHeaps(_countof(ppHeaps), ppHeaps);

    CD3DX12_GPU_DESCRIPTOR_HANDLE srvHandle(m_srvUavHeap-&gt;GetGPUDescriptorHandleForHeapStart(), srvIndex + threadIndex, m_srvUavDescriptorSize);
    CD3DX12_GPU_DESCRIPTOR_HANDLE uavHandle(m_srvUavHeap-&gt;GetGPUDescriptorHandleForHeapStart(), uavIndex + threadIndex, m_srvUavDescriptorSize);

    pCommandList-&gt;SetComputeRootConstantBufferView(RootParameterCB, m_constantBufferCS-&gt;GetGPUVirtualAddress());
    pCommandList-&gt;SetComputeRootDescriptorTable(RootParameterSRV, srvHandle);
    pCommandList-&gt;SetComputeRootDescriptorTable(RootParameterUAV, uavHandle);

    pCommandList-&gt;Dispatch(static_cast&lt;int&gt;(ceil(ParticleCount / 128.0f)), 1, 1);

    pCommandList-&gt;ResourceBarrier(1, &amp;CD3DX12_RESOURCE_BARRIER::Transition(pUavResource, D3D12_RESOURCE_STATE_UNORDERED_ACCESS, D3D12_RESOURCE_STATE_NON_PIXEL_SHADER_RESOURCE));
}
</pre>
</td>
</tr>
</table></span></div>
See <a href="https://msdn.microsoft.com/C2323482-D06D-43B7-9BDE-BFB9A6A6B70D">Example Code in the D3D12 Reference</a>.
        

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a>
 

 

