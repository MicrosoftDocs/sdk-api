---
UID: NN:evr.IMFVideoMixerControl2
title: IMFVideoMixerControl2 (evr.h)
description: Controls preferences for video deinterlacing.
helpviewer_keywords: ["IMFVideoMixerControl2","IMFVideoMixerControl2 interface [Media Foundation]","IMFVideoMixerControl2 interface [Media Foundation]","described","evr/IMFVideoMixerControl2","mf.imfvideomixercontrol2"]
old-location: mf\imfvideomixercontrol2.htm
tech.root: mfarchive
ms.assetid: a238b050-101d-4b8a-9479-984b889823f4
ms.date: 12/05/2018
ms.keywords: IMFVideoMixerControl2, IMFVideoMixerControl2 interface [Media Foundation], IMFVideoMixerControl2 interface [Media Foundation],described, evr/IMFVideoMixerControl2, mf.imfvideomixercontrol2
req.header: evr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFVideoMixerControl2
 - evr/IMFVideoMixerControl2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - evr.h
api_name:
 - IMFVideoMixerControl2
archived: true
---

# IMFVideoMixerControl2 interface


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Controls preferences for video deinterlacing.

The default video mixer for the <a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a> (EVR) implements this interface.

To get a pointer to the interface, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a> on any of the following objects, using the <b>MR_VIDEO_MIXER_SERVICE</b> service identifier:
<ul>
<li>The <a href="/windows/desktop/medfound/media-session">Media Session</a>, if the topology contains an instance of the EVR.</li>
<li>The EVR media sink.</li>
<li>The  DirectShow EVR filter.</li>
<li>The EVR mixer.</li>
</ul>

## -inheritance

The <b>IMFVideoMixerControl2</b> interface inherits from <a href="/windows/desktop/api/evr/nn-evr-imfvideomixercontrol">IMFVideoMixerControl</a>. <b>IMFVideoMixerControl2</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/evr/nn-evr-imfvideomixercontrol">IMFVideoMixerControl</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/video-quality-management">Video Quality Management</a>
