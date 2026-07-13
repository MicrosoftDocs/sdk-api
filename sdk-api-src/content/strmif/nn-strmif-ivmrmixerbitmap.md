---
UID: NN:strmif.IVMRMixerBitmap
title: IVMRMixerBitmap (strmif.h)
description: The IVMRMixerBitmap interface enables an application to blend a static image from a bitmap or DirectDraw surface onto the video stream, when using the Video Mixing Renderer Filter 7 (VMR-7).
helpviewer_keywords: ["IVMRMixerBitmap","IVMRMixerBitmap interface [DirectShow]","IVMRMixerBitmap interface [DirectShow]","described","IVMRMixerBitmapInterface","dshow.ivmrmixerbitmap","strmif/IVMRMixerBitmap"]
old-location: dshow\ivmrmixerbitmap.htm
tech.root: dshow
ms.assetid: ac7da3f9-2c17-4517-bb64-6b56257a65c3
ms.date: 4/26/2023
ms.keywords: IVMRMixerBitmap, IVMRMixerBitmap interface [DirectShow], IVMRMixerBitmap interface [DirectShow],described, IVMRMixerBitmapInterface, dshow.ivmrmixerbitmap, strmif/IVMRMixerBitmap
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVMRMixerBitmap
 - strmif/IVMRMixerBitmap
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRMixerBitmap
---

# IVMRMixerBitmap interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IVMRMixerBitmap</b> interface enables an application to blend a static image from a bitmap or DirectDraw surface onto the video stream, when using the <a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-7">Video Mixing Renderer Filter 7</a> (VMR-7).


<div class="alert"><b>Note</b>  For the VMR-9, use the <a href="/previous-versions/ms787059(v=vs.85)">IVMRMixerBitmap9</a> interface.</div>
<div> </div>


You can pass images to the VMR as frequently as you like, but changing the image several times per second may impact the performance and smoothness of the video being rendered. The new image will be blended with the next and all subsequent video frames rendered by the VMR.

Internally, the VMR uses its mixer component to perform the blending operation. Therefore the VMR must be configured correctly prior to commencing video playback. Even if only a single video stream is present, applications should call <a href="/windows/desktop/api/strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams">IVMRFilterConfig::SetNumberOfStreams</a> with a value of "1" to cause the VMR to load the mixer and compositor. The image can contain embedded per pixel alpha information; this allows the image to contain regions that are transparent. Transparent areas can also be identified by a color key value. Changes in the image are only shown on the screen while the filter graph is running.

## -inheritance

The <b>IVMRMixerBitmap</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRMixerBitmap</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/displaying-an-application-supplied-bitmap-on-the-composited-image">Displaying an Application-Supplied Bitmap on the Composited Image</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>



<a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-7">Video Mixing Renderer Filter 7</a>
