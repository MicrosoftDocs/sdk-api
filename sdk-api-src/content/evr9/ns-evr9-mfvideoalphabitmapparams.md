---
UID: NS:evr9.MFVideoAlphaBitmapParams
title: MFVideoAlphaBitmapParams (evr9.h)
description: Specifies how the enhanced video renderer (EVR) alpha-blends a bitmap with the video.
helpviewer_keywords: ["3a7f67fa-ca54-4b6f-9cfc-e8eba57f00ce","MFVideoAlphaBitmapParams","MFVideoAlphaBitmapParams structure [Media Foundation]","evr9/MFVideoAlphaBitmapParams","mf.mfvideoalphabitmapparams"]
old-location: mf\mfvideoalphabitmapparams.htm
tech.root: mfarchive
ms.assetid: 3a7f67fa-ca54-4b6f-9cfc-e8eba57f00ce
ms.date: 12/05/2018
ms.keywords: 3a7f67fa-ca54-4b6f-9cfc-e8eba57f00ce, MFVideoAlphaBitmapParams, MFVideoAlphaBitmapParams structure [Media Foundation], evr9/MFVideoAlphaBitmapParams, mf.mfvideoalphabitmapparams
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
req.typenames: MFVideoAlphaBitmapParams
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFVideoAlphaBitmapParams
 - evr9/MFVideoAlphaBitmapParams
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
 - MFVideoAlphaBitmapParams
archived: true
---

# MFVideoAlphaBitmapParams structure


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Specifies how the enhanced video renderer (EVR) alpha-blends a bitmap with the video.

## -struct-fields

### -field dwFlags

Bitwise OR of one or more flags from the <a href="/windows/win32/api/evr9/ne-evr9-mfvideoalphabitmapflags">MFVideoAlphaBitmapFlags</a> enumeration. These flags indicate which of the other structure members contain valid information.

### -field clrSrcKey

Source color key. This member is used if the <b>dwFlags</b> member contains the MFVideoAlphaBitmap_SrcColorKey flag. Any pixels in the bitmap that match the color key are rendered as transparent pixels.

You cannot specify a color key if you are alpha-blending a Direct3D surface with per-pixel alpha (D3DFMT_A8R8G8B8).

### -field rcSrc

Source rectangle. The source rectangle defines the region of the bitmap that is alpha-blended with the video. The source rectangle is given in pixels and is relative to the original bitmap.

If you are alpha-blending a GDI bitmap, you must fill in this structure when you call <a href="/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-setalphabitmap">IMFVideoMixerBitmap::SetAlphaBitmap</a>.

If you are alpha-blending a Direct3D surface and the <b>dwFlags</b> member contains the MFVideoAlphaBitmap_EntireDDS flag, the <b>rcSrc</b> member is ignored. If the flag is absent, you must fill in the <b>rcSrc</b> member.

After setting the initiali bitmap, you can update the source rectangle by calling <a href="/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-updatealphabitmapparameters">IMFVideoMixerBitmap::UpdateAlphaBitmapParameters</a>. To update the source rectangle, set the MFVideoAlphaBitmap_SrcColorKey flag in the <b>dwFlags</b> member.

The source rectangle cannot be an empty rectangle, and cannot exceed the bounds of the bitmap.

### -field nrcDest

Destination rectangle. The destination rectangle defines the region of the composited video image that receives the alpha-blended bitmap. The destination rectangle is specified as a normalized rectangle using the <a href="/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect">MFVideoNormalizedRect</a> structure.

This member is used if the <b>dwFlags</b> member contains the MFVideoAlphaBitmap_DestRect flag. Otherwise, the default destination rectangle is {0, 0, 1, 1}.

### -field fAlpha

Alpha blending value. This member is used if the <b>dwFlags</b> member contains the MFVideoAlphaBitmap_Alpha flag. Otherwise, the default value is 1.0 (opaque). The valid range is 0.0 to 1.0, inclusive.

This value is applied to the entire bitmap image. To create transparent regions, use the <b>clrSrcKey</b> member or use a DirectDraw surface with per-pixel alpha.

### -field dwFilterMode

Direct3D filtering mode to use when performing the alpha-blend operation. Specify the filter mode as a D3DTEXTUREFILTERTYPE value. For more information, see the Direct3D documentation.

This member is used if the <b>dwFlags</b> member contains the MFVideoAlphaBitmap_FilterMode flag. Otherwise, the default value is D3DTEXF_POINT.

Point filtering is particularly useful for images that contain text and will not be stretched.

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-updatealphabitmapparameters">IMFVideoMixerBitmap::UpdateAlphaBitmapParameters</a>



<a href="/windows/desktop/api/evr9/ns-evr9-mfvideoalphabitmap">MFVideoAlphaBitmap</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>