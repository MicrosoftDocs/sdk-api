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
f1_keywords: ["d3d10/ID3D10Device"]
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10Device</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D10Device</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-checkcounter">CheckCounter</a>
</td>
<td align="left" width="63%">
Get the type, name, units of measure, and a description of an existing counter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-checkcounterinfo">CheckCounterInfo</a>
</td>
<td align="left" width="63%">
Get a counter's information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-checkformatsupport">CheckFormatSupport</a>
</td>
<td align="left" width="63%">
Get the support of a given format on the installed video device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-checkmultisamplequalitylevels">CheckMultisampleQualityLevels</a>
</td>
<td align="left" width="63%">
Get the number of quality levels available during multisampling.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-cleardepthstencilview">ClearDepthStencilView</a>
</td>
<td align="left" width="63%">
Clears the depth-stencil resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-clearrendertargetview">ClearRenderTargetView</a>
</td>
<td align="left" width="63%">
Set all the elements in a render target to one value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-clearstate">ClearState</a>
</td>
<td align="left" width="63%">
Restore all default device settings; return the device to the state it was in when it was created. This will set all set all input/output resource slots, shaders, input layouts, predications, scissor rectangles, depth-stencil state, rasterizer state, blend state, sampler state, and viewports to <b>NULL</b>. The primitive topology will be set to UNDEFINED.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-copyresource">CopyResource</a>
</td>
<td align="left" width="63%">
Copy the entire contents of the source resource to the destination resource using the GPU. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-copysubresourceregion">CopySubresourceRegion</a>
</td>
<td align="left" width="63%">
Copy a region from a source resource to a destination resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createblendstate">CreateBlendState</a>
</td>
<td align="left" width="63%">
Create a blend-state object that encapsules blend state for the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createbuffer">CreateBuffer</a>
</td>
<td align="left" width="63%">
Create a <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">buffer</a> (vertex buffer, index buffer, or shader-constant buffer).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createcounter">CreateCounter</a>
</td>
<td align="left" width="63%">
Create a counter object for measuring GPU performance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createdepthstencilstate">CreateDepthStencilState</a>
</td>
<td align="left" width="63%">
Create a depth-stencil state object that encapsulates <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">depth-stencil test</a> information for the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createdepthstencilview">CreateDepthStencilView</a>
</td>
<td align="left" width="63%">
Create a depth-stencil <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views">view</a> for accessing resource data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-creategeometryshader">CreateGeometryShader</a>
</td>
<td align="left" width="63%">
Create a geometry shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-creategeometryshaderwithstreamoutput">CreateGeometryShaderWithStreamOutput</a>
</td>
<td align="left" width="63%">
Creates a geometry shader that can write to streaming output buffers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createinputlayout">CreateInputLayout</a>
</td>
<td align="left" width="63%">
Create an input-layout object to describe the input-buffer data for the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage">input-assembler stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createpixelshader">CreatePixelShader</a>
</td>
<td align="left" width="63%">
Create a pixel shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createpredicate">CreatePredicate</a>
</td>
<td align="left" width="63%">
Creates a predicate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createquery">CreateQuery</a>
</td>
<td align="left" width="63%">
This interface encapsulates methods for querying information from the GPU.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createrasterizerstate">CreateRasterizerState</a>
</td>
<td align="left" width="63%">
Create a rasterizer state object that tells the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage">rasterizer stage</a> how to behave.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createrendertargetview">CreateRenderTargetView</a>
</td>
<td align="left" width="63%">
Create a render-target <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views">view</a> for accessing resource data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createsamplerstate">CreateSamplerState</a>
</td>
<td align="left" width="63%">
Create a sampler-state object that encapsulates sampling information for a <a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-type">texture</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createshaderresourceview">CreateShaderResourceView</a>
</td>
<td align="left" width="63%">
Create a shader-resource <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views">view</a> for accessing data in a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createtexture1d">CreateTexture1D</a>
</td>
<td align="left" width="63%">
Create an array of 1D textures (see <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">Texture1D</a>).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createtexture2d">CreateTexture2D</a>
</td>
<td align="left" width="63%">
Create an array of 2D textures (see <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">Texture2D</a>).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createtexture3d">CreateTexture3D</a>
</td>
<td align="left" width="63%">
Create a single 3D texture (see <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">Texture3D</a>).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createvertexshader">CreateVertexShader</a>
</td>
<td align="left" width="63%">
Create a vertex-shader object from a compiled shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-draw">Draw</a>
</td>
<td align="left" width="63%">
Draw non-indexed, non-instanced primitives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-drawauto">DrawAuto</a>
</td>
<td align="left" width="63%">
Draw geometry of an unknown size that was created by the geometry shader stage. See remarks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-drawindexed">DrawIndexed</a>
</td>
<td align="left" width="63%">
Draw indexed, non-instanced primitives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-drawindexedinstanced">DrawIndexedInstanced</a>
</td>
<td align="left" width="63%">
Draw indexed, instanced primitives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-drawinstanced">DrawInstanced</a>
</td>
<td align="left" width="63%">
Draw non-indexed, instanced primitives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-flush">Flush</a>
</td>
<td align="left" width="63%">
Send queued-up commands in the command buffer to the GPU.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-generatemips">GenerateMips</a>
</td>
<td align="left" width="63%">
Generates mipmaps for the given shader resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-getcreationflags">GetCreationFlags</a>
</td>
<td align="left" width="63%">
Get the flags used during the call to create the device with <a href="https://docs.microsoft.com/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice">D3D10CreateDevice</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-getdeviceremovedreason">GetDeviceRemovedReason</a>
</td>
<td align="left" width="63%">
Get the reason why the device was removed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-getexceptionmode">GetExceptionMode</a>
</td>
<td align="left" width="63%">
Get the exception-mode flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-getpredication">GetPredication</a>
</td>
<td align="left" width="63%">
Get the rendering predicate state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-getprivatedata">GetPrivateData</a>
</td>
<td align="left" width="63%">
Get data from a device that is associated with a guid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gettextfiltersize">GetTextFilterSize</a>
</td>
<td align="left" width="63%">
This method is not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gsgetconstantbuffers">GSGetConstantBuffers</a>
</td>
<td align="left" width="63%">
Get the <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">constant buffers</a> used by the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/geometry-shader-stage">geometry shader</a> pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gsgetsamplers">GSGetSamplers</a>
</td>
<td align="left" width="63%">
Get an array of sampler states from the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/geometry-shader-stage">geometry shader</a> pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gsgetshader">GSGetShader</a>
</td>
<td align="left" width="63%">
Get the geometry shader currently set on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gsgetshaderresources">GSGetShaderResources</a>
</td>
<td align="left" width="63%">
Get the geometry shader resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetconstantbuffers">GSSetConstantBuffers</a>
</td>
<td align="left" width="63%">
Set the <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">constant buffers</a> used by the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/geometry-shader-stage">geometry shader</a> pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetsamplers">GSSetSamplers</a>
</td>
<td align="left" width="63%">
Set an array of sampler states to the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/geometry-shader-stage">geometry shader</a> pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetshader">GSSetShader</a>
</td>
<td align="left" width="63%">
Set a geometry shader to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetshaderresources">GSSetShaderResources</a>
</td>
<td align="left" width="63%">
Bind an array of shader resources to the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/geometry-shader-stage">geometry shader stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-iagetindexbuffer">IAGetIndexBuffer</a>
</td>
<td align="left" width="63%">
Get a pointer to the <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">index buffer</a> that is bound to the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage">input-assembler</a> stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-iagetinputlayout">IAGetInputLayout</a>
</td>
<td align="left" width="63%">
Get a pointer to the input-layout object that is bound to the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage">input-assembler stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-iagetprimitivetopology">IAGetPrimitiveTopology</a>
</td>
<td align="left" width="63%">
Get information about the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-primitive-topologies">primitive type</a>, and data order that describes input data for the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage">input assembler</a> stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-iagetvertexbuffers">IAGetVertexBuffers</a>
</td>
<td align="left" width="63%">
Get the <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">vertex buffers</a> bound to the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage">input-assembler</a> stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-iasetindexbuffer">IASetIndexBuffer</a>
</td>
<td align="left" width="63%">
Bind an <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">index buffer</a> to the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage">input-assembler</a> stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-iasetinputlayout">IASetInputLayout</a>
</td>
<td align="left" width="63%">
Bind an input-layout object to the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage">input-assembler stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-iasetprimitivetopology">IASetPrimitiveTopology</a>
</td>
<td align="left" width="63%">
Bind information about the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-primitive-topologies">primitive type</a>, and data order that describes input data for the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage">input assembler</a> stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-iasetvertexbuffers">IASetVertexBuffers</a>
</td>
<td align="left" width="63%">
Bind an array of <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">vertex buffers</a> to the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage">input-assembler</a> stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-omgetblendstate">OMGetBlendState</a>
</td>
<td align="left" width="63%">
Get the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">blend state</a> of the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-omgetdepthstencilstate">OMGetDepthStencilState</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">depth-stencil</a> state of the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-omgetrendertargets">OMGetRenderTargets</a>
</td>
<td align="left" width="63%">
Get pointers to the render targets and the depth-stencil buffer that are available to the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">output-merger stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-omsetblendstate">OMSetBlendState</a>
</td>
<td align="left" width="63%">
Set the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">blend state</a> of the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-omsetdepthstencilstate">OMSetDepthStencilState</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">depth-stencil</a> state of 
    the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-omsetrendertargets">OMSetRenderTargets</a>
</td>
<td align="left" width="63%">
Bind one or more render targets and the depth-stencil buffer to the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">output-merger stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-opensharedresource">OpenSharedResource</a>
</td>
<td align="left" width="63%">
Give a device access to a shared resource created on a different Direct3d device. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-psgetconstantbuffers">PSGetConstantBuffers</a>
</td>
<td align="left" width="63%">
Get the <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">constant buffers</a> used by the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/geometry-shader-stage">pixel shader</a> pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-psgetsamplers">PSGetSamplers</a>
</td>
<td align="left" width="63%">
Get an array of sampler states from the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/geometry-shader-stage">pixel shader</a> pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-psgetshader">PSGetShader</a>
</td>
<td align="left" width="63%">
Get the pixel shader currently set on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-psgetshaderresources">PSGetShaderResources</a>
</td>
<td align="left" width="63%">
Get the pixel shader resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetconstantbuffers">PSSetConstantBuffers</a>
</td>
<td align="left" width="63%">
Set the <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">constant buffers</a> used by the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/geometry-shader-stage">pixel shader</a> pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetsamplers">PSSetSamplers</a>
</td>
<td align="left" width="63%">
Set an array of sampler states to the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/geometry-shader-stage">pixel shader</a> pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetshader">PSSetShader</a>
</td>
<td align="left" width="63%">
Sets a pixel shader to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetshaderresources">PSSetShaderResources</a>
</td>
<td align="left" width="63%">
Bind an array of shader resources to the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/geometry-shader-stage">pixel shader stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-resolvesubresource">ResolveSubresource</a>
</td>
<td align="left" width="63%">
Copy a multisampled resource into a non-multisampled resource. This API is most useful when re-using the resulting rendertarget of one render pass as an input to a second render pass.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-rsgetscissorrects">RSGetScissorRects</a>
</td>
<td align="left" width="63%">
Get the array of <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage-getting-started">scissor rectangles</a> bound to the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage">rasterizer stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-rsgetstate">RSGetState</a>
</td>
<td align="left" width="63%">
Get the <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ns-d3d10-d3d10_rasterizer_desc">rasterizer state</a> from the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage">rasterizer stage</a> of the pipeline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-rsgetviewports">RSGetViewports</a>
</td>
<td align="left" width="63%">
Get the array of <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage-getting-started">viewports</a> bound 
    to the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage">rasterizer stage</a>


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-rssetscissorrects">RSSetScissorRects</a>
</td>
<td align="left" width="63%">
Bind an array of <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage-getting-started">scissor rectangles</a> to the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage">rasterizer stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-rssetstate">RSSetState</a>
</td>
<td align="left" width="63%">
Set the <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ns-d3d10-d3d10_rasterizer_desc">rasterizer state</a> for the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage">rasterizer stage</a> of the pipeline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-rssetviewports">RSSetViewports</a>
</td>
<td align="left" width="63%">
Bind an array of <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage-getting-started">viewports</a> to the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage">rasterizer stage</a> of the pipeline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-setexceptionmode">SetExceptionMode</a>
</td>
<td align="left" width="63%">
Get the exception-mode flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-setpredication">SetPredication</a>
</td>
<td align="left" width="63%">
Set a rendering predicate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-setprivatedata">SetPrivateData</a>
</td>
<td align="left" width="63%">
Set data to a device and associate that data with a guid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-setprivatedatainterface">SetPrivateDataInterface</a>
</td>
<td align="left" width="63%">
Associate an <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>-derived interface with this device and associate that interface with an application-defined guid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-settextfiltersize">SetTextFilterSize</a>
</td>
<td align="left" width="63%">
This method is not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-sogettargets">SOGetTargets</a>
</td>
<td align="left" width="63%">
Get the target output <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">buffers</a> for the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage">StreamOutput</a> stage of the pipeline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-sosettargets">SOSetTargets</a>
</td>
<td align="left" width="63%">
Set the target output <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">buffers</a> for the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage">StreamOutput</a> stage, which enables/disables the pipeline to stream-out data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-updatesubresource">UpdateSubresource</a>
</td>
<td align="left" width="63%">
The CPU copies data from memory to a <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">subresource</a> created in non-mappable memory. See remarks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vsgetconstantbuffers">VSGetConstantBuffers</a>
</td>
<td align="left" width="63%">
Get the <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">constant buffers</a> used by the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/geometry-shader-stage">vertex shader</a> pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vsgetsamplers">VSGetSamplers</a>
</td>
<td align="left" width="63%">
Get an array of sampler states from the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/geometry-shader-stage">vertex shader</a> pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vsgetshader">VSGetShader</a>
</td>
<td align="left" width="63%">
Get the vertex shader currently set on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vsgetshaderresources">VSGetShaderResources</a>
</td>
<td align="left" width="63%">
Get the vertex shader resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetconstantbuffers">VSSetConstantBuffers</a>
</td>
<td align="left" width="63%">
Set the <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">constant buffers</a> used by the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/geometry-shader-stage">vertex shader</a> pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetsamplers">VSSetSamplers</a>
</td>
<td align="left" width="63%">
Set an array of sampler states to the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/geometry-shader-stage">vertex shader</a> pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetshader">VSSetShader</a>
</td>
<td align="left" width="63%">
Set a vertex shader to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetshaderresources">VSSetShaderResources</a>
</td>
<td align="left" width="63%">
Bind an array of shader resources to the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/geometry-shader-stage">vertex shader stage</a>.

</td>
</tr>
</table> 


## -remarks



A device is created using <a href="https://docs.microsoft.com/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice">D3D10CreateDevice</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-interfaces">Core Interfaces</a>
 

 

