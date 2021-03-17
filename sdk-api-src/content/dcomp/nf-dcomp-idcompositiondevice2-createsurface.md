---
UID: NF:dcomp.IDCompositionDevice2.CreateSurface
title: IDCompositionDevice2::CreateSurface (dcomp.h)
description: Creates an updateable surface object that can be associated with one or more visuals for composition.
helpviewer_keywords: ["CreateSurface","CreateSurface method [DirectComposition]","CreateSurface method [DirectComposition]","IDCompositionDevice2 interface","DXGI_ALPHA_MODE_IGNORE","DXGI_ALPHA_MODE_PREMULTIPLIED","DXGI_ALPHA_MODE_UNSPECIFIED","IDCompositionDevice2 interface [DirectComposition]","CreateSurface method","IDCompositionDevice2.CreateSurface","IDCompositionDevice2::CreateSurface","dcomp/IDCompositionDevice2::CreateSurface","directcomp.idcompositiondevice2_createsurface"]
old-location: directcomp\idcompositiondevice2_createsurface.htm
tech.root: directcomp
ms.assetid: 1CBE92B6-AC48-47F1-B50A-B78030D356D8
ms.date: 12/05/2018
ms.keywords: CreateSurface, CreateSurface method [DirectComposition], CreateSurface method [DirectComposition],IDCompositionDevice2 interface, DXGI_ALPHA_MODE_IGNORE, DXGI_ALPHA_MODE_PREMULTIPLIED, DXGI_ALPHA_MODE_UNSPECIFIED, IDCompositionDevice2 interface [DirectComposition],CreateSurface method, IDCompositionDevice2.CreateSurface, IDCompositionDevice2::CreateSurface, dcomp/IDCompositionDevice2::CreateSurface, directcomp.idcompositiondevice2_createsurface
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDCompositionDevice2::CreateSurface
 - dcomp/IDCompositionDevice2::CreateSurface
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionDevice2.CreateSurface
---

# IDCompositionDevice2::CreateSurface


## -description

Creates an updateable surface object that can be associated with one or more visuals for composition.

## -parameters

### -param width [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The width of the surface, in pixels. Constrained by the <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> of the rendering device that was passed in at the time the DirectComposition device was created.

### -param height [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The height of the surface, in pixels. Constrained by the <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> of the rendering device that was passed in at the time the DirectComposition device was created.

### -param pixelFormat [in]

Type: <b><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a></b>

The pixel format of the surface.

### -param alphaMode [in]

Type: <b><a href="/windows/desktop/api/dxgi1_2/ne-dxgi1_2-dxgi_alpha_mode">DXGI_ALPHA_MODE</a></b>

The format of the alpha channel, if an alpha channel is included in the pixel format. It can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DXGI_ALPHA_MODE_UNSPECIFIED"></a><a id="dxgi_alpha_mode_unspecified"></a><dl>
<dt><b>DXGI_ALPHA_MODE_UNSPECIFIED</b></dt>
</dl>
</td>
<td width="60%">
The alpha channel is not specified. This value has the same effect as <b>DXGI_ALPHA_MODE_IGNORE</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="DXGI_ALPHA_MODE_PREMULTIPLIED"></a><a id="dxgi_alpha_mode_premultiplied"></a><dl>
<dt><b>DXGI_ALPHA_MODE_PREMULTIPLIED</b></dt>
</dl>
</td>
<td width="60%">
The color channels contain values that are premultiplied with the alpha channel.


</td>
</tr>
<tr>
<td width="40%"><a id="DXGI_ALPHA_MODE_IGNORE"></a><a id="dxgi_alpha_mode_ignore"></a><dl>
<dt><b>DXGI_ALPHA_MODE_IGNORE</b></dt>
</dl>
</td>
<td width="60%">
The alpha channel should be ignored and the bitmap should be rendered opaquely.

</td>
</tr>
</table>

### -param surface [out]

Type: <b><a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionsurface">IDCompositionSurface</a>**</b>

The newly created surface object. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

A Microsoft DirectComposition surface is a rectangular array of pixels that can be associated with a visual for composition. 

A newly created surface object is in an uninitialized state. While it is uninitialized, the surface has no effect on the composition of the visual tree. It behaves exactly like a surface that has  100% transparent pixels.



To initialize the surface with pixel data, use the <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionsurface-begindraw">IDCompositionSurface::BeginDraw</a> and <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionsurface-enddraw">IDCompositionSurface::EndDraw</a> methods. The first call to this method must cover the entire surface area to provide an initial value for every pixel. Subsequent calls may specify smaller sub-rectangles of the surface to update.



DirectComposition surfaces support the following pixel formats: 

<ul>
<li><b>DXGI_FORMAT_B8G8R8A8_UNORM</b></li>
<li><b>DXGI_FORMAT_R8G8B8A8_UNORM</b></li>
<li><b>DXGI_FORMAT_R16G16B16A16_FLOAT</b></li>
</ul>

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice2">IDCompositionDevice2</a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice-createvirtualsurface">IDCompositionDevice2::CreateVirtualSurface</a>