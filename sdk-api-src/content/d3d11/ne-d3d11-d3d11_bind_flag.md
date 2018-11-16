---
UID: NE:d3d11.D3D11_BIND_FLAG
title: D3D11_BIND_FLAG
author: windows-sdk-content
description: Identifies how to bind a resource to the pipeline.
old-location: direct3d11\d3d11_bind_flag.htm
tech.root: direct3d11
ms.assetid: 4ffa1714-bd85-4d5a-930d-20526f46e4b9
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: D3D11_BIND_CONSTANT_BUFFER, D3D11_BIND_DECODER, D3D11_BIND_DEPTH_STENCIL, D3D11_BIND_FLAG, D3D11_BIND_FLAG enumeration [Direct3D 11], D3D11_BIND_INDEX_BUFFER, D3D11_BIND_RENDER_TARGET, D3D11_BIND_SHADER_RESOURCE, D3D11_BIND_STREAM_OUTPUT, D3D11_BIND_UNORDERED_ACCESS, D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_VIDEO_ENCODER, d3d11/D3D11_BIND_CONSTANT_BUFFER, d3d11/D3D11_BIND_DECODER, d3d11/D3D11_BIND_DEPTH_STENCIL, d3d11/D3D11_BIND_FLAG, d3d11/D3D11_BIND_INDEX_BUFFER, d3d11/D3D11_BIND_RENDER_TARGET, d3d11/D3D11_BIND_SHADER_RESOURCE, d3d11/D3D11_BIND_STREAM_OUTPUT, d3d11/D3D11_BIND_UNORDERED_ACCESS, d3d11/D3D11_BIND_VERTEX_BUFFER, d3d11/D3D11_BIND_VIDEO_ENCODER, direct3d11.d3d11_bind_flag, f5054b36-4a79-15b3-51ed-9c008399e353
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d3d11.h
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
 - D3D11.h
api_name:
 - D3D11_BIND_FLAG
product: Windows
targetos: Windows
req.typenames: D3D11_BIND_FLAG
req.redist: 
---

# D3D11_BIND_FLAG enumeration


## -description


Identifies how to bind a resource to the pipeline.


## -enum-fields




### -field D3D11_BIND_VERTEX_BUFFER

Bind a buffer as a vertex buffer to the input-assembler stage.


### -field D3D11_BIND_INDEX_BUFFER

Bind a buffer as an index buffer to the input-assembler stage.


### -field D3D11_BIND_CONSTANT_BUFFER

Bind a buffer as a constant buffer to a shader stage; this flag may NOT be combined with any other bind flag.


### -field D3D11_BIND_SHADER_RESOURCE

Bind a buffer or texture to a shader stage; this flag cannot be used with the <a href="https://msdn.microsoft.com/916b00bd-2711-4ebd-a36d-d75b3a59a528">D3D11_MAP_WRITE_NO_OVERWRITE</a> flag.

<div class="alert"><b>Note</b>  The Direct3D 11.1 runtime, which is available starting with Windows 8, enables  mapping dynamic constant buffers and shader resource views (SRVs) of dynamic buffers with <a href="https://msdn.microsoft.com/en-us/library/Ff476181(v=VS.85).aspx">D3D11_MAP_WRITE_NO_OVERWRITE</a>.  The Direct3D 11 and earlier runtimes limited mapping to vertex or index buffers. To determine if a Direct3D device supports these features, call <a href="https://msdn.microsoft.com/7edf2ffd-908a-4cf8-9ac6-8fd14d7a0ea1">ID3D11Device::CheckFeatureSupport</a> with <a href="https://msdn.microsoft.com/en-us/library/Ff476124(v=VS.85).aspx">D3D11_FEATURE_D3D11_OPTIONS</a>. <b>CheckFeatureSupport</b> fills members of a <a href="https://msdn.microsoft.com/02A3B423-75AB-4F44-BEBE-B8039EF384DC">D3D11_FEATURE_DATA_D3D11_OPTIONS</a> structure with the device's features. The relevant members here are <b>MapNoOverwriteOnDynamicConstantBuffer</b> and <b>MapNoOverwriteOnDynamicBufferSRV</b>.</div>
<div> </div>

### -field D3D11_BIND_STREAM_OUTPUT

Bind an output buffer for the stream-output stage.


### -field D3D11_BIND_RENDER_TARGET

Bind a texture as a render target for the output-merger stage.


### -field D3D11_BIND_DEPTH_STENCIL

Bind a texture as a depth-stencil target for the output-merger stage.


### -field D3D11_BIND_UNORDERED_ACCESS

Bind an <a href="https://msdn.microsoft.com/597cc12f-dd0e-4603-b670-3f584f25e192">unordered access</a> resource.


### -field D3D11_BIND_DECODER

