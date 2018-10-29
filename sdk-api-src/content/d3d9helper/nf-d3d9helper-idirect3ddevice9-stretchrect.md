---
UID: NF:d3d9helper.IDirect3DDevice9.StretchRect
title: IDirect3DDevice9::StretchRect
author: windows-sdk-content
description: Copy the contents of the source rectangle to the destination rectangle. The source rectangle can be stretched and filtered by the copy. This function is often used to change the aspect ratio of a video stream.
old-location: direct3d9\idirect3ddevice9__stretchrect.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__stretchrect.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],StretchRect method, IDirect3DDevice9.StretchRect, IDirect3DDevice9::StretchRect, StretchRect, StretchRect method [Direct3D 9], StretchRect method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::StretchRect, direct3d9.idirect3ddevice9__stretchrect, fef1baf8-c226-1e9b-4d7e-3fad08fc1652
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DDevice9.StretchRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9::StretchRect


## -description


Copy the contents of the source rectangle to the destination rectangle. The source rectangle can be stretched and filtered by the copy. This function is often used to change the aspect ratio of a video stream.


## -parameters




### -param pSourceSurface [in]

Type: <b><a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a>*</b>

Pointer to the source surface. See <a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a>.


### -param pSourceRect [in]

Type: <b>const <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

Pointer to the source rectangle. A <b>NULL</b> for this parameter causes the entire source surface to be used.


### -param pDestSurface [in]

Type: <b><a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a>*</b>

Pointer to the destination surface. See <a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a>.


### -param pDestRect [in]

Type: <b>const <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

Pointer to the destination rectangle. A <b>NULL</b> for this parameter causes the entire destination surface to be used.


### -param Filter [in]

Type: <b><a href="https://msdn.microsoft.com/4e0420fa-ac76-4be4-90d7-944d8d5a5de1">D3DTEXTUREFILTERTYPE</a></b>

Filter type. Allowable values are D3DTEXF_NONE, D3DTEXF_POINT, or D3DTEXF_LINEAR. For more information, see <a href="https://msdn.microsoft.com/4e0420fa-ac76-4be4-90d7-944d8d5a5de1">D3DTEXTUREFILTERTYPE</a>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be:
     D3DERR_INVALIDCALL.




## -remarks



StretchRect Restrictions

<ul>
<li>Driver support varies. See the section on driver support (below) to see which drivers support which source and destination formats.</li>
<li>The source and destination surfaces must be created in the default memory pool.</li>
<li>If filtering is specified, you must set the appropriate filter caps (see StretchRectFilterCaps in <a href="https://msdn.microsoft.com/44457b7b-a1f7-4019-b971-8ec2334d3313">D3DCAPS9</a>).</li>
<li>Stretching is not supported between source and destination rectangles on the same surface.</li>
<li>Stretching is not supported if the destination surface is an off-screen plain surface but the source is not.</li>
<li>You many not stretch between source and destination rectangles if either surface is in a compressed format (see <a href="https://msdn.microsoft.com/60892a8b-93f4-43ba-87ef-d5c7cc6fb8c6">Using Compressed Textures (Direct3D 9)</a>).</li>
<li>Stretching supports color-space conversion from YUV to high-precision RGBA only. Since color conversion support is not supported by software emulation, use <a href="https://msdn.microsoft.com/c15bbd53-9d2d-4ea9-9a8e-bf4f10f7d7e9">IDirect3D9::CheckDeviceFormatConversion</a> to test the hardware for color conversion support.</li>
<li>If the source or destination surface is a texture surface (or a cube texture surface), you must use a Direct3D 9 driver that supports D3DDEVCAPS2_CAN_STRETCHRECT_FROM_TEXTURES (see <a href="https://msdn.microsoft.com/3f3b9f86-dee3-4506-bd2e-1dcc8ba617ed">D3DDEVCAPS2</a>).</li>
</ul>
Additional Restrictions for Depth and Stencil Surfaces

<ul>
<li>The source and destination surfaces must be plain depth stencil surfaces (not textures) (see <a href="https://msdn.microsoft.com/c94eed81-0706-44d6-a8be-83e2a5d46c39">IDirect3DDevice9::CreateDepthStencilSurface</a>).</li>
<li>Neither of the surfaces can be discardable.</li>
<li>The entire surface must be copied (that is: sub-rectangle copies are not allowed).</li>
<li>Format conversion, stretching, and shrinking are not supported.</li>
<li>StretchRect cannot be called inside of a BeginScene/EndScene pair.</li>
</ul>
Using StretchRect to downsample a Multisample Rendertarget

You can use StretchRect to copy from one rendertarget to another. If the source rendertarget is multisampled, this results in downsampling the source rendertarget. For instance you could:

