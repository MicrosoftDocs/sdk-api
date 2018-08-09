---
UID: NF:d3d12.ID3D12Device.CreateCommandQueue
title: ID3D12Device::CreateCommandQueue
author: windows-sdk-content
description: Creates a command queue.
old-location: direct3d12\id3d12device_createcommandqueue.htm
old-project: direct3d12
ms.assetid: 556D068C-9939-4B42-AFC2-4EBB2D7B553B
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: CreateCommandQueue, CreateCommandQueue method, CreateCommandQueue method,ID3D12Device interface, ID3D12Device interface,CreateCommandQueue method, ID3D12Device.CreateCommandQueue, ID3D12Device::CreateCommandQueue, d3d12/ID3D12Device::CreateCommandQueue, direct3d12.id3d12device_createcommandqueue
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
 - D3D12.dll
api_name:
 - ID3D12Device.CreateCommandQueue
product: Windows
targetos: Windows
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
---

# ID3D12Device::CreateCommandQueue


## -description


Creates a command queue.


## -parameters




### -param pDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/8C43C45B-0A7B-4336-B546-1E6F13D153F3">D3D12_COMMAND_QUEUE_DESC</a>*</b>

Specifies a D3D12_COMMAND_QUEUE_DESC that describes the command queue.
          


### -param riid

Type: <b><b>REFIID</b></b>

The globally unique identifier (GUID) for the command queue interface. See remarks.  An input parameter.
          


### -param ppCommandQueue [out]

Type: <b><b>void</b>**</b>

A pointer to a memory block that receives a pointer to the <a href="https://msdn.microsoft.com/88A4E8BA-02B9-48A1-8E46-2D2560544539">ID3D12CommandQueue</a> interface for the command queue.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns <b>E_OUTOFMEMORY</b> if there is insufficient memory to create the command queue.
            See <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a> for other possible return values.
          




## -remarks



The <b>REFIID</b>, or <b>GUID</b>, of the interface to the command queue can be obtained by using the __uuidof() macro. For example, __uuidof(ID3D12CommandQueue) will get the <b>GUID</b> of the interface to a command queue.
      


#### Examples

The <a href="https://msdn.microsoft.com/4C4475D4-534F-484F-8D60-9ACEA09AC109">D3D12HelloTriangle</a> sample uses <b>ID3D12Device::CreateCommandQueue</b> as follows:
        

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>D3D12_COMMAND_QUEUE_DESC queueDesc = {};
queueDesc.Flags = D3D12_COMMAND_QUEUE_FLAG_NONE;
queueDesc.Type = D3D12_COMMAND_LIST_TYPE_DIRECT;

ThrowIfFailed(m_device-&gt;CreateCommandQueue(&amp;queueDesc, IID_PPV_ARGS(&amp;m_commandQueue)));
</pre>
</td>
</tr>
</table></span></div>
Refer to the <a href="https://msdn.microsoft.com/C2323482-D06D-43B7-9BDE-BFB9A6A6B70D">Example Code in the D3D12 Reference</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>
 

 

