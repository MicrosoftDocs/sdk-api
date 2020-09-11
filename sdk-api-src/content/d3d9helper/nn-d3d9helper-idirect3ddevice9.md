---
UID: NN:d3d9helper.IDirect3DDevice9
title: IDirect3DDevice9 (d3d9helper.h)
description: Applications use the methods of the IDirect3DDevice9 interface to perform DrawPrimitive-based rendering, create resources, work with system-level variables, adjust gamma ramp levels, work with palettes, and create shaders.
helpviewer_keywords: ["28be25f8-38cf-f9e4-3aac-15cad98cac63","IDirect3DDevice9","IDirect3DDevice9 interface [Direct3D 9]","IDirect3DDevice9 interface [Direct3D 9]","described","d3d9helper/IDirect3DDevice9","direct3d9.idirect3ddevice9"]
old-location: direct3d9\idirect3ddevice9.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9.htm
ms.date: 12/05/2018
ms.keywords: 28be25f8-38cf-f9e4-3aac-15cad98cac63, IDirect3DDevice9, IDirect3DDevice9 interface [Direct3D 9], IDirect3DDevice9 interface [Direct3D 9],described, d3d9helper/IDirect3DDevice9, direct3d9.idirect3ddevice9
req.header: d3d9helper.h
req.include-header: D3D9.h
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
req.lib: D3d9.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3DDevice9
 - d3d9helper/IDirect3DDevice9
dev_langs:
 - c++
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
---

# IDirect3DDevice9 interface


## -description

