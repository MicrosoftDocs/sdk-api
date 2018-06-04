---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# D3D10_BIND_FLAG enumeration


## -description


Identifies how to bind a resource to the pipeline.


## -enum-fields




### -field D3D10_BIND_VERTEX_BUFFER

Bind a buffer as a <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">vertex buffer</a> to the <a href="https://msdn.microsoft.com/71141a5e-2d79-4b02-8370-c0cbc8618908">input-assembler stage</a>.


### -field D3D10_BIND_INDEX_BUFFER

Bind a buffer as an <a href="https://msdn.microsoft.com/library/windows/hardware/jj124414">index buffer</a> to the <a href="https://msdn.microsoft.com/71141a5e-2d79-4b02-8370-c0cbc8618908">input-assembler stage</a>.


### -field D3D10_BIND_CONSTANT_BUFFER

Bind a buffer as a <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">constant buffer</a> to a <a href="direct3d11.d3d10_graphics_programming_guide_shader_stages">shader stage</a>; this flag may NOT be combined with any other bind flag.


### -field D3D10_BIND_SHADER_RESOURCE

Bind a buffer or texture to a <a href="direct3d11.d3d10_graphics_programming_guide_shader_stages">shader stage</a>; this flag cannot be used with the <a href="https://msdn.microsoft.com/6a8e10cf-2cab-41f0-ba43-afa6854477ff">D3D10_MAP_WRITE_NO_OVERWRITE</a> flag.


### -field D3D10_BIND_STREAM_OUTPUT

Bind an output buffer for the <a href="https://msdn.microsoft.com/f902dc93-9612-481b-a6bd-073e924a4c79">stream-output stage</a>.


### -field D3D10_BIND_RENDER_TARGET

Bind a texture as a render target for the <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">output-merger stage</a>.


### -field D3D10_BIND_DEPTH_STENCIL

Bind a texture as a depth-stencil target for the <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">output-merger stage</a>.


## -remarks



In general, binding flags can be combined using a logical OR (except the constant-buffer flag); however, you should use a single flag to allow the device to optimize the resource usage.

This enumeration is used by a:

<ul>
<li>
<a href="https://msdn.microsoft.com/3f98c741-ff4c-4080-bd57-ef35cd6622d6">Buffer description</a> when creating a buffer.</li>
<li>Texture description when creating a texture (see <a href="https://msdn.microsoft.com/f4230e66-5b38-4c69-8406-974fb7708c16">D3D10_TEXTURE1D_DESC</a> or <a href="https://msdn.microsoft.com/2535da35-7985-4e50-b840-6a636f871697">D3D10_TEXTURE2D_DESC</a> or <a href="https://msdn.microsoft.com/b2447872-cbef-4cf2-ab7c-2739343ceb64">D3D10_TEXTURE3D_DESC</a>).</li>
</ul>
A shader-resource buffer is NOT a constant buffer; rather, it is a texture or buffer resource that is bound to a shader, that contains texture or buffer data (it is not limited to a single element type in the buffer). A shader-resource buffer is created with the D3D10_BIND_SHADER_RESOURCE flag and is bound to the pipeline using one of these APIs: <a href="https://msdn.microsoft.com/8e012e31-b161-4564-9acf-243d99366092">ID3D10Device::GSSetShaderResources</a>, <a href="https://msdn.microsoft.com/88b1515b-f070-4725-a844-30575a1800d4">ID3D10Device::PSSetShaderResources</a>, or <a href="https://msdn.microsoft.com/8481e388-3cfe-43e3-b58e-fea989d942ba">ID3D10Device::VSSetShaderResources</a>. Furthermore, a shader-resource buffer cannot use the <a href="https://msdn.microsoft.com/6a8e10cf-2cab-41f0-ba43-afa6854477ff">D3D10_MAP_WRITE_NO_OVERWRITE</a> flag.




## -see-also




<a href="https://msdn.microsoft.com/c986b22c-2960-4571-98bc-028c9f41ec65">Resource Enumerations</a>
 

 

