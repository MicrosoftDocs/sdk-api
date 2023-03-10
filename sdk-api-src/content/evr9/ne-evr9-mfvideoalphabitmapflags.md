---
UID: NE:evr9.__MIDL___MIDL_itf_evr9_0000_0002_0002
title: MFVideoAlphaBitmapFlags (evr9.h)
description: Defines flags for the MFVideoAlphaBitmapParams structure.
helpviewer_keywords: ["MFVideoAlphaBitmapFlags","MFVideoAlphaBitmapFlags enumeration [Media Foundation]","MFVideoAlphaBitmap_Alpha","MFVideoAlphaBitmap_BitMask","MFVideoAlphaBitmap_DestRect","MFVideoAlphaBitmap_EntireDDS","MFVideoAlphaBitmap_FilterMode","MFVideoAlphaBitmap_SrcColorKey","MFVideoAlphaBitmap_SrcRect","d9989c44-8a3c-4f8b-a63d-e39e26797935","evr9/MFVideoAlphaBitmapFlags","evr9/MFVideoAlphaBitmap_Alpha","evr9/MFVideoAlphaBitmap_BitMask","evr9/MFVideoAlphaBitmap_DestRect","evr9/MFVideoAlphaBitmap_EntireDDS","evr9/MFVideoAlphaBitmap_FilterMode","evr9/MFVideoAlphaBitmap_SrcColorKey","evr9/MFVideoAlphaBitmap_SrcRect","mf.mfvideoalphabitmapflags"]
old-location: mf\mfvideoalphabitmapflags.htm
tech.root: mf
ms.assetid: d9989c44-8a3c-4f8b-a63d-e39e26797935
ms.date: 12/05/2018
ms.keywords: MFVideoAlphaBitmapFlags, MFVideoAlphaBitmapFlags enumeration [Media Foundation], MFVideoAlphaBitmap_Alpha, MFVideoAlphaBitmap_BitMask, MFVideoAlphaBitmap_DestRect, MFVideoAlphaBitmap_EntireDDS, MFVideoAlphaBitmap_FilterMode, MFVideoAlphaBitmap_SrcColorKey, MFVideoAlphaBitmap_SrcRect, d9989c44-8a3c-4f8b-a63d-e39e26797935, evr9/MFVideoAlphaBitmapFlags, evr9/MFVideoAlphaBitmap_Alpha, evr9/MFVideoAlphaBitmap_BitMask, evr9/MFVideoAlphaBitmap_DestRect, evr9/MFVideoAlphaBitmap_EntireDDS, evr9/MFVideoAlphaBitmap_FilterMode, evr9/MFVideoAlphaBitmap_SrcColorKey, evr9/MFVideoAlphaBitmap_SrcRect, mf.mfvideoalphabitmapflags
req.header: evr9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: MFVideoAlphaBitmapFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_evr9_0000_0002_0002
 - evr9/__MIDL___MIDL_itf_evr9_0000_0002_0002
 - MFVideoAlphaBitmapFlags
 - evr9/MFVideoAlphaBitmapFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - evr9.h
api_name:
 - MFVideoAlphaBitmapFlags
---

# MFVideoAlphaBitmapFlags enumeration


## -description

Defines flags for the <a href="/windows/desktop/api/evr9/ns-evr9-mfvideoalphabitmapparams">MFVideoAlphaBitmapParams</a> structure.

## -enum-fields

### -field MFVideoAlphaBitmap_EntireDDS:0x1

Alpha-blend the entire DirectDraw surface.

If you are alpha-blending a DirectDraw surface, you can set this flag when you call <a href="/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-setalphabitmap">IMFVideoMixerBitmap::SetAlphaBitmap</a>. If this flag is set, the mixer ignores the <b>rcSrc</b> member of the <a href="/windows/desktop/api/evr9/ns-evr9-mfvideoalphabitmapparams">MFVideoAlphaBitmapParams</a> structure. If this flag is absent, the <b>rcSrc</b> member specifies the source rectangle.

This flag cannot be used if you specify a GDI bitmap for alpha-blending. For a GDI bitmap, you must fill in the <b>rcSrc</b> member when you call <a href="/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-setalphabitmap">SetAlphaBitmap</a>.

This flag does not apply to the <a href="/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-updatealphabitmapparameters">IMFVideoMixerBitmap::UpdateAlphaBitmapParameters</a> method.

### -field MFVideoAlphaBitmap_SrcColorKey:0x2

If this flag is set, the <b>clrSrcKey</b> member of the <a href="/windows/desktop/api/evr9/ns-evr9-mfvideoalphabitmapparams">MFVideoAlphaBitmapParams</a> structure specifies a color key for alpha-blending. If this flag is absent, the <b>clrSrcKey</b> member is ignored.

This flag is not valid if you are alpha-blending a Direct3D surface with per-pixel alpha (D3DFMT_A8R8G8B8). When the DirectDraw surface has per-pixel alpha, the pixel alpha values are used for the alpha-blending operation.

### -field MFVideoAlphaBitmap_SrcRect:0x4

Update the source rectangle.

This flag applies to the <a href="/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-updatealphabitmapparameters">UpdateAlphaBitmapParameters</a> method. If this flag is set, the <b>rcSrc</b> member of the <a href="/windows/desktop/api/evr9/ns-evr9-mfvideoalphabitmapparams">MFVideoAlphaBitmapParams</a> structure updates the source rectangle. If this flag is absent, the <b>rcSrc</b> member is ignored. By setting this flag, you can animate the image by selecting different portions of the bitmap.

This flag does not apply to the <a href="/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-setalphabitmap">SetAlphaBitmap</a> method.

### -field MFVideoAlphaBitmap_DestRect:0x8

If this flag is set, the <b>nrcDest</b> member of the <a href="/windows/desktop/api/evr9/ns-evr9-mfvideoalphabitmapparams">MFVideoAlphaBitmapParams</a> structure specifies a normalized rectangle for scaling the bitmap. If this flag is absent, the <b>nrcDest</b> member is ignored.

### -field MFVideoAlphaBitmap_FilterMode:0x10

If this flag is set, the <b>dwFilterMode</b> member of the <a href="/windows/desktop/api/evr9/ns-evr9-mfvideoalphabitmapparams">MFVideoAlphaBitmapParams</a> structure specifies a Direct3D filtering mode. If this flag is absent, the <b>dwFilterMode</b> member is ignored.

### -field MFVideoAlphaBitmap_Alpha:0x20

If this flag is set, the <b>fAlpha</b> member of the <a href="/windows/desktop/api/evr9/ns-evr9-mfvideoalphabitmapparams">MFVideoAlphaBitmapParams</a> structure specifies an alpha value to apply to the entire image. If this flag is absent, the <b>fAlpha</b> member is ignored.

### -field MFVideoAlphaBitmap_BitMask:0x3f

Bitmask to validate flag values. This value is not a valid flag.

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
