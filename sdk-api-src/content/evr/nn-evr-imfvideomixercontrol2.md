---
UID: NN:evr.IMFVideoMixerControl2
title: IMFVideoMixerControl2 (evr.h)
description: Controls preferences for video deinterlacing.helpviewer_keywords: ["IMFVideoMixerControl2","IMFVideoMixerControl2 interface [Media Foundation]","IMFVideoMixerControl2 interface [Media Foundation]","described","evr/IMFVideoMixerControl2","mf.imfvideomixercontrol2"]
old-location: mf\imfvideomixercontrol2.htm
tech.root: medfound
ms.assetid: a238b050-101d-4b8a-9479-984b889823f4
ms.date: 12/05/2018
ms.keywords: IMFVideoMixerControl2, IMFVideoMixerControl2 interface [Media Foundation], IMFVideoMixerControl2 interface [Media Foundation],described, evr/IMFVideoMixerControl2, mf.imfvideomixercontrol2
f1_keywords:
- evr/IMFVideoMixerControl2
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- evr.h
api_name:
- IMFVideoMixerControl2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFVideoMixerControl2 interface


## -description


Controls preferences for video deinterlacing.

The default video mixer for the <a href="https://docs.microsoft.com/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a> (EVR) implements this interface.

To get a pointer to the interface, call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a> on any of the following objects, using the <b>MR_VIDEO_MIXER_SERVICE</b> service identifier:
<ul>
<li>The <a href="https://docs.microsoft.com/windows/desktop/medfound/media-session">Media Session</a>, if the topology contains an instance of the EVR.</li>
<li>The EVR media sink.</li>
<li>The  DirectShow EVR filter.</li>
<li>The EVR mixer.</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFVideoMixerControl2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/evr/nn-evr-imfvideomixercontrol">IMFVideoMixerControl</a>. <b>IMFVideoMixerControl2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFVideoMixerControl2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-imfvideomixercontrol2-getmixingprefs">GetMixingPrefs</a>
</td>
<td align="left" width="63%">
Gets the current preferences for video deinterlacing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-imfvideomixercontrol2-setmixingprefs">SetMixingPrefs</a>
</td>
<td align="left" width="63%">
Sets the preferences for video deinterlacing.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/evr/nn-evr-imfvideomixercontrol">IMFVideoMixerControl</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/video-quality-management">Video Quality Management</a>
 

 

