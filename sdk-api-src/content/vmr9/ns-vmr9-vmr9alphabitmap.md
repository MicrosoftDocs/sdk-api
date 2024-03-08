---
UID: NS:vmr9._VMR9AlphaBitmap
title: VMR9AlphaBitmap (vmr9.h)
description: The VMR9AlphaBitmap structure is used with the IVMRMixerBitmap9 interface when an application provides a static bitmap for alpha blending with the video frame.
helpviewer_keywords: ["MixerPref9_AnisotropicFiltering","MixerPref9_BiLinearFiltering","MixerPref9_GaussianQuadFiltering","MixerPref9_PointFiltering","MixerPref9_PyramidalQuadFiltering","VMR9AlphaBitmap","VMR9AlphaBitmap structure [DirectShow]","VMR9AlphaBitmapStructure","dshow.vmr9alphabitmap","vmr9/VMR9AlphaBitmap"]
old-location: dshow\vmr9alphabitmap.htm
tech.root: dshow
ms.assetid: 62214c24-0a4b-43c3-91dc-3eb6e5df3d94
ms.date: 4/26/2023
ms.keywords: MixerPref9_AnisotropicFiltering, MixerPref9_BiLinearFiltering, MixerPref9_GaussianQuadFiltering, MixerPref9_PointFiltering, MixerPref9_PyramidalQuadFiltering, VMR9AlphaBitmap, VMR9AlphaBitmap structure [DirectShow], VMR9AlphaBitmapStructure, dshow.vmr9alphabitmap, vmr9/VMR9AlphaBitmap
req.header: vmr9.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: VMR9AlphaBitmap
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VMR9AlphaBitmap
 - vmr9/_VMR9AlphaBitmap
 - VMR9AlphaBitmap
 - vmr9/VMR9AlphaBitmap
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vmr9.h
api_name:
 - VMR9AlphaBitmap
---

# VMR9AlphaBitmap structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>VMR9AlphaBitmap</b> structure is used with the <a href="/windows/desktop/api/vmr9/nn-vmr9-ivmrmixerbitmap9">IVMRMixerBitmap9</a> interface when an application provides a static bitmap for alpha blending with the video frame.

## -struct-fields

### -field dwFlags

Bitwise <b>OR</b> of flags from the <a href="/previous-versions/windows/desktop/api/vmr9/ne-vmr9-vmr9alphabitmapflags">VMR9AlphaBitmapFlags</a> enumeration type.

### -field hdc

Handle to the GDI device context (HDC) for the bitmap. If this member contains a non-<b>NULL</b> value, set <b>pDDS</b> to <b>NULL</b> and set the <b>VMR9AlphaBitmap_hDC</b> flag in the <b>dwFlags</b> member. The device context is not compatible with GDI+.

### -field pDDS

Pointer to the <b>IDirect3DSurface9</b> interface of a Direct3D surface that contains the bitmap. If this member contains a valid pointer, set the <b>hdc</b> member to <b>NULL</b>. The surface format must be <b>D3DFMT_X8R8G8B8</b> (32-bit RGB) or <b>D3DFMT_A8R8G8B8</b> (32-bit RGB with per-pixel alpha). The surface must be allocated from the <b>D3DPOOL_SYSTEMMEM</b> pool.

### -field rSrc

Specifies the rectangle to copy from the source image. This rectangle is specified relative to the GDI device context or the DirectDraw surface.

When calling <a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrmixerbitmap9-setalphabitmap">IVMRMixerBitmap9::SetAlphaBitmap</a>, the source rectangle must be valid if a GDI bitmap is specified in the <b>hdc</b> member. On the other hand, if a Direct3D surface is specified in the <b>pDDS</b> member, then you can either set <b>rSrc</b> to a valid rectangle, or use the entire surface by setting the VMR9AlphaBitmap_EntireDDS flag in <b>dwFlags</b>.

When calling <a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrmixerbitmap9-updatealphabitmapparameters">IVMRMixerBitmap9::UpdateAlphaBitmapParameters</a>, <b>rSrc</b> is always optional, and is used if <b>dwFlags</b> contains the VMR9AlphaBitmap_SrcRect flag.

### -field rDest

Specifies the destination rectangle in composition space.

### -field fAlpha

Specifies the alpha blending value; must be a value from 0.0 to 1.0 (inclusive).

### -field clrSrcKey

Specifies the source color key. This value is used if the <b>dwFlags</b> member contains the <b>VMR9AlphaBitmap_SrcColorKey</b>. A color key cannot be used with a Direct3D surface that contains per-pixel alpha.

### -field dwFilterMode

One of the following flags from the <a href="/previous-versions/windows/desktop/api/vmr9/ne-vmr9-vmr9mixerprefs">VMR9MixerPrefs</a> enumeration, or zero to specify no filtering.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MixerPref9_BiLinearFiltering"></a><a id="mixerpref9_bilinearfiltering"></a><a id="MIXERPREF9_BILINEARFILTERING"></a><dl>
<dt><b>MixerPref9_BiLinearFiltering</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Bilinear interpolation filtering.

</td>
</tr>
<tr>
<td width="40%"><a id="MixerPref9_PointFiltering"></a><a id="mixerpref9_pointfiltering"></a><a id="MIXERPREF9_POINTFILTERING"></a><dl>
<dt><b>MixerPref9_PointFiltering</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Point filtering. 

</td>
</tr>
<tr>
<td width="40%"><a id="MixerPref9_AnisotropicFiltering"></a><a id="mixerpref9_anisotropicfiltering"></a><a id="MIXERPREF9_ANISOTROPICFILTERING"></a><dl>
<dt><b>MixerPref9_AnisotropicFiltering</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Anisotropic filtering.

</td>
</tr>
<tr>
<td width="40%"><a id="_MixerPref9_PyramidalQuadFiltering"></a><a id="_mixerpref9_pyramidalquadfiltering"></a><a id="_MIXERPREF9_PYRAMIDALQUADFILTERING"></a><dl>
<dt><b> MixerPref9_PyramidalQuadFiltering</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
Four-sample tent filtering.

</td>
</tr>
<tr>
<td width="40%"><a id="MixerPref9_GaussianQuadFiltering"></a><a id="mixerpref9_gaussianquadfiltering"></a><a id="MIXERPREF9_GAUSSIANQUADFILTERING"></a><dl>
<dt><b>MixerPref9_GaussianQuadFiltering</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Four-sample Gaussian filtering.

</td>
</tr>
</table>
 

This structure member is used only if the <b>dwFlags</b> member contains the <b>VMR9AlphaBitmap_FilterMode</b> flag. 

Point filtering is particularly useful for images that contain text and do not need to be stretched prior to mixing.

## -remarks

To get the HDC for a GDI bitmap, do the following:

<ol>
<li>Call <a href="/windows/desktop/api/winuser/nf-winuser-getdc">GetDC</a> to get the device context for the application's video window.</li>
<li>Call <a href="/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc">CreateCompatibleDC</a> to create a compatible device context.</li>
<li>Call <a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a> to select the bitmap into the device context obtained in the previous step.</li>
</ol>
When you are done, release the device context by calling <a href="/windows/desktop/api/wingdi/nf-wingdi-deletedc">DeleteDC</a>.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>