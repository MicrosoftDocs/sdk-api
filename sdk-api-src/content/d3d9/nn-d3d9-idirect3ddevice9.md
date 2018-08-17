---
UID: NN:d3d9.IDirect3DDevice9
title: IDirect3DDevice9
author: windows-sdk-content
description: Applications use the methods of the IDirect3DDevice9 interface to perform DrawPrimitive-based rendering, create resources, work with system-level variables, adjust gamma ramp levels, work with palettes, and create shaders.
old-location: direct3d9\idirect3ddevice9.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 28be25f8-38cf-f9e4-3aac-15cad98cac63, IDirect3DDevice9, IDirect3DDevice9 interface [Direct3D 9], IDirect3DDevice9 interface [Direct3D 9],described, d3d9helper/IDirect3DDevice9, direct3d9.idirect3ddevice9
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d9.h
req.include-header: D3D9.h
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
req.typenames: D3D12_SIGNATURE_PARAMETER_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d9.lib
 - d3d9.dll
api_name:
 - IDirect3DDevice9
product: Windows
targetos: Windows
req.lib: D3d9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9 interface


## -description


Applications use the methods of the IDirect3DDevice9 interface to perform DrawPrimitive-based rendering, create resources, work with system-level variables, adjust gamma ramp levels, work with palettes, and create shaders.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DDevice9</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirect3DDevice9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirect3DDevice9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174350(v=VS.85).aspx">BeginScene</a>
</td>
<td align="left" width="63%">
Begins a scene. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174351(v=VS.85).aspx">BeginStateBlock</a>
</td>
<td align="left" width="63%">
Signals Direct3D to begin recording a device-state block.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174352(v=VS.85).aspx">Clear</a>
</td>
<td align="left" width="63%">
Clears one or more surfaces such as a render target, <a href="https://msdn.microsoft.com/en-us/library/Bb147221(v=VS.85).aspx">multiple render targets</a>, a stencil buffer, and a depth buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174353(v=VS.85).aspx">ColorFill</a>
</td>
<td align="left" width="63%">
Allows an application to fill a rectangular area of a D3DPOOL_DEFAULT surface with a specified color.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174354(v=VS.85).aspx">CreateAdditionalSwapChain</a>
</td>
<td align="left" width="63%">
Creates an additional swap chain for rendering multiple views.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174355(v=VS.85).aspx">CreateCubeTexture</a>
</td>
<td align="left" width="63%">
Creates a cube texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174356(v=VS.85).aspx">CreateDepthStencilSurface</a>
</td>
<td align="left" width="63%">
Creates a depth-stencil resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174357(v=VS.85).aspx">CreateIndexBuffer</a>
</td>
<td align="left" width="63%">
Creates an index buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174358(v=VS.85).aspx">CreateOffscreenPlainSurface</a>
</td>
<td align="left" width="63%">
Create an off-screen surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174359(v=VS.85).aspx">CreatePixelShader</a>
</td>
<td align="left" width="63%">
Creates a pixel shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174360(v=VS.85).aspx">CreateQuery</a>
</td>
<td align="left" width="63%">
Creates a status query.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174361(v=VS.85).aspx">CreateRenderTarget</a>
</td>
<td align="left" width="63%">
Creates a render-target surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174362(v=VS.85).aspx">CreateStateBlock</a>
</td>
<td align="left" width="63%">
Creates a new state block that contains the values for all device states, vertex-related states, or pixel-related states.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174363(v=VS.85).aspx">CreateTexture</a>
</td>
<td align="left" width="63%">
Creates a texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174364(v=VS.85).aspx">CreateVertexBuffer</a>
</td>
<td align="left" width="63%">
Creates a vertex buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174365(v=VS.85).aspx">CreateVertexDeclaration</a>
</td>
<td align="left" width="63%">
Create a vertex shader declaration from the device and the vertex elements.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174366(v=VS.85).aspx">CreateVertexShader</a>
</td>
<td align="left" width="63%">
Creates a vertex shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174367(v=VS.85).aspx">CreateVolumeTexture</a>
</td>
<td align="left" width="63%">
Creates a volume texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174368(v=VS.85).aspx">DeletePatch</a>
</td>
<td align="left" width="63%">
Frees a cached high-order patch.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174369(v=VS.85).aspx">DrawIndexedPrimitive</a>
</td>
<td align="left" width="63%">
Based on indexing, renders the specified geometric primitive into an array of vertices.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174370(v=VS.85).aspx">DrawIndexedPrimitiveUP</a>
</td>
<td align="left" width="63%">
Renders the specified geometric primitive with data specified by a user memory pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174371(v=VS.85).aspx">DrawPrimitive</a>
</td>
<td align="left" width="63%">
Renders a sequence of nonindexed, geometric primitives of the specified type from the current set of data input streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174372(v=VS.85).aspx">DrawPrimitiveUP</a>
</td>
<td align="left" width="63%">
Renders data specified by a user memory pointer as a sequence of geometric primitives of the specified type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174373(v=VS.85).aspx">DrawRectPatch</a>
</td>
<td align="left" width="63%">
Draws a rectangular patch using the currently set streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174374(v=VS.85).aspx">DrawTriPatch</a>
</td>
<td align="left" width="63%">
Draws a triangular patch using the currently set streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174375(v=VS.85).aspx">EndScene</a>
</td>
<td align="left" width="63%">
Ends a scene that was begun by calling <a href="https://msdn.microsoft.com/en-us/library/Bb174350(v=VS.85).aspx">IDirect3DDevice9::BeginScene</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174376(v=VS.85).aspx">EndStateBlock</a>
</td>
<td align="left" width="63%">
Signals Direct3D to stop recording a device-state block and retrieve a pointer to the state block interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174377(v=VS.85).aspx">EvictManagedResources</a>
</td>
<td align="left" width="63%">
Evicts all managed resources, including both Direct3D and driver-managed resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174378(v=VS.85).aspx">GetAvailableTextureMem</a>
</td>
<td align="left" width="63%">
Returns an estimate of the amount of available texture memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174379(v=VS.85).aspx">GetBackBuffer</a>
</td>
<td align="left" width="63%">
Retrieves a back buffer from the device's swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174380(v=VS.85).aspx">GetClipPlane</a>
</td>
<td align="left" width="63%">
Retrieves the coefficients of a user-defined clipping plane for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174381(v=VS.85).aspx">GetClipStatus</a>
</td>
<td align="left" width="63%">
Retrieves the clip status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174382(v=VS.85).aspx">GetCreationParameters</a>
</td>
<td align="left" width="63%">
Retrieves the creation parameters of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174383(v=VS.85).aspx">GetCurrentTexturePalette</a>
</td>
<td align="left" width="63%">
Retrieves the current texture palette.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174384(v=VS.85).aspx">GetDepthStencilSurface</a>
</td>
<td align="left" width="63%">
Gets the depth-stencil surface owned by the Direct3DDevice object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174385(v=VS.85).aspx">GetDeviceCaps</a>
</td>
<td align="left" width="63%">
Retrieves the capabilities of the rendering device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174386(v=VS.85).aspx">GetDirect3D</a>
</td>
<td align="left" width="63%">
Returns an interface to the instance of the Direct3D object that created the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174387(v=VS.85).aspx">GetDisplayMode</a>
</td>
<td align="left" width="63%">
Retrieves the display mode's spatial resolution, color resolution, and refresh frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174388(v=VS.85).aspx">GetFrontBufferData</a>
</td>
<td align="left" width="63%">
Generates a copy of the device's front buffer and places that copy in a system memory buffer provided by the application. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174389(v=VS.85).aspx">GetFVF</a>
</td>
<td align="left" width="63%">
Gets the fixed vertex function declaration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174390(v=VS.85).aspx">GetGammaRamp</a>
</td>
<td align="left" width="63%">
Retrieves the gamma correction ramp for the swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174391(v=VS.85).aspx">GetIndices</a>
</td>
<td align="left" width="63%">
Retrieves index data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174392(v=VS.85).aspx">GetLight</a>
</td>
<td align="left" width="63%">
Retrieves a set of lighting properties that this device uses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174393(v=VS.85).aspx">GetLightEnable</a>
</td>
<td align="left" width="63%">
Retrieves the activity status - enabled or disabled - for a set of lighting parameters within a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174394(v=VS.85).aspx">GetMaterial</a>
</td>
<td align="left" width="63%">
Retrieves the current material properties for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174395(v=VS.85).aspx">GetNPatchMode</a>
</td>
<td align="left" width="63%">
Gets the N-patch mode segments.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174396(v=VS.85).aspx">GetNumberOfSwapChains</a>
</td>
<td align="left" width="63%">
Gets the number of implicit swap chains.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174397(v=VS.85).aspx">GetPaletteEntries</a>
</td>
<td align="left" width="63%">
Retrieves palette entries.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174398(v=VS.85).aspx">GetPixelShader</a>
</td>
<td align="left" width="63%">
Retrieves the currently set pixel shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174399(v=VS.85).aspx">GetPixelShaderConstantB</a>
</td>
<td align="left" width="63%">
Gets a Boolean shader constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174400(v=VS.85).aspx">GetPixelShaderConstantF</a>
</td>
<td align="left" width="63%">
Gets a floating-point shader constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174401(v=VS.85).aspx">GetPixelShaderConstantI</a>
</td>
<td align="left" width="63%">
Gets an integer shader constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174402(v=VS.85).aspx">GetRasterStatus</a>
</td>
<td align="left" width="63%">
Returns information describing the raster of the monitor on which the swap chain is presented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174403(v=VS.85).aspx">GetRenderState</a>
</td>
<td align="left" width="63%">
Retrieves a render-state value for a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174404(v=VS.85).aspx">GetRenderTarget</a>
</td>
<td align="left" width="63%">
Retrieves a render-target surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174405(v=VS.85).aspx">GetRenderTargetData</a>
</td>
<td align="left" width="63%">
Copies the render-target data from device memory to system memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174406(v=VS.85).aspx">GetSamplerState</a>
</td>
<td align="left" width="63%">
Gets the sampler state value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174407(v=VS.85).aspx">GetScissorRect</a>
</td>
<td align="left" width="63%">
Gets the scissor rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174408(v=VS.85).aspx">GetSoftwareVertexProcessing</a>
</td>
<td align="left" width="63%">
Gets the vertex processing (hardware or software) mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174409(v=VS.85).aspx">GetStreamSource</a>
</td>
<td align="left" width="63%">
Retrieves a vertex buffer bound to the specified data stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174410(v=VS.85).aspx">GetStreamSourceFreq</a>
</td>
<td align="left" width="63%">
Gets the stream source frequency divider value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174411(v=VS.85).aspx">GetSwapChain</a>
</td>
<td align="left" width="63%">
Gets a pointer to a swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174412(v=VS.85).aspx">GetTexture</a>
</td>
<td align="left" width="63%">
Retrieves a texture assigned to a stage for a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174413(v=VS.85).aspx">GetTextureStageState</a>
</td>
<td align="left" width="63%">
Retrieves a state value for an assigned texture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174414(v=VS.85).aspx">GetTransform</a>
</td>
<td align="left" width="63%">
Retrieves a matrix describing a transformation state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174415(v=VS.85).aspx">GetVertexDeclaration</a>
</td>
<td align="left" width="63%">
Gets a vertex shader declaration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174416(v=VS.85).aspx">GetVertexShader</a>
</td>
<td align="left" width="63%">
Retrieves the currently set vertex shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174417(v=VS.85).aspx">GetVertexShaderConstantB</a>
</td>
<td align="left" width="63%">
Gets a Boolean vertex shader constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174418(v=VS.85).aspx">GetVertexShaderConstantF</a>
</td>
<td align="left" width="63%">
Gets a floating-point vertex shader constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174419(v=VS.85).aspx">GetVertexShaderConstantI</a>
</td>
<td align="left" width="63%">
Gets an integer vertex shader constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174420(v=VS.85).aspx">GetViewport</a>
</td>
<td align="left" width="63%">
Retrieves the viewport parameters currently set for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174421(v=VS.85).aspx">LightEnable</a>
</td>
<td align="left" width="63%">
Enables or disables a set of lighting parameters within a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174422(v=VS.85).aspx">MultiplyTransform</a>
</td>
<td align="left" width="63%">
Multiplies a device's world, view, or projection matrices by a specified matrix. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174423(v=VS.85).aspx">Present</a>
</td>
<td align="left" width="63%">
Presents the contents of the next buffer in the sequence of back buffers owned by the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174424(v=VS.85).aspx">ProcessVertices</a>
</td>
<td align="left" width="63%">
Applies the vertex processing defined by the vertex shader to the set of input data streams, generating a single stream of interleaved vertex data to the destination vertex buffer. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174425(v=VS.85).aspx">Reset</a>
</td>
<td align="left" width="63%">
Resets the type, size, and format of the swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174426(v=VS.85).aspx">SetClipPlane</a>
</td>
<td align="left" width="63%">
Sets the coefficients of a user-defined clipping plane for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174427(v=VS.85).aspx">SetClipStatus</a>
</td>
<td align="left" width="63%">
Sets the clip status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174428(v=VS.85).aspx">SetCurrentTexturePalette</a>
</td>
<td align="left" width="63%">
Sets the current texture palette.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174429(v=VS.85).aspx">SetCursorPosition</a>
</td>
<td align="left" width="63%">
Sets the cursor position and update options.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174430(v=VS.85).aspx">SetCursorProperties</a>
</td>
<td align="left" width="63%">
Sets properties for the cursor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174431(v=VS.85).aspx">SetDepthStencilSurface</a>
</td>
<td align="left" width="63%">
Sets the depth stencil surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174432(v=VS.85).aspx">SetDialogBoxMode</a>
</td>
<td align="left" width="63%">
This method allows the use of GDI dialog boxes in full-screen mode applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174433(v=VS.85).aspx">SetFVF</a>
</td>
<td align="left" width="63%">
Sets the current vertex stream declaration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174434(v=VS.85).aspx">SetGammaRamp</a>
</td>
<td align="left" width="63%">
Sets the gamma correction ramp for the implicit swap chain. This method will affect the entire screen (not just the active window if you are running in windowed mode).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174435(v=VS.85).aspx">SetIndices</a>
</td>
<td align="left" width="63%">
Sets index data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174436(v=VS.85).aspx">SetLight</a>
</td>
<td align="left" width="63%">
Assigns a set of lighting properties for this device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174437(v=VS.85).aspx">SetMaterial</a>
</td>
<td align="left" width="63%">
Sets the material properties for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174438(v=VS.85).aspx">SetNPatchMode</a>
</td>
<td align="left" width="63%">
Enable or disable N-patches.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174439(v=VS.85).aspx">SetPaletteEntries</a>
</td>
<td align="left" width="63%">
Sets palette entries.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174450(v=VS.85).aspx">SetPixelShader</a>
</td>
<td align="left" width="63%">
Sets the current pixel shader to a previously created pixel shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174451(v=VS.85).aspx">SetPixelShaderConstantB</a>
</td>
<td align="left" width="63%">
Sets a Boolean shader constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174452(v=VS.85).aspx">SetPixelShaderConstantF</a>
</td>
<td align="left" width="63%">
Sets a floating-point shader constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174453(v=VS.85).aspx">SetPixelShaderConstantI</a>
</td>
<td align="left" width="63%">
Sets an integer shader constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174454(v=VS.85).aspx">SetRenderState</a>
</td>
<td align="left" width="63%">
Sets a single device render-state parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174455(v=VS.85).aspx">SetRenderTarget</a>
</td>
<td align="left" width="63%">
Sets a new color buffer for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174456(v=VS.85).aspx">SetSamplerState</a>
</td>
<td align="left" width="63%">
Sets the sampler state value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174457(v=VS.85).aspx">SetScissorRect</a>
</td>
<td align="left" width="63%">
Sets the scissor rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174458(v=VS.85).aspx">SetSoftwareVertexProcessing</a>
</td>
<td align="left" width="63%">
Use this method to switch between software and hardware vertex processing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174459(v=VS.85).aspx">SetStreamSource</a>
</td>
<td align="left" width="63%">
Binds a vertex buffer to a device data stream. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb147360(v=VS.85).aspx">Setting the Stream Source (Direct3D 9)</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174460(v=VS.85).aspx">SetStreamSourceFreq</a>
</td>
<td align="left" width="63%">
Sets the stream source frequency divider value. This may be used to draw several instances of geometry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174461(v=VS.85).aspx">SetTexture</a>
</td>
<td align="left" width="63%">
Assigns a texture to a stage for a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174462(v=VS.85).aspx">SetTextureStageState</a>
</td>
<td align="left" width="63%">
Sets the state value for the currently assigned texture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174463(v=VS.85).aspx">SetTransform</a>
</td>
<td align="left" width="63%">
Sets a single device transformation-related state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174464(v=VS.85).aspx">SetVertexDeclaration</a>
</td>
<td align="left" width="63%">
Sets a <a href="https://msdn.microsoft.com/en-us/library/Bb206335(v=VS.85).aspx">Vertex Declaration (Direct3D 9)</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174465(v=VS.85).aspx">SetVertexShader</a>
</td>
<td align="left" width="63%">
Sets the vertex shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174466(v=VS.85).aspx">SetVertexShaderConstantB</a>
</td>
<td align="left" width="63%">
Sets a Boolean vertex shader constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174467(v=VS.85).aspx">SetVertexShaderConstantF</a>
</td>
<td align="left" width="63%">
Sets a floating-point vertex shader constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174468(v=VS.85).aspx">SetVertexShaderConstantI</a>
</td>
<td align="left" width="63%">
Sets an integer vertex shader constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174469(v=VS.85).aspx">SetViewport</a>
</td>
<td align="left" width="63%">
Sets the viewport parameters for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174470(v=VS.85).aspx">ShowCursor</a>
</td>
<td align="left" width="63%">
Displays or hides the cursor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174471(v=VS.85).aspx">StretchRect</a>
</td>
<td align="left" width="63%">
Copy the contents of the source rectangle to the destination rectangle. The source rectangle can be stretched and filtered by the copy. This function is often used to change the aspect ratio of a video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174472(v=VS.85).aspx">TestCooperativeLevel</a>
</td>
<td align="left" width="63%">
Reports the current cooperative-level status of the Direct3D device for a windowed or full-screen application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb205857(v=VS.85).aspx">UpdateSurface</a>
</td>
<td align="left" width="63%">
Copies rectangular subsets of pixels from one surface to another. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb205858(v=VS.85).aspx">UpdateTexture</a>
</td>
<td align="left" width="63%">
Updates the dirty portions of a texture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb205859(v=VS.85).aspx">ValidateDevice</a>
</td>
<td align="left" width="63%">
Reports the device's ability to render the current texture-blending operations and arguments in a single pass.

</td>
</tr>
</table> 


## -remarks



The <b>IDirect3DDevice9</b> interface is obtained by calling the <a href="https://msdn.microsoft.com/en-us/library/Bb174313(v=VS.85).aspx">IDirect3D9::CreateDevice</a> method.

This interface, like all COM interfaces, inherits the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface methods.

The LPDIRECT3DDEVICE9 and PDIRECT3DDEVICE9 types are defined as pointers to the <b>IDirect3DDevice9</b> interface.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
typedef struct IDirect3DDevice9 *LPDIRECT3DDEVICE9, *PDIRECT3DDEVICE9;
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f12facdc-5a3f-4f89-8ae3-a322ef3389b2">Direct3D Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174313(v=VS.85).aspx">IDirect3D9::CreateDevice</a>
 

 

