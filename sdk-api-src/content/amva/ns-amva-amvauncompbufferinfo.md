---
UID: NS:amva._tag_AMVAUncompBufferInfo
title: AMVAUncompBufferInfo (amva.h)
description: The AMVAUncompBufferInfo structure describes the uncompressed surfaces to be allocated by the video renderer.
helpviewer_keywords: ["*LPAMVAUncompBufferInfo","AMVAUncompBufferInfo","AMVAUncompBufferInfo structure [DirectShow]","AMVAUncompBufferInfoStructure","LPAMVAUncompBufferInfo","LPAMVAUncompBufferInfo structure pointer [DirectShow]","amva/AMVAUncompBufferInfo","amva/LPAMVAUncompBufferInfo","dshow.amvauncompbufferinfo"]
old-location: dshow\amvauncompbufferinfo.htm
tech.root: dshow
ms.assetid: 113cc7ba-d05e-48a7-88cb-13645beb16d1
ms.date: 4/26/2023
ms.keywords: '*LPAMVAUncompBufferInfo, AMVAUncompBufferInfo, AMVAUncompBufferInfo structure [DirectShow], AMVAUncompBufferInfoStructure, LPAMVAUncompBufferInfo, LPAMVAUncompBufferInfo structure pointer [DirectShow], amva/AMVAUncompBufferInfo, amva/LPAMVAUncompBufferInfo, dshow.amvauncompbufferinfo'
req.header: amva.h
req.include-header: Videoacc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: AMVAUncompBufferInfo, *LPAMVAUncompBufferInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _tag_AMVAUncompBufferInfo
 - amva/_tag_AMVAUncompBufferInfo
 - LPAMVAUncompBufferInfo
 - amva/LPAMVAUncompBufferInfo
 - AMVAUncompBufferInfo
 - amva/AMVAUncompBufferInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - amva.h
api_name:
 - AMVAUncompBufferInfo
---

# AMVAUncompBufferInfo structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>AMVAUncompBufferInfo</b> structure describes the uncompressed surfaces to be allocated by the video renderer.

## -struct-fields

### -field dwMinNumSurfaces

Minimum number of surfaces to allocate.

### -field dwMaxNumSurfaces

Maximum number of surfaces to allocate.

### -field ddUncompPixelFormat

<b>DDPIXELFORMAT</b> structure, describing the pixel format of the allocated surfaces.

## -remarks

The VMR-7 and VMR-9 filters allocate at least <b>dwMinNumSurfaces</b> surfaces. For interlaced content, the VMR-7 allocates additional surfaces equal to the number of forward and backward reference frames required by the deinterlacer. The VMR-7 gets these values by calling <a href="/windows/desktop/api/strmif/nf-strmif-ivmrdeinterlacecontrol-getdeinterlacemodecaps">IVMRDeinterlaceControl::GetDeinterlaceModeCaps</a>. The VMR-9 does not need to allocate additional surfaces for deinterlacing. Thus:

<ul>
<li>For the VMR-7, the number of allocated surfaces is <b>dwMinNumSurfaces</b> + <b>dwNumForwardRefSamples</b> + <b>dwNumBackwardRefSamples</b>. For progressive content, the last two values will be zero.</li>
<li>For the VMR-9, the number of allocated surfaces is <b>dwMinNumSurfaces</b>.</li>
</ul>
Initially, the decoder should set <b>dwMinNumSurfaces</b> equal to the optimal number of surfaces needed to decode smoothly. If the renderer cannot allocate that many surfaces, the connection will fail with the error code E_OUTOFMEMORY. The decoder should reconnect with the same media type but set <b>dwMinNumSurfaces</b> equal to the minimum number of surfaces required for decoding. For example, the optimal number of surfaces might be 8, while the minimum is 4.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getuncompsurfacesinfo">IAMVideoAcceleratorNotify::GetUncompSurfacesInfo</a>