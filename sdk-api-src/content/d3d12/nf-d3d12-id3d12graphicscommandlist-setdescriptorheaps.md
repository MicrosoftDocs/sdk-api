---
UID: NF:d3d12.ID3D12GraphicsCommandList.SetDescriptorHeaps
title: ID3D12GraphicsCommandList::SetDescriptorHeaps
author: windows-sdk-content
description: Changes the currently bound descriptor heaps that are associated with a command list.
old-location: direct3d12\id3d12graphicscommandlist_setdescriptorheaps.htm
tech.root: direct3d12
ms.assetid: EE475B68-1DCA-44D4-994E-717D40F47DFA
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: ID3D12GraphicsCommandList interface,SetDescriptorHeaps method, ID3D12GraphicsCommandList.SetDescriptorHeaps, ID3D12GraphicsCommandList::SetDescriptorHeaps, SetDescriptorHeaps, SetDescriptorHeaps method, SetDescriptorHeaps method,ID3D12GraphicsCommandList interface, d3d12/ID3D12GraphicsCommandList::SetDescriptorHeaps, direct3d12.id3d12graphicscommandlist_setdescriptorheaps
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
 - ID3D12GraphicsCommandList.SetDescriptorHeaps
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d12.h
: 
- ID3D12GraphicsCommandList.SetDescriptorHeaps
: 
---

# ID3D12GraphicsCommandList::SetDescriptorHeaps


## -description


Changes the currently bound descriptor heaps that are associated with a command list.
        


## -parameters




### -param NumDescriptorHeaps [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of descriptor heaps to bind.
          


### -param ppDescriptorHeaps [in]

Type: <b><a href="https://msdn.microsoft.com/B6FF011B-3FED-425B-B9D5-A823E6915FD5">ID3D12DescriptorHeap</a>*</b>

A pointer to an array of <a href="https://msdn.microsoft.com/B6FF011B-3FED-425B-B9D5-A823E6915FD5">ID3D12DescriptorHeap</a> objects for the heaps to set on the command list.
            


## -returns



This method does not return a value.
          




## -remarks



<b>SetDescriptorHeaps</b> can be called on a bundle, but the bundle descriptor heaps must match the calling command list descriptor heap. For more information on bundle restrictions, refer to <a href="recording_command_lists_and_bundles.htm">Creating and Recording Command Lists and Bundles</a>.


#### Examples

The <a href="https://msdn.microsoft.com/4C4475D4-534F-484F-8D60-9ACEA09AC109">D3D12Bundles</a> sample uses <b>ID3D12GraphicsCommandList::SetDescriptorHeaps</b> as follows:
        


```cpp
void D3D12Bundles::PopulateCommandList(FrameResource* pFrameResource)
{
    // Command list allocators can only be reset when the associated
    // command lists have finished execution on the GPU; apps should use
    // fences to determine GPU execution progress.
    ThrowIfFailed(m_pCurrentFrameResource->m_commandAllocator->Reset());

    // However, when ExecuteCommandList() is called on a particular command
    // list, that command list can then be reset at any time and must be before
    // re-recording.
    ThrowIfFailed(m_commandList->Reset(m_pCurrentFrameResource->m_commandAllocator.Get(), m_pipelineState1.Get()));

    // Set necessary state.
    m_commandList->SetGraphicsRootSignature(m_rootSignature.Get());

    ID3D12DescriptorHeap* ppHeaps[] = { m_cbvSrvHeap.Get(), m_samplerHeap.Get() };
    m_commandList->SetDescriptorHeaps(_countof(ppHeaps), ppHeaps);

    m_commandList->RSSetViewports(1, &m_viewport);
    m_commandList->RSSetScissorRects(1, &m_scissorRect);

    // Indicate that the back buffer will be used as a render target.
    m_commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET));

    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    CD3DX12_CPU_DESCRIPTOR_HANDLE dsvHandle(m_dsvHeap->GetCPUDescriptorHandleForHeapStart());
    m_commandList->OMSetRenderTargets(1, &rtvHandle, FALSE, &dsvHandle);

    // Record commands.
    const float clearColor[] = { 0.0f, 0.2f, 0.4f, 1.0f };
    m_commandList->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
    m_commandList->ClearDepthStencilView(m_dsvHeap->GetCPUDescriptorHandleForHeapStart(), D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    if (UseBundles)
    {
        // Execute the prebuilt bundle.
        m_commandList->ExecuteBundle(pFrameResource->m_bundle.Get());
    }
    else
    {
        // Populate a new command list.
        pFrameResource->PopulateCommandList(m_commandList.Get(), m_pipelineState1.Get(), m_pipelineState2.Get(), m_currentFrameResourceIndex, m_numIndices, &m_indexBufferView,
            &m_vertexBufferView, m_cbvSrvHeap.Get(), m_cbvSrvDescriptorSize, m_samplerHeap.Get(), m_rootSignature.Get());
    }

    // Indicate that the back buffer will now be used to present.
    m_commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT));

    ThrowIfFailed(m_commandList->Close());
}

```


See <a href="https://msdn.microsoft.com/C2323482-D06D-43B7-9BDE-BFB9A6A6B70D">Example Code in the D3D12 Reference</a>.
        

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/04D3FACF-21EC-45CA-AD9B-78FDCDDC7136">Descriptor Heaps</a>



<a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a>
 

 

