---
UID: NF:d3d9helper.IDirect3DDevice9.StretchRect
title: IDirect3DDevice9::StretchRect (d3d9helper.h)
description: The IDirect3DDevice9::StretchRect method (d3d9helper.h) copies the contents of the source rectangle to the destination rectangle.
helpviewer_keywords: ["IDirect3DDevice9 interface [Direct3D 9]","StretchRect method","IDirect3DDevice9.StretchRect","IDirect3DDevice9::StretchRect","StretchRect","StretchRect method [Direct3D 9]","StretchRect method [Direct3D 9]","IDirect3DDevice9 interface","d3d9helper/IDirect3DDevice9::StretchRect","direct3d9.idirect3ddevice9__stretchrect","fef1baf8-c226-1e9b-4d7e-3fad08fc1652"]
old-location: direct3d9\idirect3ddevice9__stretchrect.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__stretchrect.htm
ms.date: 08/11/2022
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],StretchRect method, IDirect3DDevice9.StretchRect, IDirect3DDevice9::StretchRect, StretchRect, StretchRect method [Direct3D 9], StretchRect method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::StretchRect, direct3d9.idirect3ddevice9__stretchrect, fef1baf8-c226-1e9b-4d7e-3fad08fc1652
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3DDevice9::StretchRect
 - d3d9helper/IDirect3DDevice9::StretchRect
dev_langs:
 - c++
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
---

# IDirect3DDevice9::StretchRect


## -description

Copy the contents of the source rectangle to the destination rectangle. The source rectangle can be stretched and filtered by the copy. This function is often used to change the aspect ratio of a video stream.

## -parameters

### -param pSourceSurface [in]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a>*</b>

Pointer to the source surface. See <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a>.

### -param pSourceRect [in]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

Pointer to the source rectangle. A <b>NULL</b> for this parameter causes the entire source surface to be used.

### -param pDestSurface [in]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a>*</b>

Pointer to the destination surface. See <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a>.

### -param pDestRect [in]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

Pointer to the destination rectangle. A <b>NULL</b> for this parameter causes the entire destination surface to be used.

### -param Filter [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dtexturefiltertype">D3DTEXTUREFILTERTYPE</a></b>

Filter type. Allowable values are D3DTEXF_NONE, D3DTEXF_POINT, or D3DTEXF_LINEAR. For more information, see <a href="/windows/desktop/direct3d9/d3dtexturefiltertype">D3DTEXTUREFILTERTYPE</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be:
     D3DERR_INVALIDCALL.

## -remarks

StretchRect Restrictions

<ul>
<li>Driver support varies. See the section on driver support (below) to see which drivers support which source and destination formats.</li>
<li>The source and destination surfaces must be created in the default memory pool.</li>
<li>If filtering is specified, you must set the appropriate filter caps (see StretchRectFilterCaps in <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9">D3DCAPS9</a>).</li>
<li>Stretching is not supported between source and destination rectangles on the same surface.</li>
<li>Stretching is not supported if the destination surface is an off-screen plain surface but the source is not.</li>
<li>You many not stretch between source and destination rectangles if either surface is in a compressed format (see <a href="/windows/desktop/direct3d9/using-compressed-textures">Using Compressed Textures (Direct3D 9)</a>).</li>
<li>Stretching supports color-space conversion from YUV to high-precision RGBA only. Since color conversion support is not supported by software emulation, use <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformatconversion">IDirect3D9::CheckDeviceFormatConversion</a> to test the hardware for color conversion support.</li>
<li>If the source or destination surface is a texture surface (or a cube texture surface), you must use a Direct3D 9 driver that supports D3DDEVCAPS2_CAN_STRETCHRECT_FROM_TEXTURES (see <a href="/windows/desktop/direct3d9/d3ddevcaps2">D3DDEVCAPS2</a>).</li>
</ul>
Additional Restrictions for Depth and Stencil Surfaces

<ul>
<li>The source and destination surfaces must be plain depth stencil surfaces (not textures) (see <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createdepthstencilsurface">IDirect3DDevice9::CreateDepthStencilSurface</a>).</li>
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

There are many restrictions as to which surface combinations are valid for StretchRect. Factors include whether the driver is a Direct3D 9 driver or older, and whether the operation will result in stretching/shrinking.  Since applications are not expected to recognize if the driver is a Direct3D 9 driver or not, the runtime will automatically set a new cap, D3DDEVCAPS2_CAN_STRETCHRECT_FROM_TEXTURES cap (see <a href="/windows/desktop/direct3d9/d3ddevcaps2">D3DDEVCAPS2</a>), for Direct3D 9-level drivers and above.

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

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-beginscene">IDirect3DDevice9::BeginScene</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-endscene">IDirect3DDevice9::EndScene</a>
