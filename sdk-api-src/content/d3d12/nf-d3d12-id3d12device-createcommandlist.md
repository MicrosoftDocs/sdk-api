---
UID: NF:d3d12.ID3D12Device.CreateCommandList
title: ID3D12Device::CreateCommandList (d3d12.h)
author: windows-sdk-content
description: Creates a command list.
old-location: direct3d12\id3d12device_createcommandlist.htm
tech.root: direct3d12
ms.assetid: 4C615D7D-6DBC-4EDA-8D72-271EC53047BF
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateCommandList, CreateCommandList method, CreateCommandList method,ID3D12Device interface, ID3D12Device interface,CreateCommandList method, ID3D12Device.CreateCommandList, ID3D12Device::CreateCommandList, d3d12/ID3D12Device::CreateCommandList, direct3d12.id3d12device_createcommandlist
ms.topic: method
f1_keywords: 
 - "d3d12/ID3D12Device.CreateCommandList"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12Device.CreateCommandList
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12Device::CreateCommandList


## -description


Creates a command list.
        


## -parameters




### -param nodeMask [in]

Type: <b><a href="/windows/win32/WinProg/windows-data-types">UINT</a></b>

For single GPU operation, set this to zero. If there are multiple GPU nodes, set a bit to identify the node (the  device's physical adapter) for which to create the command list.
            Each bit in the mask corresponds to a single node.
            Only 1 bit must be set.
          Refer to <a href="/windows/win32/direct3d12/multi-engine">Multi-adapter systems</a>.


### -param type [in]

Type: <b><a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type">D3D12_COMMAND_LIST_TYPE</a></b>

A <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type">D3D12_COMMAND_LIST_TYPE</a>-typed value that specifies the type of command list to create.
          


### -param pCommandAllocator [in]

Type: <b><a href="/windows/win32/api/d3d12/nn-d3d12-id3d12commandallocator">ID3D12CommandAllocator</a>*</b>

A pointer to the <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12commandallocator">ID3D12CommandAllocator</a> object that the device creates command lists from.
          


### -param pInitialState [in, optional]

Type: <b><a href="/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinestate">ID3D12PipelineState</a>*</b>

A pointer to the <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinestate">ID3D12PipelineState</a> object that contains the initial pipeline state for the command list.  This is optional and can be NULL.  If NULL, the runtime sets a dummy initial pipeline state so that drivers don't have to deal with undefined state.  The overhead for this is low, particularly for a command list, for which the overall cost of recording the command list likely dwarfs the cost of one initial state setting.  So there is little cost in  not setting the initial pipeline state parameter if it isn't convenient.  

For bundles on the other hand, it might make more sense to try to set the initial state parameter since bundles are likely smaller overall and can be reused frequently.


### -param riid

Type: <b>REFIID</b>

The globally unique identifier (<b>GUID</b>) for the command list interface.
            The <b>REFIID</b>, or <b>GUID</b>, of the interface to the command list can be obtained by using the __uuidof() macro.
            For example, __uuidof(<a href="/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist">ID3D12CommandList</a>) will get the <b>GUID</b> of the interface to a command list.
          


### -param ppCommandList [out]

Type: <b>void**</b>

A pointer to a memory block that receives a pointer to the
            <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist">ID3D12CommandList</a>or
            <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist">ID3D12GraphicsCommandList</a>interface for the command list.
          


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/win32/legacy/hh437604(v=vs.85)">HRESULT</a></b>

This method returns <b>E_OUTOFMEMORY</b> if there is insufficient memory to create the command list.
              See <a href="/windows/win32/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a> for other possible return values.
            




## -remarks



The device creates command lists from the command allocator.
      


#### Examples

The <a href="/windows/win32/direct3d12/working-samples">D3D12Bundles</a> sample uses <b>ID3D12Device::CreateCommandList</b> as follows.

Create the pipeline objects.


```cpp
ComPtr<ID3D12CommandAllocator> m_commandAllocator;
ComPtr<ID3D12GraphicsCommandList> m_commandList;

```


Create a command allocator.


```cpp
ThrowIfFailed(m_device->CreateCommandAllocator(D3D12_COMMAND_LIST_TYPE_DIRECT, IID_PPV_ARGS(&m_commandAllocator)));

```


Creating the direct command list.


```cpp
ThrowIfFailed(m_device->CreateCommandList(0, D3D12_COMMAND_LIST_TYPE_DIRECT, m_commandAllocator.Get(), nullptr, IID_PPV_ARGS(&m_commandList)));

```


Refer to the <a href="/windows/win32/direct3d12/notes-on-example-code">Example Code in the D3D12 Reference</a>.

<div class="code"></div>



## -see-also




<a href="/windows/win32/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>



<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset">ID3D12GraphicsCommandList::Reset</a>
 

 

