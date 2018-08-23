---
UID: NN:d3d10.ID3D10Device
title: ID3D10Device
author: windows-sdk-content
description: The device interface represents a virtual adapter for Direct3D 10.0; it is used to perform rendering and create Direct3D resources.
old-location: direct3d10\id3d10device.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: ID3D10Device, ID3D10Device interface [Direct3D 10], ID3D10Device interface [Direct3D 10],described, ac9e57ea-6b44-febb-6528-dfb8cc6740db, d3d10/ID3D10Device, direct3d10.id3d10device
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d10.h
req.include-header: 
req.redist: 
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
req.typenames: D3D10_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device interface


## -description


The device interface represents a virtual adapter for Direct3D 10.0; it is used to perform rendering and create Direct3D resources.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10Device</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D10Device</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10Device</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a36399af-088f-47b2-a580-d871f9e92038">CheckCounter</a>
</td>
<td align="left" width="63%">
Get the type, name, units of measure, and a description of an existing counter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dfa4cc61-2c1d-45a7-839c-f7df64d488ac">CheckCounterInfo</a>
</td>
<td align="left" width="63%">
Get a counter's information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50b4fcbb-3c51-4027-b766-ea0590eb7766">CheckFormatSupport</a>
</td>
<td align="left" width="63%">
Get the support of a given format on the installed video device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b43c582-3ddb-49d8-be0d-1a784f482750">CheckMultisampleQualityLevels</a>
</td>
<td align="left" width="63%">
Get the number of quality levels available during multisampling.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac596c4d-dc54-4433-8625-defa8a04bba0">ClearDepthStencilView</a>
</td>
<td align="left" width="63%">
Clears the depth-stencil resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c1a630a3-3ffe-4d6a-a8e2-7a228167adb2">ClearRenderTargetView</a>
</td>
<td align="left" width="63%">
Set all the elements in a render target to one value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9fb42265-26fc-44c1-aa43-cb87ac475718">ClearState</a>
</td>
<td align="left" width="63%">
Restore all default device settings; return the device to the state it was in when it was created. This will set all set all input/output resource slots, shaders, input layouts, predications, scissor rectangles, depth-stencil state, rasterizer state, blend state, sampler state, and viewports to <b>NULL</b>. The primitive topology will be set to UNDEFINED.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f3f8089-8343-4f83-9208-fd21617b8d19">CopyResource</a>
</td>
<td align="left" width="63%">
Copy the entire contents of the source resource to the destination resource using the GPU. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/78803e46-9945-45d4-a7cc-41f527831251">CopySubresourceRegion</a>
</td>
<td align="left" width="63%">
Copy a region from a source resource to a destination resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a5b000d-769b-4e4c-9c9c-d8fced703812">CreateBlendState</a>
</td>
<td align="left" width="63%">
Create a blend-state object that encapsules blend state for the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77e943f7-f347-4d04-8e2e-a678d5a2c81c">CreateBuffer</a>
</td>
<td align="left" width="63%">
Create a <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">buffer</a> (vertex buffer, index buffer, or shader-constant buffer).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bead7e2d-3d29-4b41-87f7-b821a4ffb78a">CreateCounter</a>
</td>
<td align="left" width="63%">
Create a counter object for measuring GPU performance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/41dab20f-53e7-488d-a0c5-7435122d81b8">CreateDepthStencilState</a>
</td>
<td align="left" width="63%">
Create a depth-stencil state object that encapsulates <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">depth-stencil test</a> information for the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42bff154-36e6-4199-899c-c21917444c1d">CreateDepthStencilView</a>
</td>
<td align="left" width="63%">
Create a depth-stencil <a href="https://msdn.microsoft.com/ccfe6273-0dcf-4b42-9d74-665a0b4cd14a">view</a> for accessing resource data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6202ed81-a599-497f-a271-940f5605fb84">CreateGeometryShader</a>
</td>
<td align="left" width="63%">
Create a geometry shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f4e99b74-032b-4ae2-88d1-f0837cdbcbfb">CreateGeometryShaderWithStreamOutput</a>
</td>
<td align="left" width="63%">
Creates a geometry shader that can write to streaming output buffers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/61516e1a-f588-4dcb-9ada-9b483fe7cc99">CreateInputLayout</a>
</td>
<td align="left" width="63%">
Create an input-layout object to describe the input-buffer data for the <a href="https://msdn.microsoft.com/71141a5e-2d79-4b02-8370-c0cbc8618908">input-assembler stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85dfc580-1231-413d-8cc1-6bfd9e0eec68">CreatePixelShader</a>
</td>
<td align="left" width="63%">
Create a pixel shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/472d782b-a9ea-49b2-8489-4e074e48c15e">CreatePredicate</a>
</td>
<td align="left" width="63%">
Creates a predicate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8313b54-6aa8-4a41-9dbd-9c175bf6a1d2">CreateQuery</a>
</td>
<td align="left" width="63%">
This interface encapsulates methods for querying information from the GPU.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd304e42-e4f6-4bc4-baf0-b4c8287e3351">CreateRasterizerState</a>
</td>
<td align="left" width="63%">
Create a rasterizer state object that tells the <a href="https://msdn.microsoft.com/efd3f819-7c63-4e1a-9923-8e7198354ec6">rasterizer stage</a> how to behave.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/950dc130-c23c-41e4-ad51-49167916fa5c">CreateRenderTargetView</a>
</td>
<td align="left" width="63%">
Create a render-target <a href="https://msdn.microsoft.com/ccfe6273-0dcf-4b42-9d74-665a0b4cd14a">view</a> for accessing resource data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82dea278-1555-49b8-9c1d-91399afa5c7e">CreateSamplerState</a>
</td>
<td align="left" width="63%">
Create a sampler-state object that encapsulates sampling information for a <a href="https://msdn.microsoft.com/e8cb483a-d831-4942-b6fe-61dd5edb1813">texture</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32e5d4d0-6686-4bcc-8ddb-fe519544051b">CreateShaderResourceView</a>
</td>
<td align="left" width="63%">
Create a shader-resource <a href="https://msdn.microsoft.com/ccfe6273-0dcf-4b42-9d74-665a0b4cd14a">view</a> for accessing data in a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/805e7bef-f4d5-4aa9-99a1-491e0518db7b">CreateTexture1D</a>
</td>
<td align="left" width="63%">
Create an array of 1D textures (see <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">Texture1D</a>).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f9e81e1-721c-4895-9196-2be3e5b260fd">CreateTexture2D</a>
</td>
<td align="left" width="63%">
Create an array of 2D textures (see <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">Texture2D</a>).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f57a2e5-c663-46c3-a092-798a15cf9154">CreateTexture3D</a>
</td>
<td align="left" width="63%">
Create a single 3D texture (see <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">Texture3D</a>).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a7449878-b0a7-44b6-acbc-172449523098">CreateVertexShader</a>
</td>
<td align="left" width="63%">
Create a vertex-shader object from a compiled shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01847bc8-3a58-4296-9e67-2fecd3832e48">Draw</a>
</td>
<td align="left" width="63%">
Draw non-indexed, non-instanced primitives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22261780-2768-4ea2-9e92-57ae5560e8fe">DrawAuto</a>
</td>
<td align="left" width="63%">
Draw geometry of an unknown size that was created by the geometry shader stage. See remarks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/10c4a734-6425-4bd1-ac8e-85e3255e732a">DrawIndexed</a>
</td>
<td align="left" width="63%">
Draw indexed, non-instanced primitives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/00713e51-0bc6-4141-a10a-ab998666cdb4">DrawIndexedInstanced</a>
</td>
<td align="left" width="63%">
Draw indexed, instanced primitives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de2cc0de-7bf3-4b03-a3de-65f841bfc228">DrawInstanced</a>
</td>
<td align="left" width="63%">
Draw non-indexed, instanced primitives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f907d7d-4316-453f-a7ea-6b228a0df569">Flush</a>
</td>
<td align="left" width="63%">
Send queued-up commands in the command buffer to the GPU.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc3491b6-99fb-4560-bce1-dd7758626cf9">GenerateMips</a>
</td>
<td align="left" width="63%">
Generates mipmaps for the given shader resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/490126d3-7298-4f88-9703-3dc2dd30c0a8">GetCreationFlags</a>
</td>
<td align="left" width="63%">
Get the flags used during the call to create the device with <a href="https://msdn.microsoft.com/da48d6d4-f35b-4cd1-a358-8eec63dfa674">D3D10CreateDevice</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2c2085b-f0d8-4227-81dd-c37907920564">GetDeviceRemovedReason</a>
</td>
<td align="left" width="63%">
Get the reason why the device was removed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c343ba41-4fec-4598-8eac-30674ab77a49">GetExceptionMode</a>
</td>
<td align="left" width="63%">
Get the exception-mode flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20cafa97-0677-4660-a889-01e99668b04f">GetPredication</a>
</td>
<td align="left" width="63%">
Get the rendering predicate state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba0be621-d063-425f-a87f-ded0135c6434">GetPrivateData</a>
</td>
<td align="left" width="63%">
Get data from a device that is associated with a guid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9f1d623-d0ff-4613-bead-00e2439c8ace">GetTextFilterSize</a>
</td>
<td align="left" width="63%">
This method is not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce3c33fe-4f6c-4395-9eb7-a4fb9b21984d">GSGetConstantBuffers</a>
</td>
<td align="left" width="63%">
Get the <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">constant buffers</a> used by the <a href="direct3d10.d3d10_graphics_programming_guide_shader_stages">geometry shader</a> pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8d73dab-f81b-4858-9e30-a25c969d0290">GSGetSamplers</a>
</td>
<td align="left" width="63%">
Get an array of sampler states from the <a href="direct3d10.d3d10_graphics_programming_guide_shader_stages">geometry shader</a> pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d848f51-a06c-4757-b79c-6c7a31b06b6b">GSGetShader</a>
</td>
<td align="left" width="63%">
Get the geometry shader currently set on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca76febd-72ca-4a07-b5cc-8490a8792dab">GSGetShaderResources</a>
</td>
<td align="left" width="63%">
Get the geometry shader resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b736c9db-e0c0-4c38-a58a-7b3c247e374d">GSSetConstantBuffers</a>
</td>
<td align="left" width="63%">
Set the <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">constant buffers</a> used by the <a href="direct3d10.d3d10_graphics_programming_guide_shader_stages">geometry shader</a> pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/881cea8b-eb37-4614-b4dc-81a3e8c929d3">GSSetSamplers</a>
</td>
<td align="left" width="63%">
Set an array of sampler states to the <a href="direct3d10.d3d10_graphics_programming_guide_shader_stages">geometry shader</a> pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cd591f9d-dd17-48e3-b952-9f38c7572b93">GSSetShader</a>
</td>
<td align="left" width="63%">
Set a geometry shader to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e012e31-b161-4564-9acf-243d99366092">GSSetShaderResources</a>
</td>
<td align="left" width="63%">
Bind an array of shader resources to the <a href="direct3d10.d3d10_graphics_programming_guide_shader_stages">geometry shader stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/744cf15e-524b-4287-9482-b590ab30148c">IAGetIndexBuffer</a>
</td>
<td align="left" width="63%">
Get a pointer to the <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">index buffer</a> that is bound to the <a href="https://msdn.microsoft.com/71141a5e-2d79-4b02-8370-c0cbc8618908">input-assembler</a> stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50b7ff83-2ce2-4805-a20b-a5329d2a955c">IAGetInputLayout</a>
</td>
<td align="left" width="63%">
Get a pointer to the input-layout object that is bound to the <a href="https://msdn.microsoft.com/71141a5e-2d79-4b02-8370-c0cbc8618908">input-assembler stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1662dd95-df26-4f0c-9f12-07d958bfb3aa">IAGetPrimitiveTopology</a>
</td>
<td align="left" width="63%">
Get information about the <a href="https://msdn.microsoft.com/357ad085-fd91-4420-abc3-1c57e8cbb517">primitive type</a>, and data order that describes input data for the <a href="https://msdn.microsoft.com/71141a5e-2d79-4b02-8370-c0cbc8618908">input assembler</a> stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7dc43a98-b7f8-4276-802a-147ee8abf437">IAGetVertexBuffers</a>
</td>
<td align="left" width="63%">
Get the <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">vertex buffers</a> bound to the <a href="https://msdn.microsoft.com/71141a5e-2d79-4b02-8370-c0cbc8618908">input-assembler</a> stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b276345-502e-47fa-9caa-52a82916b577">IASetIndexBuffer</a>
</td>
<td align="left" width="63%">
Bind an <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">index buffer</a> to the <a href="https://msdn.microsoft.com/71141a5e-2d79-4b02-8370-c0cbc8618908">input-assembler</a> stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/10270e52-8ba6-45a6-a6f2-80e3f3447806">IASetInputLayout</a>
</td>
<td align="left" width="63%">
Bind an input-layout object to the <a href="https://msdn.microsoft.com/71141a5e-2d79-4b02-8370-c0cbc8618908">input-assembler stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c39db604-7d00-4b22-8bbe-9eda6908c3a1">IASetPrimitiveTopology</a>
</td>
<td align="left" width="63%">
Bind information about the <a href="https://msdn.microsoft.com/357ad085-fd91-4420-abc3-1c57e8cbb517">primitive type</a>, and data order that describes input data for the <a href="https://msdn.microsoft.com/71141a5e-2d79-4b02-8370-c0cbc8618908">input assembler</a> stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/00fcf32c-982f-4636-bf02-b3f95803684a">IASetVertexBuffers</a>
</td>
<td align="left" width="63%">
Bind an array of <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">vertex buffers</a> to the <a href="https://msdn.microsoft.com/71141a5e-2d79-4b02-8370-c0cbc8618908">input-assembler</a> stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da49b042-c6e1-41e9-8e49-238de090d502">OMGetBlendState</a>
</td>
<td align="left" width="63%">
Get the <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">blend state</a> of the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/18aa270d-5806-4f3d-b2a1-88481cc2560a">OMGetDepthStencilState</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">depth-stencil</a> state of the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9157ec59-f916-40cd-80b0-68d9f63c4db9">OMGetRenderTargets</a>
</td>
<td align="left" width="63%">
Get pointers to the render targets and the depth-stencil buffer that are available to the <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">output-merger stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39169f4f-8a7b-4db0-abd5-5b67b204b394">OMSetBlendState</a>
</td>
<td align="left" width="63%">
Set the <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">blend state</a> of the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7cf8e5ca-08f2-4fa3-8657-cbce5d773dcf">OMSetDepthStencilState</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">depth-stencil</a> state of 
    the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/68c20b1a-921a-4513-811b-f3b6999518f8">OMSetRenderTargets</a>
</td>
<td align="left" width="63%">
Bind one or more render targets and the depth-stencil buffer to the <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">output-merger stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/581117dc-dd3a-47ac-a080-f23e72a82a6f">OpenSharedResource</a>
</td>
<td align="left" width="63%">
Give a device access to a shared resource created on a different Direct3d device. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dbf82053-540b-4629-9bc2-be249eed1336">PSGetConstantBuffers</a>
</td>
<td align="left" width="63%">
Get the <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">constant buffers</a> used by the <a href="direct3d10.d3d10_graphics_programming_guide_shader_stages">pixel shader</a> pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/654ba7fe-f807-40b0-8510-7f37c2067dcd">PSGetSamplers</a>
</td>
<td align="left" width="63%">
Get an array of sampler states from the <a href="direct3d10.d3d10_graphics_programming_guide_shader_stages">pixel shader</a> pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6499083a-6c0f-42b4-a43b-9c4f9cb82edd">PSGetShader</a>
</td>
<td align="left" width="63%">
Get the pixel shader currently set on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/063a391b-3a0b-4f87-ab67-7a0df8e82ccb">PSGetShaderResources</a>
</td>
<td align="left" width="63%">
Get the pixel shader resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3d8de009-8a56-458c-bb62-de36ae094717">PSSetConstantBuffers</a>
</td>
<td align="left" width="63%">
Set the <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">constant buffers</a> used by the <a href="direct3d10.d3d10_graphics_programming_guide_shader_stages">pixel shader</a> pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2684b37d-8f10-4c32-8c52-fc2e5bf2122c">PSSetSamplers</a>
</td>
<td align="left" width="63%">
Set an array of sampler states to the <a href="direct3d10.d3d10_graphics_programming_guide_shader_stages">pixel shader</a> pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e7cf7fb-e2c0-4524-a909-5592decd9a66">PSSetShader</a>
</td>
<td align="left" width="63%">
Sets a pixel shader to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/88b1515b-f070-4725-a844-30575a1800d4">PSSetShaderResources</a>
</td>
<td align="left" width="63%">
Bind an array of shader resources to the <a href="direct3d10.d3d10_graphics_programming_guide_shader_stages">pixel shader stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf2e9849-dbd8-4047-8e34-88fca5409bc9">ResolveSubresource</a>
</td>
<td align="left" width="63%">
Copy a multisampled resource into a non-multisampled resource. This API is most useful when re-using the resulting rendertarget of one render pass as an input to a second render pass.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64a1e3eb-b7ff-4665-8b9a-b33d76be0953">RSGetScissorRects</a>
</td>
<td align="left" width="63%">
Get the array of <a href="https://msdn.microsoft.com/d78c3845-76fd-4bd7-a603-bb1d8c66ac49">scissor rectangles</a> bound to the <a href="https://msdn.microsoft.com/efd3f819-7c63-4e1a-9923-8e7198354ec6">rasterizer stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a088c319-9f85-4170-b29d-e786d53e0c4d">RSGetState</a>
</td>
<td align="left" width="63%">
Get the <a href="https://msdn.microsoft.com/ae4bb4c4-35a8-43c3-bfa5-f57b44bc367e">rasterizer state</a> from the <a href="https://msdn.microsoft.com/efd3f819-7c63-4e1a-9923-8e7198354ec6">rasterizer stage</a> of the pipeline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/878637b8-ecc6-4580-82d4-f4b990bba9c8">RSGetViewports</a>
</td>
<td align="left" width="63%">
Get the array of <a href="https://msdn.microsoft.com/d78c3845-76fd-4bd7-a603-bb1d8c66ac49">viewports</a> bound 
    to the <a href="https://msdn.microsoft.com/efd3f819-7c63-4e1a-9923-8e7198354ec6">rasterizer stage</a>


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38b1d970-ecbd-45cc-a4c5-76f671247e56">RSSetScissorRects</a>
</td>
<td align="left" width="63%">
Bind an array of <a href="https://msdn.microsoft.com/d78c3845-76fd-4bd7-a603-bb1d8c66ac49">scissor rectangles</a> to the <a href="https://msdn.microsoft.com/efd3f819-7c63-4e1a-9923-8e7198354ec6">rasterizer stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b873af4-9724-4a36-bfdd-ea47c667124f">RSSetState</a>
</td>
<td align="left" width="63%">
Set the <a href="https://msdn.microsoft.com/ae4bb4c4-35a8-43c3-bfa5-f57b44bc367e">rasterizer state</a> for the <a href="https://msdn.microsoft.com/efd3f819-7c63-4e1a-9923-8e7198354ec6">rasterizer stage</a> of the pipeline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d622c531-8cd5-46f6-82dd-27a202c2b58f">RSSetViewports</a>
</td>
<td align="left" width="63%">
Bind an array of <a href="https://msdn.microsoft.com/d78c3845-76fd-4bd7-a603-bb1d8c66ac49">viewports</a> to the <a href="https://msdn.microsoft.com/efd3f819-7c63-4e1a-9923-8e7198354ec6">rasterizer stage</a> of the pipeline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd15256d-4dc8-43d5-87de-2d35956dc0bd">SetExceptionMode</a>
</td>
<td align="left" width="63%">
Get the exception-mode flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/175c4905-834a-4f18-bbf6-3bbe20e06d4d">SetPredication</a>
</td>
<td align="left" width="63%">
Set a rendering predicate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1fc318f0-feeb-4aac-91e8-ee9e4d785f40">SetPrivateData</a>
</td>
<td align="left" width="63%">
Set data to a device and associate that data with a guid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71d529a1-acaf-49a9-a4c7-6896979c8909">SetPrivateDataInterface</a>
</td>
<td align="left" width="63%">
Associate an <a href="http://msdn.microsoft.com/en-us/library/ms680509(VS.85).aspx">IUnknown</a>-derived interface with this device and associate that interface with an application-defined guid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af4eda3a-3348-41f5-a474-28af082dfed9">SetTextFilterSize</a>
</td>
<td align="left" width="63%">
This method is not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/83753497-3f00-4c5d-9b75-13269b06bdc2">SOGetTargets</a>
</td>
<td align="left" width="63%">
Get the target output <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">buffers</a> for the <a href="https://msdn.microsoft.com/f902dc93-9612-481b-a6bd-073e924a4c79">StreamOutput</a> stage of the pipeline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd4a71a1-2180-421f-8c9b-735c33f6de75">SOSetTargets</a>
</td>
<td align="left" width="63%">
Set the target output <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">buffers</a> for the <a href="https://msdn.microsoft.com/f902dc93-9612-481b-a6bd-073e924a4c79">StreamOutput</a> stage, which enables/disables the pipeline to stream-out data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eeab4057-4827-4c4b-ae8d-1cbf1f1c9e44">UpdateSubresource</a>
</td>
<td align="left" width="63%">
The CPU copies data from memory to a <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">subresource</a> created in non-mappable memory. See remarks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dfb614c5-2e83-45e7-80a1-24d66d170b3d">VSGetConstantBuffers</a>
</td>
<td align="left" width="63%">
Get the <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">constant buffers</a> used by the <a href="direct3d10.d3d10_graphics_programming_guide_shader_stages">vertex shader</a> pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb35c064-b308-40a3-ae77-7b4e8819fffa">VSGetSamplers</a>
</td>
<td align="left" width="63%">
Get an array of sampler states from the <a href="direct3d10.d3d10_graphics_programming_guide_shader_stages">vertex shader</a> pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d4922ef4-ff5a-4664-ac37-68facb7c7314">VSGetShader</a>
</td>
<td align="left" width="63%">
Get the vertex shader currently set on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8f2247e0-0d30-4ea0-a470-0ec38f33a0c8">VSGetShaderResources</a>
</td>
<td align="left" width="63%">
Get the vertex shader resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf5a2172-a4ca-4e76-ae79-d5fbf5bcb155">VSSetConstantBuffers</a>
</td>
<td align="left" width="63%">
Set the <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">constant buffers</a> used by the <a href="direct3d10.d3d10_graphics_programming_guide_shader_stages">vertex shader</a> pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4310c4dc-7fb4-4b69-9bc5-e89761d2e34c">VSSetSamplers</a>
</td>
<td align="left" width="63%">
Set an array of sampler states to the <a href="direct3d10.d3d10_graphics_programming_guide_shader_stages">vertex shader</a> pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ebc673d-d3e0-4678-8c6e-b11fb75e1ed1">VSSetShader</a>
</td>
<td align="left" width="63%">
Set a vertex shader to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8481e388-3cfe-43e3-b58e-fea989d942ba">VSSetShaderResources</a>
</td>
<td align="left" width="63%">
Bind an array of shader resources to the <a href="direct3d10.d3d10_graphics_programming_guide_shader_stages">vertex shader stage</a>.

</td>
</tr>
</table> 


## -remarks



A device is created using <a href="https://msdn.microsoft.com/da48d6d4-f35b-4cd1-a358-8eec63dfa674">D3D10CreateDevice</a>.




## -see-also




<a href="https://msdn.microsoft.com/f5ad2db8-da90-4bcd-83a7-7466723a9c3c">Core Interfaces</a>
 

 

