---
UID: NS:evr9.MFVideoAlphaBitmap
title: MFVideoAlphaBitmap (evr9.h)
description: Specifies a bitmap for the enhanced video renderer (EVR) to alpha-blend with the video.
helpviewer_keywords: ["609041f2-7ba4-4157-819b-4ac21612dca2","MFVideoAlphaBitmap","MFVideoAlphaBitmap structure [Media Foundation]","evr9/MFVideoAlphaBitmap","mf.mfvideoalphabitmap"]
old-location: mf\mfvideoalphabitmap.htm
tech.root: mfarchive
ms.assetid: 609041f2-7ba4-4157-819b-4ac21612dca2
ms.date: 12/05/2018
ms.keywords: 609041f2-7ba4-4157-819b-4ac21612dca2, MFVideoAlphaBitmap, MFVideoAlphaBitmap structure [Media Foundation], evr9/MFVideoAlphaBitmap, mf.mfvideoalphabitmap
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
req.typenames: MFVideoAlphaBitmap
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFVideoAlphaBitmap
 - evr9/MFVideoAlphaBitmap
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
 - MFVideoAlphaBitmap
archived: true
---

# MFVideoAlphaBitmap structure


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Specifies a bitmap for the enhanced video renderer (EVR) to alpha-blend with the video.

## -struct-fields

### -field GetBitmapFromDC

If <b>TRUE</b>, the <b>hdc</b> member is used. Otherwise, the <b>pDDs</b> member is used.

### -field bitmap

A union that contains the following members.



#### pDDs

Pointer to the <b>IDirect3DSurface9</b> interface of a Direct3D surface that contains the bitmap. If <b>GetBitmapFromDC</b> is <b>TRUE</b>, this member is ignored.

### -field bitmap.hdc

Handle to the device context (DC) of a GDI bitmap. If <b>GetBitmapFromDC</b> is <b>FALSE</b>, this member is ignored.

### -field bitmap.pDDS

### -field params

<a href="/windows/desktop/api/evr9/ns-evr9-mfvideoalphabitmapparams">MFVideoAlphaBitmapParams</a> structure that specifies the parameters for the alpha-blending operation.

## -remarks

To specify a GDI bitmap, create a device context and call <b>SelectObject</b> to select the bitmap into the DC. Then set the <b>hdc</b> member of the structure equal to the handle to the DC and set the <b>GetBitmapFromDC</b> member to <b>TRUE</b>.

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-setalphabitmap">IMFVideoMixerBitmap::SetAlphaBitmap</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>