Set this flag to indicate that a  <a href="https://msdn.microsoft.com/d745093e-2d51-4d45-a88a-caa0ca58b2ba">2D texture</a> is used to receive output from the decoder API. The common way to create resources for a decoder output is by calling the  <a href="https://msdn.microsoft.com/69950ce7-9c8e-4f00-860d-e118e2bbc81a">ID3D11Device::CreateTexture2D</a> method to create an array of 2D  textures. However, you cannot use texture arrays that are created with this flag in calls to <a href="https://msdn.microsoft.com/a8e3cda3-76f9-48c3-9e0c-e530f95fe8b8">ID3D11Device::CreateShaderResourceView</a>.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.1.


### -field D3D11_BIND_VIDEO_ENCODER

Set this flag to indicate that a  <a href="https://msdn.microsoft.com/d745093e-2d51-4d45-a88a-caa0ca58b2ba">2D texture</a> is used to receive input from the video encoder API. The common way to create resources for a video encoder is by calling the  <a href="https://msdn.microsoft.com/69950ce7-9c8e-4f00-860d-e118e2bbc81a">ID3D11Device::CreateTexture2D</a> method to create an array of 2D  textures. However, you cannot use texture arrays that are created with this flag in calls to <a href="https://msdn.microsoft.com/a8e3cda3-76f9-48c3-9e0c-e530f95fe8b8">ID3D11Device::CreateShaderResourceView</a>.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.1.


## -remarks



In general, binding flags can be combined using a logical OR (except the constant-buffer flag); however, you should use a single flag to allow the device to optimize the resource usage.

This enumeration is used by a:

<ul>
<li>
<a href="https://msdn.microsoft.com/a5e470bb-011b-4a2a-96d6-cbf76fe12638">Buffer description</a> when creating a buffer.</li>
<li>Texture description when creating a texture (see <a href="https://msdn.microsoft.com/8523d7b1-856e-4ec8-9286-4f1f2730a428">D3D11_TEXTURE1D_DESC</a> or <a href="https://msdn.microsoft.com/90c0f877-daf5-4b3d-9846-5bb414c55461">D3D11_TEXTURE2D_DESC</a> or <a href="https://msdn.microsoft.com/b3fd4280-c967-4eed-8a10-97f0c7ef56ac">D3D11_TEXTURE3D_DESC</a>).</li>
</ul>
A shader-resource buffer is NOT a constant buffer; rather, it is a texture or buffer resource that is bound to a shader, that contains texture or buffer data (it is not limited to a single element type in the buffer). A shader-resource buffer is created with the D3D11_BIND_SHADER_RESOURCE flag and is bound to the pipeline using one of these APIs: <a href="https://msdn.microsoft.com/f08af865-ec0a-4fc7-af59-004b6956be00">ID3D11DeviceContext::GSSetShaderResources</a>, <a href="https://msdn.microsoft.com/acccbde4-68d0-4c76-bf77-643884af1bbe">ID3D11DeviceContext::PSSetShaderResources</a>, or <a href="https://msdn.microsoft.com/f5dbd212-6896-41b1-b61b-f1c1a690a195">ID3D11DeviceContext::VSSetShaderResources</a>. Furthermore, a shader-resource buffer cannot use the <a href="https://msdn.microsoft.com/916b00bd-2711-4ebd-a36d-d75b3a59a528">D3D11_MAP_WRITE_NO_OVERWRITE</a> flag.

<div class="alert"><b>Note</b>  The Direct3D 11.1 runtime, which is available starting with Windows 8, enables  mapping dynamic constant buffers and shader resource views (SRVs) of dynamic buffers with <a href="https://msdn.microsoft.com/en-us/library/Ff476181(v=VS.85).aspx">D3D11_MAP_WRITE_NO_OVERWRITE</a>.  The Direct3D 11 and earlier runtimes limited mapping to vertex or index buffers. To determine if a Direct3D device supports these features, call <a href="https://msdn.microsoft.com/7edf2ffd-908a-4cf8-9ac6-8fd14d7a0ea1">ID3D11Device::CheckFeatureSupport</a> with <a href="https://msdn.microsoft.com/en-us/library/Ff476124(v=VS.85).aspx">D3D11_FEATURE_D3D11_OPTIONS</a>. <b>CheckFeatureSupport</b> fills members of a <a href="https://msdn.microsoft.com/02A3B423-75AB-4F44-BEBE-B8039EF384DC">D3D11_FEATURE_DATA_D3D11_OPTIONS</a> structure with the device's features. The relevant members here are <b>MapNoOverwriteOnDynamicConstantBuffer</b> and <b>MapNoOverwriteOnDynamicBufferSRV</b>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/b547819b-7006-40b5-84a4-adf198048051">Resource Enumerations</a>
 

 

