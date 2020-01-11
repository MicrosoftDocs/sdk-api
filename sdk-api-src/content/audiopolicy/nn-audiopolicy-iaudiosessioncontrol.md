---
UID: NN:audiopolicy.IAudioSessionControl
title: IAudioSessionControl (audiopolicy.h)
description: The IAudioSessionControl interface enables a client to configure the control parameters for an audio session and to monitor events in the session.
old-location: coreaudio\iaudiosessioncontrol.htm
tech.root: CoreAudio
ms.assetid: 4446140e-2e61-40ed-b0f9-4c1b90e7c2de
ms.date: 12/05/2018
ms.keywords: IAudioSessionControl, IAudioSessionControl interface [Core Audio], IAudioSessionControl interface [Core Audio],described, audiopolicy/IAudioSessionControl, coreaudio.iaudiosessioncontrol
f1_keywords:
- audiopolicy/IAudioSessionControl
dev_langs:
- c++
req.header: audiopolicy.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
- Audiopolicy.h
api_name:
- IAudioSessionControl
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioSessionControl interface


## -description



The <b>IAudioSessionControl</b> interface enables a client to configure the control parameters for an <a href="https://docs.microsoft.com/windows/desktop/CoreAudio/audio-sessions">audio session</a> and to monitor events in the session. The <a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a> method initializes a stream object and assigns the stream to an audio session. The client obtains a reference to the <b>IAudioSessionControl</b> interface on a stream object by calling the <a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getservice">IAudioClient::GetService</a> method with parameter <i>riid</i> set to <b>REFIID</b> IID_IAudioSessionControl.

Alternatively, a client can obtain the <b>IAudioSessionControl</b> interface of an existing session without having to first create a stream object and add the stream to the session. Instead, the client calls the <a href="https://docs.microsoft.com/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager-getaudiosessioncontrol">IAudioSessionManager::GetAudioSessionControl</a> method with parameter <i>AudioSessionGuid</i> set to the session GUID.

The client can register to receive notification from the session manager when clients change session parameters through the methods in the <b>IAudioSessionControl</b> interface.

When releasing an <b>IAudioSessionControl</b> interface instance, the client must call the interface's <b>Release</b> method from the same thread as the call to <b>IAudioClient::GetService</b> that created the object.

The <b>IAudioSessionControl</b> interface controls an audio session. An audio session is a collection of shared-mode streams. This interface does not work with exclusive-mode streams.

For a code example that uses the <b>IAudioSessionControl</b> interface, see <a href="https://docs.microsoft.com/windows/desktop/CoreAudio/audio-events-for-legacy-audio-applications">Audio Events for Legacy Audio Applications</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioSessionControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioSessionControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioSessionControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-getdisplayname">GetDisplayName</a>
</td>
<td align="left" width="63%">
Retrieves the display name for the audio session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-getgroupingparam">GetGroupingParam</a>
</td>
<td align="left" width="63%">
Retrieves the grouping parameter of the audio session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-geticonpath">GetIconPath</a>
</td>
<td align="left" width="63%">
Retrieves the path for the display icon for the audio session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-getstate">GetState</a>
</td>
<td align="left" width="63%">
Retrieves the current state of the audio session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification">RegisterAudioSessionNotification</a>
</td>
<td align="left" width="63%">
Registers the client to receive notifications of session events, including changes in the session state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-setdisplayname">SetDisplayName</a>
</td>
<td align="left" width="63%">
Assigns a display name to the current audio session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-setgroupingparam">SetGroupingParam</a>
</td>
<td align="left" width="63%">
Assigns a session to a grouping of sessions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-seticonpath">SetIconPath</a>
</td>
<td align="left" width="63%">
Assigns a display icon to the current session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-unregisteraudiosessionnotification">UnregisterAudioSessionNotification</a>
</td>
<td align="left" width="63%">
Deletes a previous registration by the client to receive notifications.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getservice">IAudioClient::GetService</a>



<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a>



<a href="https://docs.microsoft.com/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager-getaudiosessioncontrol">IAudioSessionManager::GetAudioSessionControl</a>



<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/wasapi">WASAPI</a>
 

 

