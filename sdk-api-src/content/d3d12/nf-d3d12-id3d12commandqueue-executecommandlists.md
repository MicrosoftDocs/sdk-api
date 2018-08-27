---
UID: NF:d3d12.ID3D12CommandQueue.ExecuteCommandLists
title: ID3D12CommandQueue::ExecuteCommandLists
author: windows-sdk-content
description: Submits an array of command lists for execution.
old-location: direct3d12\id3d12commandqueue_executecommandlists.htm
old-project: direct3d12
ms.assetid: 653C15CD-0996-4B3B-A5F6-3E85CD0516AD
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: ExecuteCommandLists, ExecuteCommandLists method, ExecuteCommandLists method,ID3D12CommandQueue interface, ID3D12CommandQueue interface,ExecuteCommandLists method, ID3D12CommandQueue.ExecuteCommandLists, ID3D12CommandQueue::ExecuteCommandLists, d3d12/ID3D12CommandQueue::ExecuteCommandLists, direct3d12.id3d12commandqueue_executecommandlists
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - d3d12.h
api_name:
 - ID3D12CommandQueue.ExecuteCommandLists
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D12CommandQueue::ExecuteCommandLists


## -description


Submits an array of command lists for execution.


## -parameters




### -param NumCommandLists [in]

The number of command lists to be executed.
          


### -param ppCommandLists [in]

The array of <a href="https://msdn.microsoft.com/1E0359CC-0F53-4C82-9F1A-092F6F72EE20">ID3D12CommandList</a> command lists to be executed.
          


## -returns



This method does not return a value.




## -remarks



The driver is free to patch the submitted command lists. It is the calling application’s responsibility to ensure that the graphics processing unit (GPU) is not currently reading the any of the submitted command lists from a previous execution.
        

Applications are encouraged to batch together command list executions to reduce fixed costs associated with submitted commands to the GPU.
        

<h3><a id="Runtime_validation"></a><a id="runtime_validation"></a><a id="RUNTIME_VALIDATION"></a>Runtime validation</h3>
Bundles can't be submitted to a command queue directly. If a bundle is passed to this method, the runtime will drop the call.  The runtime will also drop the call if the <a href="https://msdn.microsoft.com/EA9F00AD-8506-4F3C-871E-A51ED69005BB">Close</a> has not been called on any of the command lists.
          

The runtime will detect if the command allocators associated with the command lists have been reset after <a href="https://msdn.microsoft.com/EA9F00AD-8506-4F3C-871E-A51ED69005BB">Close</a> was called.  The runtime will drop the call and remove the device in this situation.
          

The runtime will drop the call and remove the device if the command queue fence indicates that a previous execution of any of the command lists has not yet completed.
          

The runtime will validate the "before" and "after" states of resource transition barriers inside of <b>ExecuteCommandLists</b>.  If the “before” state of a transition does not match up with the “after” state of a previous transition, then the runtime will drop the call and remove the device.
          

The runtime will validate the “before” and “after” states of queries used by the command lists.  If an error is detected, then the runtime will drop the call and remove the device.

<h3><a id="Debug_layer"></a><a id="debug_layer"></a><a id="DEBUG_LAYER"></a>Debug layer</h3>
The debug layer will issue errors for all cases where the runtime would drop the call.

The debug layer will issue an error if it detects that any resource referenced by the command lists, including queries, has been destroyed.
          


#### Examples

Renders a scene.


```cpp
// Pipeline objects.
D3D12_VIEWPORT m_viewport;
ComPtr<IDXGISwapChain3> m_swapChain;
ComPtr<ID3D11DeviceContext> m_d3d11DeviceContext;
ComPtr<ID3D11On12Device> m_d3d11On12Device;
ComPtr<ID3D12Device> m_d3d12Device;
ComPtr<IDWriteFactory> m_dWriteFactory;
ComPtr<ID2D1Factory3> m_d2dFactory;
ComPtr<ID2D1Device2> m_d2dDevice;
ComPtr<ID2D1DeviceContext2> m_d2dDeviceContext;
ComPtr<ID3D12Resource> m_renderTargets[FrameCount];
ComPtr<ID3D11Resource> m_wrappedBackBuffers[FrameCount];
ComPtr<ID2D1Bitmap1> m_d2dRenderTargets[FrameCount];
ComPtr<ID3D12CommandAllocator> m_commandAllocators[FrameCount];
ComPtr<ID3D12CommandQueue> m_commandQueue;
ComPtr<ID3D12RootSignature> m_rootSignature;
ComPtr<ID3D12DescriptorHeap> m_rtvHeap;
ComPtr<ID3D12PipelineState> m_pipelineState;
ComPtr<ID3D12GraphicsCommandList> m_commandList;
D3D12_RECT m_scissorRect;

```

```cpp
// Render the scene.
void D3D1211on12::OnRender()
{
    // Record all the commands we need to render the scene into the command list.
    PopulateCommandList();

    // Execute the command list.
    ID3D12CommandList* ppCommandLists[] = { m_commandList.Get() };
    m_commandQueue->ExecuteCommandLists(_countof(ppCommandLists), ppCommandLists);

    RenderUI();

    // Present the frame.
    ThrowIfFailed(m_swapChain->Present(1, 0));

    MoveToNextFrame();
}

```


Refer to the <a href="https://msdn.microsoft.com/C2323482-D06D-43B7-9BDE-BFB9A6A6B70D">Example Code in the D3D12 Reference</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/88A4E8BA-02B9-48A1-8E46-2D2560544539">ID3D12CommandQueue</a>
 

 

