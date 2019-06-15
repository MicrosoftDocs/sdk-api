---
UID: NF:d3d12.ID3D12Device.CreateCommandQueue
title: ID3D12Device::CreateCommandQueue (d3d12.h)
author: windows-sdk-content
description: Creates a command queue.
old-location: direct3d12\id3d12device_createcommandqueue.htm
tech.root: direct3d12
ms.assetid: 556D068C-9939-4B42-AFC2-4EBB2D7B553B
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateCommandQueue, CreateCommandQueue method, CreateCommandQueue method,ID3D12Device interface, ID3D12Device interface,CreateCommandQueue method, ID3D12Device.CreateCommandQueue, ID3D12Device::CreateCommandQueue, d3d12/ID3D12Device::CreateCommandQueue, direct3d12.id3d12device_createcommandqueue
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
 - ID3D12Device.CreateCommandQueue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12Device::CreateCommandQueue


## -description


Creates a command queue.


## -parameters




### -param pDesc [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_queue_desc">D3D12_COMMAND_QUEUE_DESC</a>*</b>

Specifies a D3D12_COMMAND_QUEUE_DESC that describes the command queue.
          


### -param riid

Type: <b><b>REFIID</b></b>

The globally unique identifier (GUID) for the command queue interface. See remarks.  An input parameter.
          


### -param ppCommandQueue [out]

Type: <b><b>void</b>**</b>

A pointer to a memory block that receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue">ID3D12CommandQueue</a> interface for the command queue.
          


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

This method returns <b>E_OUTOFMEMORY</b> if there is insufficient memory to create the command queue.
            See <a href="https://docs.microsoft.com/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a> for other possible return values.
          




## -remarks



The <b>REFIID</b>, or <b>GUID</b>, of the interface to the command queue can be obtained by using the __uuidof() macro. For example, __uuidof(ID3D12CommandQueue) will get the <b>GUID</b> of the interface to a command queue.
      


#### Examples

The <a href="https://docs.microsoft.com/windows/desktop/direct3d12/working-samples">D3D12HelloTriangle</a> sample uses <b>ID3D12Device::CreateCommandQueue</b> as follows:
        


```cpp
D3D12_COMMAND_QUEUE_DESC queueDesc = {};
queueDesc.Flags = D3D12_COMMAND_QUEUE_FLAG_NONE;
queueDesc.Type = D3D12_COMMAND_LIST_TYPE_DIRECT;

ThrowIfFailed(m_device->CreateCommandQueue(&queueDesc, IID_PPV_ARGS(&m_commandQueue)));

```


Refer to the <a href="https://docs.microsoft.com/windows/desktop/direct3d12/notes-on-example-code">Example Code in the D3D12 Reference</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>
 

 

