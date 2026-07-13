---
UID: NS:d3d12.D3D12_CPU_DESCRIPTOR_HANDLE
title: D3D12_CPU_DESCRIPTOR_HANDLE (d3d12.h)
description: Describes a CPU descriptor handle.
helpviewer_keywords: ["D3D12_CPU_DESCRIPTOR_HANDLE","D3D12_CPU_DESCRIPTOR_HANDLE structure","d3d12/D3D12_CPU_DESCRIPTOR_HANDLE","direct3d12.d3d12_cpu_descriptor_handle"]
old-location: direct3d12\d3d12_cpu_descriptor_handle.htm
tech.root: direct3d12
ms.assetid: 92451E4C-5E70-4015-8760-3F75066A44FD
ms.date: 12/05/2018
ms.keywords: D3D12_CPU_DESCRIPTOR_HANDLE, D3D12_CPU_DESCRIPTOR_HANDLE structure, d3d12/D3D12_CPU_DESCRIPTOR_HANDLE, direct3d12.d3d12_cpu_descriptor_handle
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
targetos: Windows
req.typenames: D3D12_CPU_DESCRIPTOR_HANDLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_CPU_DESCRIPTOR_HANDLE
 - d3d12/D3D12_CPU_DESCRIPTOR_HANDLE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_CPU_DESCRIPTOR_HANDLE
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
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart">ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart</a>
</li>
</ul>
This structure is passed into the following methods:
        

<ul>
<li>
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors">ID3D12Device::CopyDescriptors</a>
</li>
<li>
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple">ID3D12Device::CopyDescriptorsSimple</a>
</li>
<li>
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview">ID3D12Device::CreateConstantBufferView</a>
</li>
<li>
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview">ID3D12Device::CreateShaderResourceView</a>
</li>
<li>
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview">ID3D12Device::CreateUnorderedAccessView</a>
</li>
<li>
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrendertargetview">ID3D12Device::CreateRenderTargetView</a>
</li>
<li>
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createdepthstencilview">ID3D12Device::CreateDepthStencilView</a>
</li>
<li>
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createsampler">ID3D12Device::CreateSampler</a>
</li>
<li>
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview">ID3D12GraphicsCommandList::ClearDepthStencilView</a>
</li>
<li>
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview">ID3D12GraphicsCommandList::ClearRenderTargetView</a>
</li>
<li>
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint">ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint</a>
</li>
<li>
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat">ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat</a>
</li>
<li>
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets">ID3D12GraphicsCommandList::OMSetRenderTargets</a>
</li>
</ul>

To get the handle increment size use <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize">ID3D12Device.GetDescriptorHandleIncrementSize</a>

## -see-also

<a href="/windows/desktop/direct3d12/cd3dx12-cpu-descriptor-handle">CD3DX12_CPU_DESCRIPTOR_HANDLE</a>
<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize">ID3D12Device.GetDescriptorHandleIncrementSize</a>


<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>