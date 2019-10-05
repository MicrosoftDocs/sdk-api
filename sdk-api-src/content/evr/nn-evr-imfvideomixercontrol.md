---
UID: NN:evr.IMFVideoMixerControl
title: IMFVideoMixerControl (evr.h)
author: windows-sdk-content
description: Controls how the Enhanced Video Renderer (EVR) mixes video substreams.
old-location: mf\imfvideomixercontrol.htm
tech.root: medfound
ms.assetid: 8b5f54e3-c6da-4201-857a-9c718ad911db
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 8b5f54e3-c6da-4201-857a-9c718ad911db, IMFVideoMixerControl, IMFVideoMixerControl interface [Media Foundation], IMFVideoMixerControl interface [Media Foundation],described, evr/IMFVideoMixerControl, mf.imfvideomixercontrol
ms.topic: interface
f1_keywords: 
 - "evr/IMFVideoMixerControl"
dev_langs:
 - c++
req.header: evr.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFVideoMixerControl
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFVideoMixerControl interface


## -description


Controls how the <a href="https://docs.microsoft.com/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a> (EVR) mixes video substreams. Applications can use this interface to control video mixing during playback.

The EVR mixer implements this interface. To get a pointer to the interface, call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a>. The service identifier GUID is MR_VIDEO_MIXER_SERVICE. Call <b>GetService</b> on any of the following objects:
<ul>
<li>The <a href="https://docs.microsoft.com/windows/desktop/medfound/media-session">Media Session</a>, if the topology contains an instance of the EVR.
            </li>
<li>The EVR media sink.
            </li>
<li>The DirectShow EVR filter.
            </li>
<li>The EVR mixer.
            </li>
</ul>If you implement a custom mixer for the EVR, the mixer can optionally expose this interface as a service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFVideoMixerControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFVideoMixerControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFVideoMixerControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-imfvideomixercontrol-getstreamoutputrect">GetStreamOutputRect</a>
</td>
<td align="left" width="63%">
Retrieves the position of a video stream within the composition rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-imfvideomixercontrol-getstreamzorder">GetStreamZOrder</a>
</td>
<td align="left" width="63%">
Retrieves the z-order of a video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-imfvideomixercontrol-setstreamoutputrect">SetStreamOutputRect</a>
</td>
<td align="left" width="63%">
Sets the position of a video stream within the composition rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-imfvideomixercontrol-setstreamzorder">SetStreamZOrder</a>
</td>
<td align="left" width="63%">
Sets the z-order of a video stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

