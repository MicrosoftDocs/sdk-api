---
UID: NN:d3d9.IDirect3DDevice9
title: IDirect3DDevice9
author: windows-driver-content
description: Applications use the methods of the IDirect3DDevice9 interface to perform DrawPrimitive-based rendering, create resources, work with system-level variables, adjust gamma ramp levels, work with palettes, and create shaders.
old-location: direct3d9\idirect3ddevice9.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9.htm
ms.author: windowsdriverdev
ms.date: 4/10/2018
ms.keywords: 28be25f8-38cf-f9e4-3aac-15cad98cac63, IDirect3DDevice9, IDirect3DDevice9 interface [Direct3D 9], IDirect3DDevice9 interface [Direct3D 9], described, d3d9helper/IDirect3DDevice9, direct3d9.idirect3ddevice9
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: d3d9.h
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
req.typenames: D3D12_SIGNATURE_PARAMETER_DESC
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3d9.lib
-	d3d9.dll
api_name:
-	IDirect3DDevice9
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
<a href="https://msdn.microsoft.com/7fc1375d-b2de-4762-9963-8428938e499f">BeginScene</a>
</td>
<td align="left" width="63%">
Begins a scene. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee197fbc-d13b-42c2-a293-72306a0d05ce">BeginStateBlock</a>
</td>
<td align="left" width="63%">
Signals Direct3D to begin recording a device-state block.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406339">Clear</a>
</td>
<td align="left" width="63%">
Clears one or more surfaces such as a render target, <a href="https://msdn.microsoft.com/library/windows/hardware/hh998432">multiple render targets</a>, a stencil buffer, and a depth buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de8c1f15-cb82-4c20-86e0-78b730dae55d">ColorFill</a>
</td>
<td align="left" width="63%">
Allows an application to fill a rectangular area of a D3DPOOL_DEFAULT surface with a specified color.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d41b36f6-8481-47f8-bd38-8f51bc9ff9b8">CreateAdditionalSwapChain</a>
</td>
<td align="left" width="63%">
Creates an additional swap chain for rendering multiple views.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8ae94bb-5b16-4d08-aeb9-cb15029725c9">CreateCubeTexture</a>
</td>
<td align="left" width="63%">
Creates a cube texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c94eed81-0706-44d6-a8be-83e2a5d46c39">CreateDepthStencilSurface</a>
</td>
<td align="left" width="63%">
Creates a depth-stencil resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8bfc9f23-ea7a-411b-82b9-5f19cb2f81e0">CreateIndexBuffer</a>
</td>
<td align="left" width="63%">
Creates an index buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9502aa34-afde-4547-a5da-224f29719c07">CreateOffscreenPlainSurface</a>
</td>
<td align="left" width="63%">
Create an off-screen surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/241fd2a9-6ce0-486c-b4e6-48d22e6debbd">CreatePixelShader</a>
</td>
<td align="left" width="63%">
Creates a pixel shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0733a30e-b142-46cd-a8b5-3f70ced77521">CreateQuery</a>
</td>
<td align="left" width="63%">
Creates a status query.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3c0c8651-0c54-4eeb-bd37-c2aa26b1211d">CreateRenderTarget</a>
</td>
<td align="left" width="63%">
Creates a render-target surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36951221-ab14-45bc-bfb3-4294e3d20fb0">CreateStateBlock</a>
</td>
<td align="left" width="63%">
Creates a new state block that contains the values for all device states, vertex-related states, or pixel-related states.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/61b27c7f-cfec-4cb1-bdb9-a973c37a7df4">CreateTexture</a>
</td>
<td align="left" width="63%">
Creates a texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b914bbd-d4bb-4d59-9820-f494a4cf0757">CreateVertexBuffer</a>
</td>
<td align="left" width="63%">
Creates a vertex buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/34979faa-0656-4f0c-b21d-3a3212819391">CreateVertexDeclaration</a>
</td>
<td align="left" width="63%">
Create a vertex shader declaration from the device and the vertex elements.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2eb4521d-ec5d-4b51-aa84-7b80d6a90e0a">CreateVertexShader</a>
</td>
<td align="left" width="63%">
Creates a vertex shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a0dada01-aca1-46ef-8321-62022219843f">CreateVolumeTexture</a>
</td>
<td align="left" width="63%">
Creates a volume texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2febb03e-63ed-4c16-b6ba-1927f749c1ca">DeletePatch</a>
</td>
<td align="left" width="63%">
Frees a cached high-order patch.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/535a261a-ca4f-432b-9126-f46c44dc8430">DrawIndexedPrimitive</a>
</td>
<td align="left" width="63%">
Based on indexing, renders the specified geometric primitive into an array of vertices.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/61b13680-293b-4c7e-9cf0-d91e764498fb">DrawIndexedPrimitiveUP</a>
</td>
<td align="left" width="63%">
Renders the specified geometric primitive with data specified by a user memory pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b83110ba-85af-4f02-b651-9e64c37269f5">DrawPrimitive</a>
</td>
<td align="left" width="63%">
Renders a sequence of nonindexed, geometric primitives of the specified type from the current set of data input streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1be42c40-49af-458e-a5f5-1f56d2aa4f86">DrawPrimitiveUP</a>
</td>
<td align="left" width="63%">
Renders data specified by a user memory pointer as a sequence of geometric primitives of the specified type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/478b4a3d-3366-47ec-8a66-92aa2aa06477">DrawRectPatch</a>
</td>
<td align="left" width="63%">
Draws a rectangular patch using the currently set streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9076fbe6-0f14-4b28-8f34-145e4eac6f22">DrawTriPatch</a>
</td>
<td align="left" width="63%">
Draws a triangular patch using the currently set streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ff1e40e-9e19-4168-ae29-6f7d204ab236">EndScene</a>
</td>
<td align="left" width="63%">
Ends a scene that was begun by calling <a href="https://msdn.microsoft.com/7fc1375d-b2de-4762-9963-8428938e499f">IDirect3DDevice9::BeginScene</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/170fab09-671f-4faf-99e4-849ba4a53688">EndStateBlock</a>
</td>
<td align="left" width="63%">
Signals Direct3D to stop recording a device-state block and retrieve a pointer to the state block interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7e3ba8a1-1b41-4ecb-a580-eeeddcb94c74">EvictManagedResources</a>
</td>
<td align="left" width="63%">
Evicts all managed resources, including both Direct3D and driver-managed resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d36d35e4-f972-4af3-9a2e-604a28c2b38c">GetAvailableTextureMem</a>
</td>
<td align="left" width="63%">
Returns an estimate of the amount of available texture memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fac7f4eb-ce6f-4f9d-810c-f3a0ad155cc2">GetBackBuffer</a>
</td>
<td align="left" width="63%">
Retrieves a back buffer from the device's swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0e8ec541-606d-4f90-a396-40eb72e9422d">GetClipPlane</a>
</td>
<td align="left" width="63%">
Retrieves the coefficients of a user-defined clipping plane for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b8a68504-bc0f-4d36-a3f4-729fa9ab5004">GetClipStatus</a>
</td>
<td align="left" width="63%">
Retrieves the clip status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/18889d40-a64f-41da-92dd-7b197749e685">GetCreationParameters</a>
</td>
<td align="left" width="63%">
Retrieves the creation parameters of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e72ec7a1-9904-4a07-a662-24c6532cfdc8">GetCurrentTexturePalette</a>
</td>
<td align="left" width="63%">
Retrieves the current texture palette.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/314ba7bd-12e0-476c-ab64-f94edc9f3f88">GetDepthStencilSurface</a>
</td>
<td align="left" width="63%">
Gets the depth-stencil surface owned by the Direct3DDevice object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/184e93b7-8869-4a7a-a898-14fb4174cf0b">GetDeviceCaps</a>
</td>
<td align="left" width="63%">
Retrieves the capabilities of the rendering device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42666561-fb2b-47b4-b2c4-49926ea67964">GetDirect3D</a>
</td>
<td align="left" width="63%">
Returns an interface to the instance of the Direct3D object that created the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a96215a-366d-4820-9d9c-440673f1ef75">GetDisplayMode</a>
</td>
<td align="left" width="63%">
Retrieves the display mode's spatial resolution, color resolution, and refresh frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a5e34b4-baec-4305-b0ca-d09b0925a2ef">GetFrontBufferData</a>
</td>
<td align="left" width="63%">
Generates a copy of the device's front buffer and places that copy in a system memory buffer provided by the application. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7295c1c3-1b09-4775-8ed6-8e84d545b6d0">GetFVF</a>
</td>
<td align="left" width="63%">
Gets the fixed vertex function declaration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/798ed6ed-ae8b-412d-b70b-024d198eb16f">GetGammaRamp</a>
</td>
<td align="left" width="63%">
Retrieves the gamma correction ramp for the swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a52c3298-d94e-4d81-b7f6-bda3d4d54f52">GetIndices</a>
</td>
<td align="left" width="63%">
Retrieves index data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1e52be8e-7e24-400d-89c5-93dd316534bc">GetLight</a>
</td>
<td align="left" width="63%">
Retrieves a set of lighting properties that this device uses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7dacc010-fef7-4fcb-8e3e-08b683476eef">GetLightEnable</a>
</td>
<td align="left" width="63%">
Retrieves the activity status - enabled or disabled - for a set of lighting parameters within a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/834855f6-85ff-4c68-b1e7-8418042b71aa">GetMaterial</a>
</td>
<td align="left" width="63%">
Retrieves the current material properties for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/89b9beec-ce26-4a37-b0d2-eb59f86831c0">GetNPatchMode</a>
</td>
<td align="left" width="63%">
Gets the N-patch mode segments.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0e6adf96-821a-4471-b332-2be691b994cd">GetNumberOfSwapChains</a>
</td>
<td align="left" width="63%">
Gets the number of implicit swap chains.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f89396a5-57bf-4e3c-b5e8-044f58201156">GetPaletteEntries</a>
</td>
<td align="left" width="63%">
Retrieves palette entries.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64d62518-8fc8-4021-b98f-2176435d84cc">GetPixelShader</a>
</td>
<td align="left" width="63%">
Retrieves the currently set pixel shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe32886b-f50c-47a6-b854-a96f53fd92b4">GetPixelShaderConstantB</a>
</td>
<td align="left" width="63%">
Gets a Boolean shader constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f8271a5-782b-4e9a-93a6-8c7d98e0f1f7">GetPixelShaderConstantF</a>
</td>
<td align="left" width="63%">
Gets a floating-point shader constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6bad21d7-2058-4801-be26-21aa7823c518">GetPixelShaderConstantI</a>
</td>
<td align="left" width="63%">
Gets an integer shader constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn940224">GetRasterStatus</a>
</td>
<td align="left" width="63%">
Returns information describing the raster of the monitor on which the swap chain is presented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ec6a1fd-d310-4316-a9e6-60378320ea12">GetRenderState</a>
</td>
<td align="left" width="63%">
Retrieves a render-state value for a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e6109f4-8e86-413c-a347-dade4e578c89">GetRenderTarget</a>
</td>
<td align="left" width="63%">
Retrieves a render-target surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9fc6121c-3da8-49d8-9bd6-c8654ce90100">GetRenderTargetData</a>
</td>
<td align="left" width="63%">
Copies the render-target data from device memory to system memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/497305c9-7cbf-4aee-9a83-dddfdd9014ae">GetSamplerState</a>
</td>
<td align="left" width="63%">
Gets the sampler state value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd7bbe5a-4542-45d2-922e-b7b5147bf284">GetScissorRect</a>
</td>
<td align="left" width="63%">
Gets the scissor rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eb2392f7-044e-4a6c-bbbb-3ab26c3c0d9c">GetSoftwareVertexProcessing</a>
</td>
<td align="left" width="63%">
Gets the vertex processing (hardware or software) mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d64dbbc5-48db-42c5-8b2f-dc0a3068fe16">GetStreamSource</a>
</td>
<td align="left" width="63%">
Retrieves a vertex buffer bound to the specified data stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7be2e5bd-c105-451e-b195-43b296b3a9bd">GetStreamSourceFreq</a>
</td>
<td align="left" width="63%">
Gets the stream source frequency divider value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/343522f2-33e8-46a5-a17f-b6c36b8fe82b">GetSwapChain</a>
</td>
<td align="left" width="63%">
Gets a pointer to a swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f472de6f-6c46-4424-95e5-62164afaf026">GetTexture</a>
</td>
<td align="left" width="63%">
Retrieves a texture assigned to a stage for a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ecc2019-16f9-4c32-9ecb-33c2b85108dc">GetTextureStageState</a>
</td>
<td align="left" width="63%">
Retrieves a state value for an assigned texture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0e91cdfc-27d7-481f-b0e0-f89f0049ffce">GetTransform</a>
</td>
<td align="left" width="63%">
Retrieves a matrix describing a transformation state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/842f8b2f-cdfd-4d88-a114-7b129f09fd61">GetVertexDeclaration</a>
</td>
<td align="left" width="63%">
Gets a vertex shader declaration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c33415b-960a-4f55-a497-b30d0525cf3f">GetVertexShader</a>
</td>
<td align="left" width="63%">
Retrieves the currently set vertex shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66e0ff74-0891-41ce-9129-33636a774ee5">GetVertexShaderConstantB</a>
</td>
<td align="left" width="63%">
Gets a Boolean vertex shader constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c5ef658-91bf-492a-86a6-2c0637e43e00">GetVertexShaderConstantF</a>
</td>
<td align="left" width="63%">
Gets a floating-point vertex shader constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e4cf79af-9f87-484d-8e01-e0c7122e101d">GetVertexShaderConstantI</a>
</td>
<td align="left" width="63%">
Gets an integer vertex shader constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/026da206-b2e7-421c-92f8-344fef7ad245">GetViewport</a>
</td>
<td align="left" width="63%">
Retrieves the viewport parameters currently set for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3a23a10b-ded5-4dfc-ac17-ebe199f9a788">LightEnable</a>
</td>
<td align="left" width="63%">
Enables or disables a set of lighting parameters within a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a7c6b4ad-4915-402b-940a-354b44fda6a5">MultiplyTransform</a>
</td>
<td align="left" width="63%">
Multiplies a device's world, view, or projection matrices by a specified matrix. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/47e67956-7ab4-4e05-bf05-685bdc094cf2">Present</a>
</td>
<td align="left" width="63%">
Presents the contents of the next buffer in the sequence of back buffers owned by the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a34ecb6-6437-46dc-aa79-bf4d24395a86">ProcessVertices</a>
</td>
<td align="left" width="63%">
Applies the vertex processing defined by the vertex shader to the set of input data streams, generating a single stream of interleaved vertex data to the destination vertex buffer. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Resets the type, size, and format of the swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5a7f085-6a69-4da8-9c3a-a7c546c10514">SetClipPlane</a>
</td>
<td align="left" width="63%">
Sets the coefficients of a user-defined clipping plane for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c035c2a3-79e3-4e33-a3d5-7674ba3cda88">SetClipStatus</a>
</td>
<td align="left" width="63%">
Sets the clip status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5d97ccf4-20cd-4773-905a-e12b279e4f0b">SetCurrentTexturePalette</a>
</td>
<td align="left" width="63%">
Sets the current texture palette.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b6410e5-fdeb-4390-b0c6-227f0c6666c6">SetCursorPosition</a>
</td>
<td align="left" width="63%">
Sets the cursor position and update options.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45e4935a-cdbd-4412-8ca5-fc4e1ceb6434">SetCursorProperties</a>
</td>
<td align="left" width="63%">
Sets properties for the cursor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0ffb4fc-6428-44b1-9f9d-88a5fa88d712">SetDepthStencilSurface</a>
</td>
<td align="left" width="63%">
Sets the depth stencil surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4cca59f4-07ae-42d2-9dc8-3ec90ad75f3b">SetDialogBoxMode</a>
</td>
<td align="left" width="63%">
This method allows the use of GDI dialog boxes in full-screen mode applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30c7db1d-5814-49d5-a92a-de597b31cb63">SetFVF</a>
</td>
<td align="left" width="63%">
Sets the current vertex stream declaration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad44b71a-f391-49bb-963d-705f6dd9325c">SetGammaRamp</a>
</td>
<td align="left" width="63%">
Sets the gamma correction ramp for the implicit swap chain. This method will affect the entire screen (not just the active window if you are running in windowed mode).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b27403da-9079-4f97-8520-c2617b53e059">SetIndices</a>
</td>
<td align="left" width="63%">
Sets index data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e1f07ba6-8a9f-4bac-8dad-16160559fa4c">SetLight</a>
</td>
<td align="left" width="63%">
Assigns a set of lighting properties for this device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52cdcd0c-1cc9-4849-91e2-822414f7f186">SetMaterial</a>
</td>
<td align="left" width="63%">
Sets the material properties for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab5a1cfd-0c37-471c-af27-4ae078b8f7cd">SetNPatchMode</a>
</td>
<td align="left" width="63%">
Enable or disable N-patches.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b205c4a-b01c-4856-91de-d45645f38404">SetPaletteEntries</a>
</td>
<td align="left" width="63%">
Sets palette entries.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bcc00274-7294-4c41-ac23-74b674bdfb77">SetPixelShader</a>
</td>
<td align="left" width="63%">
Sets the current pixel shader to a previously created pixel shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/69e44683-a551-4503-8246-c22423092734">SetPixelShaderConstantB</a>
</td>
<td align="left" width="63%">
Sets a Boolean shader constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17f68eb6-254c-4457-98ea-4a76ee1823ac">SetPixelShaderConstantF</a>
</td>
<td align="left" width="63%">
Sets a floating-point shader constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da71a62b-016d-4c3c-8fa7-23c5e349c5fe">SetPixelShaderConstantI</a>
</td>
<td align="left" width="63%">
Sets an integer shader constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/65738aae-aa90-48c5-8c9c-1927d1c92c54">SetRenderState</a>
</td>
<td align="left" width="63%">
Sets a single device render-state parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e194af98-492a-4650-acca-68ebe0cd759c">SetRenderTarget</a>
</td>
<td align="left" width="63%">
Sets a new color buffer for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2aee31b4-dab0-4a73-ae8a-1bee1876ed8c">SetSamplerState</a>
</td>
<td align="left" width="63%">
Sets the sampler state value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ea215b7-eda1-4538-a5b8-6bbbb692494c">SetScissorRect</a>
</td>
<td align="left" width="63%">
Sets the scissor rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/05e67ec5-98f8-47c4-b5b7-aabb974db88a">SetSoftwareVertexProcessing</a>
</td>
<td align="left" width="63%">
Use this method to switch between software and hardware vertex processing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/15f4cbf8-7f14-4905-b32e-ed253bc0a3de">SetStreamSource</a>
</td>
<td align="left" width="63%">
Binds a vertex buffer to a device data stream. For more information, see <a href="https://msdn.microsoft.com/ef317537-3095-435d-b0f2-83cb3b385da2">Setting the Stream Source (Direct3D 9)</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12fdf57b-25c6-4896-b0a2-931b1a546c35">SetStreamSourceFreq</a>
</td>
<td align="left" width="63%">
Sets the stream source frequency divider value. This may be used to draw several instances of geometry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec62aeee-037f-4c33-b242-e0483872016c">SetTexture</a>
</td>
<td align="left" width="63%">
Assigns a texture to a stage for a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/303f7a80-edaf-4106-a4ce-8fb7a7d30a5a">SetTextureStageState</a>
</td>
<td align="left" width="63%">
Sets the state value for the currently assigned texture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1dc94280-131f-47e8-8dd7-cea43dc6e6da">SetTransform</a>
</td>
<td align="left" width="63%">
Sets a single device transformation-related state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ca4d714-b2df-432e-9140-447cef7eaec1">SetVertexDeclaration</a>
</td>
<td align="left" width="63%">
Sets a <a href="https://msdn.microsoft.com/09dae498-3b33-4c33-bc7e-47f2bf784e4c">Vertex Declaration (Direct3D 9)</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e4913fd8-5cb3-4799-8c91-d39f213d4b47">SetVertexShader</a>
</td>
<td align="left" width="63%">
Sets the vertex shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3a781645-e622-415c-88ce-8c768ac602d5">SetVertexShaderConstantB</a>
</td>
<td align="left" width="63%">
Sets a Boolean vertex shader constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d3f206f-2951-4a32-91cc-2b579cc630d0">SetVertexShaderConstantF</a>
</td>
<td align="left" width="63%">
Sets a floating-point vertex shader constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d244d8c0-065b-4d88-9c0a-1610e518e887">SetVertexShaderConstantI</a>
</td>
<td align="left" width="63%">
Sets an integer vertex shader constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57fd3a83-4bb4-4f6c-9233-d65208d4bb39">SetViewport</a>
</td>
<td align="left" width="63%">
Sets the viewport parameters for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76d848f1-a426-489f-9207-ef708adea1be">ShowCursor</a>
</td>
<td align="left" width="63%">
Displays or hides the cursor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ad6d48f-8420-461a-96b5-e730ac06c393">StretchRect</a>
</td>
<td align="left" width="63%">
Copy the contents of the source rectangle to the destination rectangle. The source rectangle can be stretched and filtered by the copy. This function is often used to change the aspect ratio of a video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da2ac8dd-0df8-4661-995f-9c3e6ccb62d2">TestCooperativeLevel</a>
</td>
<td align="left" width="63%">
Reports the current cooperative-level status of the Direct3D device for a windowed or full-screen application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/303a4224-9c5d-4fc6-a7c5-168f18166e3c">UpdateSurface</a>
</td>
<td align="left" width="63%">
Copies rectangular subsets of pixels from one surface to another. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79be31d9-0dd2-416c-b58c-9b3b7777c65c">UpdateTexture</a>
</td>
<td align="left" width="63%">
Updates the dirty portions of a texture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ae81f51-fa31-4d8a-88a0-f271a76e082b">ValidateDevice</a>
</td>
<td align="left" width="63%">
Reports the device's ability to render the current texture-blending operations and arguments in a single pass.

</td>
</tr>
</table> 


## -remarks



The <b>IDirect3DDevice9</b> interface is obtained by calling the <a href="https://msdn.microsoft.com/22ad1d16-c1cc-4591-8311-daf6cf9924bb">IDirect3D9::CreateDevice</a> method.

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



<a href="https://msdn.microsoft.com/22ad1d16-c1cc-4591-8311-daf6cf9924bb">IDirect3D9::CreateDevice</a>
 

 

