---
UID: NN:evr9.IMFVideoMixerBitmap
title: IMFVideoMixerBitmap (evr9.h)
description: Alpha-blends a static bitmap image with the video displayed by the Enhanced Video Renderer (EVR).
helpviewer_keywords: ["4da4bdb9-857b-40c9-b910-04a099a23ab5","IMFVideoMixerBitmap","IMFVideoMixerBitmap interface [Media Foundation]","IMFVideoMixerBitmap interface [Media Foundation]","described","evr9/IMFVideoMixerBitmap","mf.imfvideomixerbitmap"]
old-location: mf\imfvideomixerbitmap.htm
tech.root: mfarchive
ms.assetid: 4da4bdb9-857b-40c9-b910-04a099a23ab5
ms.date: 12/05/2018
ms.keywords: 4da4bdb9-857b-40c9-b910-04a099a23ab5, IMFVideoMixerBitmap, IMFVideoMixerBitmap interface [Media Foundation], IMFVideoMixerBitmap interface [Media Foundation],described, evr9/IMFVideoMixerBitmap, mf.imfvideomixerbitmap
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFVideoMixerBitmap
 - evr9/IMFVideoMixerBitmap
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFVideoMixerBitmap
archived: true
---

# IMFVideoMixerBitmap interface


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Alpha-blends a static bitmap image with the video displayed by the <a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a> (EVR).

The EVR mixer implements this interface. To get a pointer to the interface, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a>. The service identifier GUID is MR_VIDEO_MIXER_SERVICE. Call <b>GetService</b> on any of the following objects:
<ul>
<li>The <a href="/windows/desktop/medfound/media-session">Media Session</a>, if the topology contains an instance of the EVR.
            </li>
<li>The EVR media sink.
            </li>
<li>The DirectShow EVR filter.
            </li>
<li>The EVR mixer.
            </li>
</ul>If you implement a custom mixer for the EVR, the mixer can optionally expose this interface as a service.

## -inheritance

The <b>IMFVideoMixerBitmap</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFVideoMixerBitmap</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
