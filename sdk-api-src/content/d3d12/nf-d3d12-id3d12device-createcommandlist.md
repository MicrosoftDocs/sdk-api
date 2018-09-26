---
UID: NF:d3d12.ID3D12Device.CreateCommandList
title: ID3D12Device::CreateCommandList
author: windows-sdk-content
description: Creates a command list.
old-location: direct3d12\id3d12device_createcommandlist.htm
tech.root: direct3d12
ms.assetid: 4C615D7D-6DBC-4EDA-8D72-271EC53047BF
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: CreateCommandList, CreateCommandList method, CreateCommandList method,ID3D12Device interface, ID3D12Device interface,CreateCommandList method, ID3D12Device.CreateCommandList, ID3D12Device::CreateCommandList, d3d12/ID3D12Device::CreateCommandList, direct3d12.id3d12device_createcommandlist
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12Device::CreateCommandList


## -description


Creates a command list.
        


## -parameters




### -param nodeMask [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

For single GPU operation, set this to zero. If there are multiple GPU nodes, set a bit to identify the node (the  device's physical adapter) for which to create the command list.
            Each bit in the mask corresponds to a single node.
            Only 1 bit must be set.
          Refer to <a href="https://msdn.microsoft.com/CC4C6594-D48F-40C1-93EE-9F98532BC038">Multi-Adapter</a>.


### -param type [in]

Type: <b><a href="https://msdn.microsoft.com/28BC70FF-6818-4B8D-9DE4-8316AB2FB288">D3D12_COMMAND_LIST_TYPE</a></b>

A <a href="https://msdn.microsoft.com/28BC70FF-6818-4B8D-9DE4-8316AB2FB288">D3D12_COMMAND_LIST_TYPE</a>-typed value that specifies the type of command list to create.
          


### -param pCommandAllocator [in]

Type: <b><a href="https://msdn.microsoft.com/ADC494E6-1698-415D-90C5-F99FCD4C5309">ID3D12CommandAllocator</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/ADC494E6-1698-415D-90C5-F99FCD4C5309">ID3D12CommandAllocator</a> object that the device creates command lists from.
          


### -param pInitialState [in, optional]

Type: <b><a href="https://msdn.microsoft.com/DD922194-8AD2-4ADF-9AC2-46C903C56AE6">ID3D12PipelineState</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/DD922194-8AD2-4ADF-9AC2-46C903C56AE6">ID3D12PipelineState</a> object that contains the initial pipeline state for the command list.  This is optional and can be NULL.  If NULL, the runtime sets a dummy initial pipeline state so that drivers don't have to deal with undefined state.  The overhead for this is low, particularly for a command list, for which the overall cost of recording the command list likely dwarfs the cost of one initial state setting.  So there is little cost in  not setting the initial pipeline state parameter if it isn't convenient.  

For bundles on the other hand, it might make more sense to try to set the initial state parameter since bundles are likely smaller overall and can be reused frequently.


### -param riid

Type: <b>REFIID</b>

The globally unique identifier (<b>GUID</b>) for the command list interface.
            The <b>REFIID</b>, or <b>GUID</b>, of the interface to the command list can be obtained by using the __uuidof() macro.
            For example, __uuidof(<a href="https://msdn.microsoft.com/1E0359CC-0F53-4C82-9F1A-092F6F72EE20">ID3D12CommandList</a>) will get the <b>GUID</b> of the interface to a command list.
          


### -param ppCommandList [out]

Type: <b>void**</b>

A pointer to a memory block that receives a pointer to the
            <a href="https://msdn.microsoft.com/1E0359CC-0F53-4C82-9F1A-092F6F72EE20">ID3D12CommandList</a>or
            <a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a>interface for the command list.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns <b>E_OUTOFMEMORY</b> if there is insufficient memory to create the command list.
              See <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a> for other possible return values.
            




## -remarks



The device creates command lists from the command allocator.
      


#### Examples

The <a href="https://msdn.microsoft.com/4C4475D4-534F-484F-8D60-9ACEA09AC109">D3D12Bundles</a> sample uses <b>ID3D12Device::CreateCommandList</b> as follows.

Create the pipeline objects.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>ComPtr&lt;ID3D12CommandAllocator&gt; m_commandAllocator;
ComPtr&lt;ID3D12GraphicsCommandList&gt; m_commandList;
</pre>
</td>
</tr>
</table></span></div>
Create a command allocator.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>ThrowIfFailed(m_device-&gt;CreateCommandAllocator(D3D12_COMMAND_LIST_TYPE_DIRECT, IID_PPV_ARGS(&amp;m_commandAllocator)));
</pre>
</td>
</tr>
</table></span></div>
Creating the direct command list.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>ThrowIfFailed(m_device-&gt;CreateCommandList(0, D3D12_COMMAND_LIST_TYPE_DIRECT, m_commandAllocator.Get(), nullptr, IID_PPV_ARGS(&amp;m_commandList)));
</pre>
</td>
</tr>
</table></span></div>
Refer to the <a href="https://msdn.microsoft.com/C2323482-D06D-43B7-9BDE-BFB9A6A6B70D">Example Code in the D3D12 Reference</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>



<a href="https://msdn.microsoft.com/36726FB6-09DE-4723-A60E-75FCE55F2E35">ID3D12GraphicsCommandList::Reset</a>
 

 