Applications use the methods of the IDirect3DDevice9 interface to perform DrawPrimitive-based rendering, create resources, work with system-level variables, adjust gamma ramp levels, work with palettes, and create shaders.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DDevice9</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirect3DDevice9</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-beginscene">BeginScene</a>
</td>
<td align="left" width="63%">
Begins a scene. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-beginstateblock">BeginStateBlock</a>
</td>
<td align="left" width="63%">
Signals Direct3D to begin recording a device-state block.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-clear">Clear</a>
</td>
<td align="left" width="63%">
Clears one or more surfaces such as a render target, <a href="https://docs.microsoft.com/windows/desktop/direct3d9/multiple-render-targets">multiple render targets</a>, a stencil buffer, and a depth buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-colorfill">ColorFill</a>
</td>
<td align="left" width="63%">
Allows an application to fill a rectangular area of a D3DPOOL_DEFAULT surface with a specified color.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createadditionalswapchain">CreateAdditionalSwapChain</a>
</td>
<td align="left" width="63%">
Creates an additional swap chain for rendering multiple views.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createcubetexture">CreateCubeTexture</a>
</td>
<td align="left" width="63%">
Creates a cube texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createdepthstencilsurface">CreateDepthStencilSurface</a>
</td>
<td align="left" width="63%">
Creates a depth-stencil resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createindexbuffer">CreateIndexBuffer</a>
</td>
<td align="left" width="63%">
Creates an index buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createoffscreenplainsurface">CreateOffscreenPlainSurface</a>
</td>
<td align="left" width="63%">
Create an off-screen surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createpixelshader">CreatePixelShader</a>
</td>
<td align="left" width="63%">
Creates a pixel shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createquery">CreateQuery</a>
</td>
<td align="left" width="63%">
Creates a status query.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createrendertarget">CreateRenderTarget</a>
</td>
<td align="left" width="63%">
Creates a render-target surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createstateblock">CreateStateBlock</a>
</td>
<td align="left" width="63%">
Creates a new state block that contains the values for all device states, vertex-related states, or pixel-related states.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createtexture">CreateTexture</a>
</td>
<td align="left" width="63%">
Creates a texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvertexbuffer">CreateVertexBuffer</a>
</td>
<td align="left" width="63%">
Creates a vertex buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvertexdeclaration">CreateVertexDeclaration</a>
</td>
<td align="left" width="63%">
Create a vertex shader declaration from the device and the vertex elements.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvertexshader">CreateVertexShader</a>
</td>
<td align="left" width="63%">
Creates a vertex shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvolumetexture">CreateVolumeTexture</a>
</td>
<td align="left" width="63%">
Creates a volume texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-deletepatch">DeletePatch</a>
</td>
<td align="left" width="63%">
Frees a cached high-order patch.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawindexedprimitive">DrawIndexedPrimitive</a>
</td>
<td align="left" width="63%">
Based on indexing, renders the specified geometric primitive into an array of vertices.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawindexedprimitiveup">DrawIndexedPrimitiveUP</a>
</td>
<td align="left" width="63%">
Renders the specified geometric primitive with data specified by a user memory pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawprimitive">DrawPrimitive</a>
</td>
<td align="left" width="63%">
Renders a sequence of nonindexed, geometric primitives of the specified type from the current set of data input streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawprimitiveup">DrawPrimitiveUP</a>
</td>
<td align="left" width="63%">
Renders data specified by a user memory pointer as a sequence of geometric primitives of the specified type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawrectpatch">DrawRectPatch</a>
</td>
<td align="left" width="63%">
Draws a rectangular patch using the currently set streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawtripatch">DrawTriPatch</a>
</td>
<td align="left" width="63%">
Draws a triangular patch using the currently set streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-endscene">EndScene</a>
</td>
<td align="left" width="63%">
Ends a scene that was begun by calling <a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-beginscene">IDirect3DDevice9::BeginScene</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-endstateblock">EndStateBlock</a>
</td>
<td align="left" width="63%">
Signals Direct3D to stop recording a device-state block and retrieve a pointer to the state block interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-evictmanagedresources">EvictManagedResources</a>
</td>
<td align="left" width="63%">
Evicts all managed resources, including both Direct3D and driver-managed resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getavailabletexturemem">GetAvailableTextureMem</a>
</td>
<td align="left" width="63%">
Returns an estimate of the amount of available texture memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getbackbuffer">GetBackBuffer</a>
</td>
<td align="left" width="63%">
Retrieves a back buffer from the device's swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getclipplane">GetClipPlane</a>
</td>
<td align="left" width="63%">
Retrieves the coefficients of a user-defined clipping plane for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getclipstatus">GetClipStatus</a>
</td>
<td align="left" width="63%">
Retrieves the clip status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getcreationparameters">GetCreationParameters</a>
</td>
<td align="left" width="63%">
Retrieves the creation parameters of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getcurrenttexturepalette">GetCurrentTexturePalette</a>
</td>
<td align="left" width="63%">
Retrieves the current texture palette.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getdepthstencilsurface">GetDepthStencilSurface</a>
</td>
<td align="left" width="63%">
Gets the depth-stencil surface owned by the Direct3DDevice object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getdevicecaps">GetDeviceCaps</a>
</td>
<td align="left" width="63%">
Retrieves the capabilities of the rendering device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getdirect3d">GetDirect3D</a>
</td>
<td align="left" width="63%">
Returns an interface to the instance of the Direct3D object that created the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getdisplaymode">GetDisplayMode</a>
</td>
<td align="left" width="63%">
Retrieves the display mode's spatial resolution, color resolution, and refresh frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getfrontbufferdata">GetFrontBufferData</a>
</td>
<td align="left" width="63%">
Generates a copy of the device's front buffer and places that copy in a system memory buffer provided by the application. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getfvf">GetFVF</a>
</td>
<td align="left" width="63%">
Gets the fixed vertex function declaration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getgammaramp">GetGammaRamp</a>
</td>
<td align="left" width="63%">
Retrieves the gamma correction ramp for the swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getindices">GetIndices</a>
</td>
<td align="left" width="63%">
Retrieves index data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getlight">GetLight</a>
</td>
<td align="left" width="63%">
Retrieves a set of lighting properties that this device uses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getlightenable">GetLightEnable</a>
</td>
<td align="left" width="63%">
Retrieves the activity status - enabled or disabled - for a set of lighting parameters within a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getmaterial">GetMaterial</a>
</td>
<td align="left" width="63%">
Retrieves the current material properties for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getnpatchmode">GetNPatchMode</a>
</td>
<td align="left" width="63%">
Gets the N-patch mode segments.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getnumberofswapchains">GetNumberOfSwapChains</a>
</td>
<td align="left" width="63%">
Gets the number of implicit swap chains.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getpaletteentries">GetPaletteEntries</a>
</td>
<td align="left" width="63%">
Retrieves palette entries.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getpixelshader">GetPixelShader</a>
</td>
<td align="left" width="63%">
Retrieves the currently set pixel shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getpixelshaderconstantb">GetPixelShaderConstantB</a>
</td>
<td align="left" width="63%">
Gets a Boolean shader constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getpixelshaderconstantf">GetPixelShaderConstantF</a>
</td>
<td align="left" width="63%">
Gets a floating-point shader constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getpixelshaderconstanti">GetPixelShaderConstantI</a>
</td>
<td align="left" width="63%">
Gets an integer shader constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getrasterstatus">GetRasterStatus</a>
</td>
<td align="left" width="63%">
Returns information describing the raster of the monitor on which the swap chain is presented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getrenderstate">GetRenderState</a>
</td>
<td align="left" width="63%">
Retrieves a render-state value for a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getrendertarget">GetRenderTarget</a>
</td>
<td align="left" width="63%">
Retrieves a render-target surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getrendertargetdata">GetRenderTargetData</a>
</td>
<td align="left" width="63%">
Copies the render-target data from device memory to system memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getsamplerstate">GetSamplerState</a>
</td>
<td align="left" width="63%">
Gets the sampler state value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getscissorrect">GetScissorRect</a>
</td>
<td align="left" width="63%">
Gets the scissor rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getsoftwarevertexprocessing">GetSoftwareVertexProcessing</a>
</td>
<td align="left" width="63%">
Gets the vertex processing (hardware or software) mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getstreamsource">GetStreamSource</a>
</td>
<td align="left" width="63%">
Retrieves a vertex buffer bound to the specified data stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getstreamsourcefreq">GetStreamSourceFreq</a>
</td>
<td align="left" width="63%">
Gets the stream source frequency divider value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getswapchain">GetSwapChain</a>
</td>
<td align="left" width="63%">
Gets a pointer to a swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-gettexture">GetTexture</a>
</td>
<td align="left" width="63%">
Retrieves a texture assigned to a stage for a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-gettexturestagestate">GetTextureStageState</a>
</td>
<td align="left" width="63%">
Retrieves a state value for an assigned texture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-gettransform">GetTransform</a>
</td>
<td align="left" width="63%">
Retrieves a matrix describing a transformation state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getvertexdeclaration">GetVertexDeclaration</a>
</td>
<td align="left" width="63%">
Gets a vertex shader declaration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getvertexshader">GetVertexShader</a>
</td>
<td align="left" width="63%">
Retrieves the currently set vertex shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getvertexshaderconstantb">GetVertexShaderConstantB</a>
</td>
<td align="left" width="63%">
Gets a Boolean vertex shader constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getvertexshaderconstantf">GetVertexShaderConstantF</a>
</td>
<td align="left" width="63%">
Gets a floating-point vertex shader constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getvertexshaderconstanti">GetVertexShaderConstantI</a>
</td>
<td align="left" width="63%">
Gets an integer vertex shader constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getviewport">GetViewport</a>
</td>
<td align="left" width="63%">
Retrieves the viewport parameters currently set for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-lightenable">LightEnable</a>
</td>
<td align="left" width="63%">
Enables or disables a set of lighting parameters within a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-multiplytransform">MultiplyTransform</a>
</td>
<td align="left" width="63%">
Multiplies a device's world, view, or projection matrices by a specified matrix. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-present">Present</a>
</td>
<td align="left" width="63%">
Presents the contents of the next buffer in the sequence of back buffers owned by the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-processvertices">ProcessVertices</a>
</td>
<td align="left" width="63%">
Applies the vertex processing defined by the vertex shader to the set of input data streams, generating a single stream of interleaved vertex data to the destination vertex buffer. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the type, size, and format of the swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane">SetClipPlane</a>
</td>
<td align="left" width="63%">
Sets the coefficients of a user-defined clipping plane for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipstatus">SetClipStatus</a>
</td>
<td align="left" width="63%">
Sets the clip status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setcurrenttexturepalette">SetCurrentTexturePalette</a>
</td>
<td align="left" width="63%">
Sets the current texture palette.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setcursorposition">SetCursorPosition</a>
</td>
<td align="left" width="63%">
Sets the cursor position and update options.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setcursorproperties">SetCursorProperties</a>
</td>
<td align="left" width="63%">
Sets properties for the cursor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setdepthstencilsurface">SetDepthStencilSurface</a>
</td>
<td align="left" width="63%">
Sets the depth stencil surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setdialogboxmode">SetDialogBoxMode</a>
</td>
<td align="left" width="63%">
This method allows the use of GDI dialog boxes in full-screen mode applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setfvf">SetFVF</a>
</td>
<td align="left" width="63%">
Sets the current vertex stream declaration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setgammaramp">SetGammaRamp</a>
</td>
<td align="left" width="63%">
Sets the gamma correction ramp for the implicit swap chain. This method will affect the entire screen (not just the active window if you are running in windowed mode).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setindices">SetIndices</a>
</td>
<td align="left" width="63%">
Sets index data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight">SetLight</a>
</td>
<td align="left" width="63%">
Assigns a set of lighting properties for this device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial">SetMaterial</a>
</td>
<td align="left" width="63%">
Sets the material properties for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode">SetNPatchMode</a>
</td>
<td align="left" width="63%">
Enable or disable N-patches.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpaletteentries">SetPaletteEntries</a>
</td>
<td align="left" width="63%">
Sets palette entries.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader">SetPixelShader</a>
</td>
<td align="left" width="63%">
Sets the current pixel shader to a previously created pixel shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb">SetPixelShaderConstantB</a>
</td>
<td align="left" width="63%">
Sets a Boolean shader constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf">SetPixelShaderConstantF</a>
</td>
<td align="left" width="63%">
Sets a floating-point shader constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti">SetPixelShaderConstantI</a>
</td>
<td align="left" width="63%">
Sets an integer shader constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate">SetRenderState</a>
</td>
<td align="left" width="63%">
Sets a single device render-state parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget">SetRenderTarget</a>
</td>
<td align="left" width="63%">
Sets a new color buffer for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate">SetSamplerState</a>
</td>
<td align="left" width="63%">
Sets the sampler state value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setscissorrect">SetScissorRect</a>
</td>
<td align="left" width="63%">
Sets the scissor rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsoftwarevertexprocessing">SetSoftwareVertexProcessing</a>
</td>
<td align="left" width="63%">
Use this method to switch between software and hardware vertex processing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource">SetStreamSource</a>
</td>
<td align="left" width="63%">
Binds a vertex buffer to a device data stream. For more information, see <a href="https://docs.microsoft.com/windows/desktop/direct3d9/setting-the-stream-source">Setting the Stream Source (Direct3D 9)</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq">SetStreamSourceFreq</a>
</td>
<td align="left" width="63%">
Sets the stream source frequency divider value. This may be used to draw several instances of geometry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture">SetTexture</a>
</td>
<td align="left" width="63%">
Assigns a texture to a stage for a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate">SetTextureStageState</a>
</td>
<td align="left" width="63%">
Sets the state value for the currently assigned texture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform">SetTransform</a>
</td>
<td align="left" width="63%">
Sets a single device transformation-related state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexdeclaration">SetVertexDeclaration</a>
</td>
<td align="left" width="63%">
Sets a <a href="https://docs.microsoft.com/windows/desktop/direct3d9/vertex-declaration">Vertex Declaration (Direct3D 9)</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader">SetVertexShader</a>
</td>
<td align="left" width="63%">
Sets the vertex shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb">SetVertexShaderConstantB</a>
</td>
<td align="left" width="63%">
Sets a Boolean vertex shader constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf">SetVertexShaderConstantF</a>
</td>
<td align="left" width="63%">
Sets a floating-point vertex shader constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti">SetVertexShaderConstantI</a>
</td>
<td align="left" width="63%">
Sets an integer vertex shader constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport">SetViewport</a>
</td>
<td align="left" width="63%">
Sets the viewport parameters for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-showcursor">ShowCursor</a>
</td>
<td align="left" width="63%">
Displays or hides the cursor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect">StretchRect</a>
</td>
<td align="left" width="63%">
Copy the contents of the source rectangle to the destination rectangle. The source rectangle can be stretched and filtered by the copy. This function is often used to change the aspect ratio of a video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel">TestCooperativeLevel</a>
</td>
<td align="left" width="63%">
Reports the current cooperative-level status of the Direct3D device for a windowed or full-screen application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatesurface">UpdateSurface</a>
</td>
<td align="left" width="63%">
Copies rectangular subsets of pixels from one surface to another. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatetexture">UpdateTexture</a>
</td>
<td align="left" width="63%">
Updates the dirty portions of a texture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-validatedevice">ValidateDevice</a>
</td>
<td align="left" width="63%">
Reports the device's ability to render the current texture-blending operations and arguments in a single pass.

</td>
</tr>
</table>

## -remarks

The <b>IDirect3DDevice9</b> interface is obtained by calling the <a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-createdevice">IDirect3D9::CreateDevice</a> method.

This interface, like all COM interfaces, inherits the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface methods.

The LPDIRECT3DDEVICE9 and PDIRECT3DDEVICE9 types are defined as pointers to the <b>IDirect3DDevice9</b> interface.


```

typedef struct IDirect3DDevice9 *LPDIRECT3DDEVICE9, *PDIRECT3DDEVICE9;

```

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/direct3d9/dx9-graphics-reference-d3d-interfaces">Direct3D Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-createdevice">IDirect3D9::CreateDevice</a>

