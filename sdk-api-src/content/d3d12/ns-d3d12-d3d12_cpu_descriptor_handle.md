---
UID: NS:d3d12.D3D12_CPU_DESCRIPTOR_HANDLE
title: D3D12_CPU_DESCRIPTOR_HANDLE
author: windows-sdk-content
description: Describes a CPU descriptor handle.
old-location: direct3d12\d3d12_cpu_descriptor_handle.htm
tech.root: direct3d12
ms.assetid: 92451E4C-5E70-4015-8760-3F75066A44FD
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: D3D12_CPU_DESCRIPTOR_HANDLE, D3D12_CPU_DESCRIPTOR_HANDLE structure, d3d12/D3D12_CPU_DESCRIPTOR_HANDLE, direct3d12.d3d12_cpu_descriptor_handle
ms.prod: windows
ms.technology: windows-sdk
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
<a href="https://msdn.microsoft.com/en-us/library/Dn899174(v=VS.85).aspx">ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart</a>
</li>
</ul>
This structure is passed into the following methods:
        

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn899176(v=VS.85).aspx">ID3D12Device::CopyDescriptors</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn899177(v=VS.85).aspx">ID3D12Device::CopyDescriptorsSimple</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn788659(v=VS.85).aspx">ID3D12Device::CreateConstantBufferView</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn788672(v=VS.85).aspx">ID3D12Device::CreateShaderResourceView</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn788674(v=VS.85).aspx">ID3D12Device::CreateUnorderedAccessView</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn788668(v=VS.85).aspx">ID3D12Device::CreateRenderTargetView</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn788661(v=VS.85).aspx">ID3D12Device::CreateDepthStencilView</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn788671(v=VS.85).aspx">ID3D12Device::CreateSampler</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn903840(v=VS.85).aspx">ID3D12GraphicsCommandList::ClearDepthStencilView</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn903842(v=VS.85).aspx">ID3D12GraphicsCommandList::ClearRenderTargetView</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn903853(v=VS.85).aspx">ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn903849(v=VS.85).aspx">ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn986884(v=VS.85).aspx">ID3D12GraphicsCommandList::OMSetRenderTargets</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt186565(v=VS.85).aspx">CD3DX12_CPU_DESCRIPTOR_HANDLE</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn770459(v=VS.85).aspx">Core Structures</a>
 

 

