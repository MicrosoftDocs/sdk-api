---
UID: NN:d3d10.ID3D10Device
title: ID3D10Device (d3d10.h)
author: windows-sdk-content
description: The device interface represents a virtual adapter for Direct3D 10.0; it is used to perform rendering and create Direct3D resources.
old-location: direct3d10\id3d10device.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D10Device, ID3D10Device interface [Direct3D 10], ID3D10Device interface [Direct3D 10],described, ac9e57ea-6b44-febb-6528-dfb8cc6740db, d3d10/ID3D10Device, direct3d10.id3d10device
ms.topic: interface
req.header: d3d10.h
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
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
<a href="https://msdn.microsoft.com/en-us/library/Bb173534(v=VS.85).aspx">CheckCounter</a>
</td>
<td align="left" width="63%">
Get the type, name, units of measure, and a description of an existing counter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173535(v=VS.85).aspx">CheckCounterInfo</a>
</td>
<td align="left" width="63%">
Get a counter's information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173536(v=VS.85).aspx">CheckFormatSupport</a>
</td>
<td align="left" width="63%">
Get the support of a given format on the installed video device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173537(v=VS.85).aspx">CheckMultisampleQualityLevels</a>
</td>
<td align="left" width="63%">
Get the number of quality levels available during multisampling.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173538(v=VS.85).aspx">ClearDepthStencilView</a>
</td>
<td align="left" width="63%">
Clears the depth-stencil resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173539(v=VS.85).aspx">ClearRenderTargetView</a>
</td>
<td align="left" width="63%">
Set all the elements in a render target to one value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173540(v=VS.85).aspx">ClearState</a>
</td>
<td align="left" width="63%">
Restore all default device settings; return the device to the state it was in when it was created. This will set all set all input/output resource slots, shaders, input layouts, predications, scissor rectangles, depth-stencil state, rasterizer state, blend state, sampler state, and viewports to <b>NULL</b>. The primitive topology will be set to UNDEFINED.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173541(v=VS.85).aspx">CopyResource</a>
</td>
<td align="left" width="63%">
Copy the entire contents of the source resource to the destination resource using the GPU. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173542(v=VS.85).aspx">CopySubresourceRegion</a>
</td>
<td align="left" width="63%">
Copy a region from a source resource to a destination resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173543(v=VS.85).aspx">CreateBlendState</a>
</td>
<td align="left" width="63%">
Create a blend-state object that encapsules blend state for the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173544(v=VS.85).aspx">CreateBuffer</a>
</td>
<td align="left" width="63%">
Create a <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">buffer</a> (vertex buffer, index buffer, or shader-constant buffer).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173545(v=VS.85).aspx">CreateCounter</a>
</td>
<td align="left" width="63%">
Create a counter object for measuring GPU performance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173546(v=VS.85).aspx">CreateDepthStencilState</a>
</td>
<td align="left" width="63%">
Create a depth-stencil state object that encapsulates <a href="https://msdn.microsoft.com/en-us/library/Bb205120(v=VS.85).aspx">depth-stencil test</a> information for the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173547(v=VS.85).aspx">CreateDepthStencilView</a>
</td>
<td align="left" width="63%">
Create a depth-stencil <a href="https://msdn.microsoft.com/en-us/library/Bb205128(v=VS.85).aspx">view</a> for accessing resource data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173548(v=VS.85).aspx">CreateGeometryShader</a>
</td>
<td align="left" width="63%">
Create a geometry shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173549(v=VS.85).aspx">CreateGeometryShaderWithStreamOutput</a>
</td>
<td align="left" width="63%">
Creates a geometry shader that can write to streaming output buffers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173550(v=VS.85).aspx">CreateInputLayout</a>
</td>
<td align="left" width="63%">
Create an input-layout object to describe the input-buffer data for the <a href="https://msdn.microsoft.com/en-us/library/Bb205116(v=VS.85).aspx">input-assembler stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173551(v=VS.85).aspx">CreatePixelShader</a>
</td>
<td align="left" width="63%">
Create a pixel shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173552(v=VS.85).aspx">CreatePredicate</a>
</td>
<td align="left" width="63%">
Creates a predicate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173553(v=VS.85).aspx">CreateQuery</a>
</td>
<td align="left" width="63%">
This interface encapsulates methods for querying information from the GPU.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173554(v=VS.85).aspx">CreateRasterizerState</a>
</td>
<td align="left" width="63%">
Create a rasterizer state object that tells the <a href="https://msdn.microsoft.com/en-us/library/Bb205125(v=VS.85).aspx">rasterizer stage</a> how to behave.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173556(v=VS.85).aspx">CreateRenderTargetView</a>
</td>
<td align="left" width="63%">
Create a render-target <a href="https://msdn.microsoft.com/en-us/library/Bb205128(v=VS.85).aspx">view</a> for accessing resource data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173557(v=VS.85).aspx">CreateSamplerState</a>
</td>
<td align="left" width="63%">
Create a sampler-state object that encapsulates sampling information for a <a href="https://msdn.microsoft.com/en-us/library/Bb509700(v=VS.85).aspx">texture</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173558(v=VS.85).aspx">CreateShaderResourceView</a>
</td>
<td align="left" width="63%">
Create a shader-resource <a href="https://msdn.microsoft.com/en-us/library/Bb205128(v=VS.85).aspx">view</a> for accessing data in a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173559(v=VS.85).aspx">CreateTexture1D</a>
</td>
<td align="left" width="63%">
Create an array of 1D textures (see <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">Texture1D</a>).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173560(v=VS.85).aspx">CreateTexture2D</a>
</td>
<td align="left" width="63%">
Create an array of 2D textures (see <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">Texture2D</a>).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173561(v=VS.85).aspx">CreateTexture3D</a>
</td>
<td align="left" width="63%">
Create a single 3D texture (see <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">Texture3D</a>).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173562(v=VS.85).aspx">CreateVertexShader</a>
</td>
<td align="left" width="63%">
Create a vertex-shader object from a compiled shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173563(v=VS.85).aspx">Draw</a>
</td>
<td align="left" width="63%">
Draw non-indexed, non-instanced primitives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173564(v=VS.85).aspx">DrawAuto</a>
</td>
<td align="left" width="63%">
Draw geometry of an unknown size that was created by the geometry shader stage. See remarks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173565(v=VS.85).aspx">DrawIndexed</a>
</td>
<td align="left" width="63%">
Draw indexed, non-instanced primitives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173566(v=VS.85).aspx">DrawIndexedInstanced</a>
</td>
<td align="left" width="63%">
Draw indexed, instanced primitives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173567(v=VS.85).aspx">DrawInstanced</a>
</td>
<td align="left" width="63%">
Draw non-indexed, instanced primitives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173568(v=VS.85).aspx">Flush</a>
</td>
<td align="left" width="63%">
Send queued-up commands in the command buffer to the GPU.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173569(v=VS.85).aspx">GenerateMips</a>
</td>
<td align="left" width="63%">
Generates mipmaps for the given shader resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173570(v=VS.85).aspx">GetCreationFlags</a>
</td>
<td align="left" width="63%">
Get the flags used during the call to create the device with <a href="https://msdn.microsoft.com/en-us/library/Bb205086(v=VS.85).aspx">D3D10CreateDevice</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173571(v=VS.85).aspx">GetDeviceRemovedReason</a>
</td>
<td align="left" width="63%">
Get the reason why the device was removed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173572(v=VS.85).aspx">GetExceptionMode</a>
</td>
<td align="left" width="63%">
Get the exception-mode flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173573(v=VS.85).aspx">GetPredication</a>
</td>
<td align="left" width="63%">
Get the rendering predicate state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173574(v=VS.85).aspx">GetPrivateData</a>
</td>
<td align="left" width="63%">
Get data from a device that is associated with a guid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173575(v=VS.85).aspx">GetTextFilterSize</a>
</td>
<td align="left" width="63%">
This method is not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173576(v=VS.85).aspx">GSGetConstantBuffers</a>
</td>
<td align="left" width="63%">
Get the <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">constant buffers</a> used by the <a href="https://msdn.microsoft.com/en-us/library/Mt787170(v=VS.85).aspx">geometry shader</a> pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173577(v=VS.85).aspx">GSGetSamplers</a>
</td>
<td align="left" width="63%">
Get an array of sampler states from the <a href="https://msdn.microsoft.com/en-us/library/Mt787170(v=VS.85).aspx">geometry shader</a> pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173578(v=VS.85).aspx">GSGetShader</a>
</td>
<td align="left" width="63%">
Get the geometry shader currently set on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173579(v=VS.85).aspx">GSGetShaderResources</a>
</td>
<td align="left" width="63%">
Get the geometry shader resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173580(v=VS.85).aspx">GSSetConstantBuffers</a>
</td>
<td align="left" width="63%">
Set the <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">constant buffers</a> used by the <a href="https://msdn.microsoft.com/en-us/library/Mt787170(v=VS.85).aspx">geometry shader</a> pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173581(v=VS.85).aspx">GSSetSamplers</a>
</td>
<td align="left" width="63%">
Set an array of sampler states to the <a href="https://msdn.microsoft.com/en-us/library/Mt787170(v=VS.85).aspx">geometry shader</a> pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173582(v=VS.85).aspx">GSSetShader</a>
</td>
<td align="left" width="63%">
Set a geometry shader to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173583(v=VS.85).aspx">GSSetShaderResources</a>
</td>
<td align="left" width="63%">
Bind an array of shader resources to the <a href="https://msdn.microsoft.com/en-us/library/Mt787170(v=VS.85).aspx">geometry shader stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173584(v=VS.85).aspx">IAGetIndexBuffer</a>
</td>
<td align="left" width="63%">
Get a pointer to the <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">index buffer</a> that is bound to the <a href="https://msdn.microsoft.com/en-us/library/Bb205116(v=VS.85).aspx">input-assembler</a> stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173585(v=VS.85).aspx">IAGetInputLayout</a>
</td>
<td align="left" width="63%">
Get a pointer to the input-layout object that is bound to the <a href="https://msdn.microsoft.com/en-us/library/Bb205116(v=VS.85).aspx">input-assembler stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173586(v=VS.85).aspx">IAGetPrimitiveTopology</a>
</td>
<td align="left" width="63%">
Get information about the <a href="https://msdn.microsoft.com/en-us/library/Bb205124(v=VS.85).aspx">primitive type</a>, and data order that describes input data for the <a href="https://msdn.microsoft.com/en-us/library/Bb205116(v=VS.85).aspx">input assembler</a> stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173587(v=VS.85).aspx">IAGetVertexBuffers</a>
</td>
<td align="left" width="63%">
Get the <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">vertex buffers</a> bound to the <a href="https://msdn.microsoft.com/en-us/library/Bb205116(v=VS.85).aspx">input-assembler</a> stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173588(v=VS.85).aspx">IASetIndexBuffer</a>
</td>
<td align="left" width="63%">
Bind an <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">index buffer</a> to the <a href="https://msdn.microsoft.com/en-us/library/Bb205116(v=VS.85).aspx">input-assembler</a> stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173589(v=VS.85).aspx">IASetInputLayout</a>
</td>
<td align="left" width="63%">
Bind an input-layout object to the <a href="https://msdn.microsoft.com/en-us/library/Bb205116(v=VS.85).aspx">input-assembler stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173590(v=VS.85).aspx">IASetPrimitiveTopology</a>
</td>
<td align="left" width="63%">
Bind information about the <a href="https://msdn.microsoft.com/en-us/library/Bb205124(v=VS.85).aspx">primitive type</a>, and data order that describes input data for the <a href="https://msdn.microsoft.com/en-us/library/Bb205116(v=VS.85).aspx">input assembler</a> stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173591(v=VS.85).aspx">IASetVertexBuffers</a>
</td>
<td align="left" width="63%">
Bind an array of <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">vertex buffers</a> to the <a href="https://msdn.microsoft.com/en-us/library/Bb205116(v=VS.85).aspx">input-assembler</a> stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173592(v=VS.85).aspx">OMGetBlendState</a>
</td>
<td align="left" width="63%">
Get the <a href="https://msdn.microsoft.com/en-us/library/Bb205120(v=VS.85).aspx">blend state</a> of the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173593(v=VS.85).aspx">OMGetDepthStencilState</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/en-us/library/Bb205120(v=VS.85).aspx">depth-stencil</a> state of the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173594(v=VS.85).aspx">OMGetRenderTargets</a>
</td>
<td align="left" width="63%">
Get pointers to the render targets and the depth-stencil buffer that are available to the <a href="https://msdn.microsoft.com/en-us/library/Bb205120(v=VS.85).aspx">output-merger stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173595(v=VS.85).aspx">OMSetBlendState</a>
</td>
<td align="left" width="63%">
Set the <a href="https://msdn.microsoft.com/en-us/library/Bb205120(v=VS.85).aspx">blend state</a> of the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173596(v=VS.85).aspx">OMSetDepthStencilState</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://msdn.microsoft.com/en-us/library/Bb205120(v=VS.85).aspx">depth-stencil</a> state of 
    the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173597(v=VS.85).aspx">OMSetRenderTargets</a>
</td>
<td align="left" width="63%">
Bind one or more render targets and the depth-stencil buffer to the <a href="https://msdn.microsoft.com/en-us/library/Bb205120(v=VS.85).aspx">output-merger stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173598(v=VS.85).aspx">OpenSharedResource</a>
</td>
<td align="left" width="63%">
Give a device access to a shared resource created on a different Direct3d device. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173599(v=VS.85).aspx">PSGetConstantBuffers</a>
</td>
<td align="left" width="63%">
Get the <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">constant buffers</a> used by the <a href="https://msdn.microsoft.com/en-us/library/Mt787170(v=VS.85).aspx">pixel shader</a> pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173600(v=VS.85).aspx">PSGetSamplers</a>
</td>
<td align="left" width="63%">
Get an array of sampler states from the <a href="https://msdn.microsoft.com/en-us/library/Mt787170(v=VS.85).aspx">pixel shader</a> pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173601(v=VS.85).aspx">PSGetShader</a>
</td>
<td align="left" width="63%">
Get the pixel shader currently set on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173602(v=VS.85).aspx">PSGetShaderResources</a>
</td>
<td align="left" width="63%">
Get the pixel shader resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173603(v=VS.85).aspx">PSSetConstantBuffers</a>
</td>
<td align="left" width="63%">
Set the <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">constant buffers</a> used by the <a href="https://msdn.microsoft.com/en-us/library/Mt787170(v=VS.85).aspx">pixel shader</a> pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173604(v=VS.85).aspx">PSSetSamplers</a>
</td>
<td align="left" width="63%">
Set an array of sampler states to the <a href="https://msdn.microsoft.com/en-us/library/Mt787170(v=VS.85).aspx">pixel shader</a> pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173605(v=VS.85).aspx">PSSetShader</a>
</td>
<td align="left" width="63%">
Sets a pixel shader to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173606(v=VS.85).aspx">PSSetShaderResources</a>
</td>
<td align="left" width="63%">
Bind an array of shader resources to the <a href="https://msdn.microsoft.com/en-us/library/Mt787170(v=VS.85).aspx">pixel shader stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173607(v=VS.85).aspx">ResolveSubresource</a>
</td>
<td align="left" width="63%">
Copy a multisampled resource into a non-multisampled resource. This API is most useful when re-using the resulting rendertarget of one render pass as an input to a second render pass.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173608(v=VS.85).aspx">RSGetScissorRects</a>
</td>
<td align="left" width="63%">
Get the array of <a href="https://msdn.microsoft.com/en-us/library/Bb205126(v=VS.85).aspx">scissor rectangles</a> bound to the <a href="https://msdn.microsoft.com/en-us/library/Bb205125(v=VS.85).aspx">rasterizer stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173609(v=VS.85).aspx">RSGetState</a>
</td>
<td align="left" width="63%">
Get the <a href="https://msdn.microsoft.com/en-us/library/Bb172408(v=VS.85).aspx">rasterizer state</a> from the <a href="https://msdn.microsoft.com/en-us/library/Bb205125(v=VS.85).aspx">rasterizer stage</a> of the pipeline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173610(v=VS.85).aspx">RSGetViewports</a>
</td>
<td align="left" width="63%">
Get the array of <a href="https://msdn.microsoft.com/en-us/library/Bb205126(v=VS.85).aspx">viewports</a> bound 
    to the <a href="https://msdn.microsoft.com/en-us/library/Bb205125(v=VS.85).aspx">rasterizer stage</a>


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173611(v=VS.85).aspx">RSSetScissorRects</a>
</td>
<td align="left" width="63%">
Bind an array of <a href="https://msdn.microsoft.com/en-us/library/Bb205126(v=VS.85).aspx">scissor rectangles</a> to the <a href="https://msdn.microsoft.com/en-us/library/Bb205125(v=VS.85).aspx">rasterizer stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173612(v=VS.85).aspx">RSSetState</a>
</td>
<td align="left" width="63%">
Set the <a href="https://msdn.microsoft.com/en-us/library/Bb172408(v=VS.85).aspx">rasterizer state</a> for the <a href="https://msdn.microsoft.com/en-us/library/Bb205125(v=VS.85).aspx">rasterizer stage</a> of the pipeline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173613(v=VS.85).aspx">RSSetViewports</a>
</td>
<td align="left" width="63%">
Bind an array of <a href="https://msdn.microsoft.com/en-us/library/Bb205126(v=VS.85).aspx">viewports</a> to the <a href="https://msdn.microsoft.com/en-us/library/Bb205125(v=VS.85).aspx">rasterizer stage</a> of the pipeline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173614(v=VS.85).aspx">SetExceptionMode</a>
</td>
<td align="left" width="63%">
Get the exception-mode flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173615(v=VS.85).aspx">SetPredication</a>
</td>
<td align="left" width="63%">
Set a rendering predicate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173616(v=VS.85).aspx">SetPrivateData</a>
</td>
<td align="left" width="63%">
Set data to a device and associate that data with a guid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173617(v=VS.85).aspx">SetPrivateDataInterface</a>
</td>
<td align="left" width="63%">
Associate an <a href="http://msdn.microsoft.com/en-us/library/ms680509(VS.85).aspx">IUnknown</a>-derived interface with this device and associate that interface with an application-defined guid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173618(v=VS.85).aspx">SetTextFilterSize</a>
</td>
<td align="left" width="63%">
This method is not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173619(v=VS.85).aspx">SOGetTargets</a>
</td>
<td align="left" width="63%">
Get the target output <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">buffers</a> for the <a href="https://msdn.microsoft.com/en-us/library/Bb205121(v=VS.85).aspx">StreamOutput</a> stage of the pipeline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173620(v=VS.85).aspx">SOSetTargets</a>
</td>
<td align="left" width="63%">
Set the target output <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">buffers</a> for the <a href="https://msdn.microsoft.com/en-us/library/Bb205121(v=VS.85).aspx">StreamOutput</a> stage, which enables/disables the pipeline to stream-out data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173621(v=VS.85).aspx">UpdateSubresource</a>
</td>
<td align="left" width="63%">
The CPU copies data from memory to a <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">subresource</a> created in non-mappable memory. See remarks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173622(v=VS.85).aspx">VSGetConstantBuffers</a>
</td>
<td align="left" width="63%">
Get the <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">constant buffers</a> used by the <a href="https://msdn.microsoft.com/en-us/library/Mt787170(v=VS.85).aspx">vertex shader</a> pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173623(v=VS.85).aspx">VSGetSamplers</a>
</td>
<td align="left" width="63%">
Get an array of sampler states from the <a href="https://msdn.microsoft.com/en-us/library/Mt787170(v=VS.85).aspx">vertex shader</a> pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173624(v=VS.85).aspx">VSGetShader</a>
</td>
<td align="left" width="63%">
Get the vertex shader currently set on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173625(v=VS.85).aspx">VSGetShaderResources</a>
</td>
<td align="left" width="63%">
Get the vertex shader resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173626(v=VS.85).aspx">VSSetConstantBuffers</a>
</td>
<td align="left" width="63%">
Set the <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">constant buffers</a> used by the <a href="https://msdn.microsoft.com/en-us/library/Mt787170(v=VS.85).aspx">vertex shader</a> pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173627(v=VS.85).aspx">VSSetSamplers</a>
</td>
<td align="left" width="63%">
Set an array of sampler states to the <a href="https://msdn.microsoft.com/en-us/library/Mt787170(v=VS.85).aspx">vertex shader</a> pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173628(v=VS.85).aspx">VSSetShader</a>
</td>
<td align="left" width="63%">
Set a vertex shader to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173629(v=VS.85).aspx">VSSetShaderResources</a>
</td>
<td align="left" width="63%">
Bind an array of shader resources to the <a href="https://msdn.microsoft.com/en-us/library/Mt787170(v=VS.85).aspx">vertex shader stage</a>.

</td>
</tr>
</table> 


## -remarks



A device is created using <a href="https://msdn.microsoft.com/en-us/library/Bb205086(v=VS.85).aspx">D3D10CreateDevice</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205152(v=VS.85).aspx">Core Interfaces</a>
 

 

