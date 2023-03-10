---
UID: NF:d3d12.ID3D12Device.CreateShaderResourceView
title: ID3D12Device::CreateShaderResourceView (d3d12.h)
description: Creates a shader-resource view for accessing data in a resource. (ID3D12Device.CreateShaderResourceView)
helpviewer_keywords: ["CreateShaderResourceView","CreateShaderResourceView method","CreateShaderResourceView method","ID3D12Device interface","ID3D12Device interface","CreateShaderResourceView method","ID3D12Device.CreateShaderResourceView","ID3D12Device::CreateShaderResourceView","d3d12/ID3D12Device::CreateShaderResourceView","direct3d12.id3d12device_createshaderresourceview"]
old-location: direct3d12\id3d12device_createshaderresourceview.htm
tech.root: direct3d12
ms.assetid: 4FD7082D-2DA9-469E-BA74-6735D407D5FE
ms.date: 12/05/2018
ms.keywords: CreateShaderResourceView, CreateShaderResourceView method, CreateShaderResourceView method,ID3D12Device interface, ID3D12Device interface,CreateShaderResourceView method, ID3D12Device.CreateShaderResourceView, ID3D12Device::CreateShaderResourceView, d3d12/ID3D12Device::CreateShaderResourceView, direct3d12.id3d12device_createshaderresourceview
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12Device::CreateShaderResourceView
 - d3d12/ID3D12Device::CreateShaderResourceView
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12Device.CreateShaderResourceView
---

# ID3D12Device::CreateShaderResourceView


## -description

Creates a shader-resource view for accessing data in a resource.

## -parameters

### -param pResource [in, optional]

Type: <b><a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a>*</b>

A pointer to the <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a> object that represents the shader resource.

At least one of <i>pResource</i> or <i>pDesc</i>  must be provided.
A null <i>pResource</i> is used to initialize a null descriptor, which guarantees D3D11-like null binding behavior (reading 0s, writes are discarded), but must have a valid <i>pDesc</i> in order to determine the descriptor type.

### -param pDesc [in, optional]

Type: <b>const <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc">D3D12_SHADER_RESOURCE_VIEW_DESC</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc">D3D12_SHADER_RESOURCE_VIEW_DESC</a> structure that describes the shader-resource view. 

A null <i>pDesc</i> is used to initialize a default descriptor, if possible. This behavior is identical to the D3D11 null descriptor behavior, where defaults are filled in. This behavior inherits the resource format and dimension (if not typeless) and for buffers SRVs target a full buffer and are typed (not raw or structured), and for textures SRVs target a full texture, all mips and all array slices. Not all resources support null descriptor initialization.

### -param DestDescriptor [in]

Type: <b><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle">D3D12_CPU_DESCRIPTOR_HANDLE</a></b>

Describes the CPU descriptor handle that represents the shader-resource view. This handle can be created in a shader-visible or non-shader-visible descriptor heap.

## -remarks

<h3><a id="Processing_YUV_4_2_0_video_formats"></a><a id="processing_yuv_4_2_0_video_formats"></a><a id="PROCESSING_YUV_4_2_0_VIDEO_FORMATS"></a>Processing YUV 4:2:0 video formats</h3>
An app must map the luma (Y) plane separately from the chroma (UV) planes. Developers do this by calling <b>CreateShaderResourceView</b> twice for the same texture and passing in 1-channel and 2-channel formats. Passing in a 1-channel format compatible with the Y plane maps only the Y plane. Passing in a 2-channel format compatible with the UV planes (together) maps only the U and V planes as a single resource view.

YUV 4:2:0 formats are listed in <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>.


#### Examples

The <a href="/windows/desktop/direct3d12/working-samples">D3D12nBodyGravity</a> sample uses <b>ID3D12Device::CreateShaderResourceView</b> as follows:
        

Describe and create two shader resource views based on one description.


```cpp
D3D12_SHADER_RESOURCE_VIEW_DESC srvDesc = {};
srvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
srvDesc.Format = DXGI_FORMAT_UNKNOWN;
srvDesc.ViewDimension = D3D12_SRV_DIMENSION_BUFFER;
srvDesc.Buffer.FirstElement = 0;
srvDesc.Buffer.NumElements = ParticleCount;
srvDesc.Buffer.StructureByteStride = sizeof(Particle);
srvDesc.Buffer.Flags = D3D12_BUFFER_SRV_FLAG_NONE;

CD3DX12_CPU_DESCRIPTOR_HANDLE srvHandle0(m_srvUavHeap->GetCPUDescriptorHandleForHeapStart(), SrvParticlePosVelo0 + index, m_srvUavDescriptorSize);
CD3DX12_CPU_DESCRIPTOR_HANDLE srvHandle1(m_srvUavHeap->GetCPUDescriptorHandleForHeapStart(), SrvParticlePosVelo1 + index, m_srvUavDescriptorSize);
m_device->CreateShaderResourceView(m_particleBuffer0[index].Get(), &srvDesc, srvHandle0);
m_device->CreateShaderResourceView(m_particleBuffer1[index].Get(), &srvDesc, srvHandle1);

```


Refer to the <a href="/windows/desktop/direct3d12/notes-on-example-code">Example Code in the D3D12 Reference</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>