<ul>
<li>Create a multisampled rendertarget.</li>
<li>Create a second rendertarget of the same size, that is not multisampled.</li>
<li>Copy (using StretchRect the multisample rendertarget to the second rendertarget.</li>
</ul>
Note that use of the extra surface involved in using StretchRect to downsample a Multisample Rendertarget will result in a performance hit.

Driver Support

There are many restrictions as to which surface combinations are valid for StretchRect. Factors include whether the driver is a Direct3D 9 driver or older, and whether the operation will result in stretching/shrinking.  Since applications are not expected to recognize if the driver is a Direct3D 9 driver or not, the runtime will automatically set a new cap, D3DDEVCAPS2_CAN_STRETCHRECT_FROM_TEXTURES cap (see <a href="https://msdn.microsoft.com/3f3b9f86-dee3-4506-bd2e-1dcc8ba617ed">D3DDEVCAPS2</a>), for Direct3D 9-level drivers and above.

<table>
<tr>
<th>DirectX 8 Driver (no stretching)</th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
</tr>
<tr>
<th></th>
<th></th>
<th>Dest formats</th>
<th></th>
<th></th>
<th></th>
</tr>
<tr>
<th></th>
<th></th>
<th>Texture</th>
<th>RT texture</th>
<th>RT</th>
<th>Off-screen plain</th>
</tr>
<tr>
<th>Src formats</th>
<th>Texture</th>
<td>No</td>
<td>No</td>
<td>No</td>
<td>No</td>
</tr>
<tr>
<th></th>
<th>RT texture</th>
<td>No</td>
<td>Yes</td>
<td>Yes</td>
<td>No</td>
</tr>
<tr>
<th></th>
<th>RT</th>
<td>No</td>
<td>Yes</td>
<td>Yes</td>
<td>No</td>
</tr>
<tr>
<th></th>
<th>Off-screen plain</th>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
</tr>
</table>
 

<table>
<tr>
<th>DirectX 8 Driver (stretching)</th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
</tr>
<tr>
<th></th>
<th></th>
<th>Dest formats</th>
<th></th>
<th></th>
<th></th>
</tr>
<tr>
<th></th>
<th></th>
<th>Texture</th>
<th>RT texture</th>
<th>RT</th>
<th>Off-screen plain</th>
</tr>
<tr>
<th>Src formats</th>
<th>Texture</th>
<td>No</td>
<td>No</td>
<td>No</td>
<td>No</td>
</tr>
<tr>
<th></th>
<th>RT texture</th>
<td>No</td>
<td>No</td>
<td>No</td>
<td>No</td>
</tr>
<tr>
<th></th>
<th>RT</th>
<td>No</td>
<td>Yes</td>
<td>Yes</td>
<td>No</td>
</tr>
<tr>
<th></th>
<th>Off-screen plain</th>
<td>No</td>
<td>Yes</td>
<td>Yes</td>
<td>No</td>
</tr>
</table>
 

<table>
<tr>
<th>Direct3D 9 Driver (no stretching)</th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
</tr>
<tr>
<th></th>
<th></th>
<th>Dest formats</th>
<th></th>
<th></th>
<th></th>
</tr>
<tr>
<th></th>
<th></th>
<th>Texture</th>
<th>RT texture</th>
<th>RT</th>
<th>Off-screen plain</th>
</tr>
<tr>
<th>Src formats</th>
<th>Texture</th>
<td>No</td>
<td>Yes</td>
<td>Yes</td>
<td>No</td>
</tr>
<tr>
<th></th>
<th>RT texture</th>
<td>No</td>
<td>Yes</td>
<td>Yes</td>
<td>No</td>
</tr>
<tr>
<th></th>
<th>RT</th>
<td>No</td>
<td>Yes</td>
<td>Yes</td>
<td>No</td>
</tr>
<tr>
<th></th>
<th>Off-screen plain</th>
<td>No</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
</tr>
</table>
 

<table>
<tr>
<th>Direct3D 9 Driver (stretching)</th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
</tr>
<tr>
<th></th>
<th></th>
<th>Dest formats</th>
<th></th>
<th></th>
<th></th>
</tr>
<tr>
<th></th>
<th></th>
<th>Texture</th>
<th>RT texture</th>
<th>RT</th>
<th>Off-screen plain</th>
</tr>
<tr>
<th>Src formats</th>
<th>Texture</th>
<td>No</td>
<td>Yes</td>
<td>Yes</td>
<td>No</td>
</tr>
<tr>
<th></th>
<th>RT texture</th>
<td>No</td>
<td>Yes</td>
<td>Yes</td>
<td>No</td>
</tr>
<tr>
<th></th>
<th>RT</th>
<td>No</td>
<td>Yes</td>
<td>Yes</td>
<td>No</td>
</tr>
<tr>
<th></th>
<th>Off-screen plain</th>
<td>No</td>
<td>Yes</td>
<td>Yes</td>
<td>No</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/7fc1375d-b2de-4762-9963-8428938e499f">IDirect3DDevice9::BeginScene</a>



<a href="https://msdn.microsoft.com/9ff1e40e-9e19-4168-ae29-6f7d204ab236">IDirect3DDevice9::EndScene</a>
 

 

