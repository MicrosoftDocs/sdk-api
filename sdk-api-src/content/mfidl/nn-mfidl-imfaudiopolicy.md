---
UID: NN:mfidl.IMFAudioPolicy
title: IMFAudioPolicy (mfidl.h)
author: windows-sdk-content
description: Configures the audio session that is associated with the streaming audio renderer (SAR).
old-location: mf\imfaudiopolicy.htm
tech.root: medfound
ms.assetid: fcd4dbfb-3f9f-4089-b9cc-7b41b2c2678a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFAudioPolicy, IMFAudioPolicy interface [Media Foundation], IMFAudioPolicy interface [Media Foundation],described, fcd4dbfb-3f9f-4089-b9cc-7b41b2c2678a, mf.imfaudiopolicy, mfidl/IMFAudioPolicy
ms.topic: interface
f1_keywords: ["mfidl/IMFAudioPolicy"]
req.header: mfidl.h
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFAudioPolicy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFAudioPolicy interface


## -description


Configures the audio session that is associated with the streaming audio renderer (SAR). Use this interface to change how the audio session appears in the Windows volume control.

The SAR exposes this interface as a service. To get a pointer to the interface, call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a> with the service identifier MR_AUDIO_POLICY_SERVICE. You can call <b>GetService</b> directly on the SAR or call it on the Media Session.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFAudioPolicy</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFAudioPolicy</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFAudioPolicy</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getdisplayname">GetDisplayName</a>
</td>
<td align="left" width="63%">
Retrieves the display name of the audio session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getgroupingparam">GetGroupingParam</a>
</td>
<td align="left" width="63%">
Retrieves the group of sessions to which this audio session belongs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath">GetIconPath</a>
</td>
<td align="left" width="63%">
Retrieves the icon resource for the audio session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-setdisplayname">SetDisplayName</a>
</td>
<td align="left" width="63%">
Sets the display name of the audio session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-setgroupingparam">SetGroupingParam</a>
</td>
<td align="left" width="63%">
Assigns the audio session to a group of sessions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-seticonpath">SetIconPath</a>
</td>
<td align="left" width="63%">
Sets the icon resource for the audio session.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/streaming-audio-renderer">Streaming Audio Renderer</a>
 

 

