---
UID: NS:d3d12.D3D12_CPU_DESCRIPTOR_HANDLE
title: D3D12_CPU_DESCRIPTOR_HANDLE (d3d12.h)
author: windows-sdk-content
description: Describes a CPU descriptor handle.
old-location: direct3d12\d3d12_cpu_descriptor_handle.htm
tech.root: direct3d12
ms.assetid: 92451E4C-5E70-4015-8760-3F75066A44FD
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D12_CPU_DESCRIPTOR_HANDLE, D3D12_CPU_DESCRIPTOR_HANDLE structure, d3d12/D3D12_CPU_DESCRIPTOR_HANDLE, direct3d12.d3d12_cpu_descriptor_handle
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_CPU_DESCRIPTOR_HANDLE
product: Windows
targetos: Windows
req.typenames: D3D12_CPU_DESCRIPTOR_HANDLE
req.redist: 
ms.custom: 19H1
---

# D3D12_CPU_DESCRIPTOR_HANDLE structure


## -description


Describes a CPU descriptor handle.
        


## -struct-fields




### -field ptr

The address of  the descriptor.
          


## -remarks



This structure is returned by the following methods:
        

<ul>
<li>
<a href="https://msdn.microsoft.com/80C41537-1579-4166-A7F9-FB2478ECDE77">ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart</a>
</li>
</ul>
This structure is passed into the following methods:
        

<ul>
<li>
<a href="https://msdn.microsoft.com/F995EF34-74FF-4FCA-A018-E2F48DF92450">ID3D12Device::CopyDescriptors</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6DA1FCDA-042C-4727-9814-B8F57E14CD51">ID3D12Device::CopyDescriptorsSimple</a>
</li>
<li>
<a href="https://msdn.microsoft.com/13251F82-4AE9-4234-A0C8-0E666F8A1856">ID3D12Device::CreateConstantBufferView</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4FD7082D-2DA9-469E-BA74-6735D407D5FE">ID3D12Device::CreateShaderResourceView</a>
</li>
<li>
<a href="https://msdn.microsoft.com/E834E469-2958-44A9-978F-F42D6BB6B1DC">ID3D12Device::CreateUnorderedAccessView</a>
</li>
<li>
<a href="https://msdn.microsoft.com/B5BFAE54-4FAC-47E5-A7F1-3F9E78FED3B4">ID3D12Device::CreateRenderTargetView</a>
</li>
<li>
<a href="https://msdn.microsoft.com/57C0CA35-CFBE-4D79-B8D7-BD01CEBEA144">ID3D12Device::CreateDepthStencilView</a>
</li>
<li>
<a href="https://msdn.microsoft.com/453B2D3D-843E-4DB0-BC47-59BD9C78BFD6">ID3D12Device::CreateSampler</a>
</li>
<li>
<a href="https://msdn.microsoft.com/EF56EA6C-00DB-4231-B67D-B99811F51246">ID3D12GraphicsCommandList::ClearDepthStencilView</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5AB13E36-A189-41B4-AEF8-B5C5831655DB">ID3D12GraphicsCommandList::ClearRenderTargetView</a>
</li>
<li>
<a href="https://msdn.microsoft.com/A048BF0C-9141-4DDF-91F9-B53464033A44">ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6A19F429-D7B2-4A71-8904-31BFA1FD10C6">ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat</a>
</li>
<li>
<a href="https://msdn.microsoft.com/FE565AA2-FA34-4824-870E-9C4C7C19C93C">ID3D12GraphicsCommandList::OMSetRenderTargets</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/91736069-7D13-47B0-B78C-0F6F104F97EB">CD3DX12_CPU_DESCRIPTOR_HANDLE</a>



<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

