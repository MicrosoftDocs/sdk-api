---
UID: NN:audiopolicy.IAudioSessionEvents
title: IAudioSessionEvents (audiopolicy.h)
description: The IAudioSessionEvents interface provides notifications of session-related events such as changes in the volume level, display name, and session state.
old-location: coreaudio\iaudiosessionevents.htm
tech.root: CoreAudio
ms.assetid: fd287ef7-8a37-4342-b4c2-79b84a56c30e
ms.date: 12/05/2018
ms.keywords: IAudioSessionEvents, IAudioSessionEvents interface [Core Audio], IAudioSessionEvents interface [Core Audio],described, audiopolicy/IAudioSessionEvents, coreaudio.iaudiosessionevents
f1_keywords:
- audiopolicy/IAudioSessionEvents
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
- IAudioSessionEvents
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioSessionEvents interface


## -description



The <b>IAudioSessionEvents</b> interface provides notifications of session-related events such as changes in the volume level, display name, and session state. Unlike the other interfaces in this section, which are implemented by the WASAPI system component, a WASAPI client implements the <b>IAudioSessionEvents</b> interface. To receive event notifications, the client passes a pointer to its <b>IAudioSessionEvents</b> interface to the <a href="https://docs.microsoft.com/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification">IAudioSessionControl::RegisterAudioSessionNotification</a> method.

After registering its <b>IAudioClientSessionEvents</b> interface, the client receives event notifications in the form of callbacks through the methods in the interface.

In implementing the <b>IAudioSessionEvents</b> interface, the client should observe these rules to avoid deadlocks and undefined behavior:

<ul>
<li>The methods in the interface must be nonblocking. The client should never wait on a synchronization object during an event callback.</li>
<li>The client should never call the <a href="https://docs.microsoft.com/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-unregisteraudiosessionnotification">IAudioSessionControl::UnregisterAudioSessionNotification</a> method during an event callback.</li>
<li>The client should never release the final reference on a WASAPI object during an event callback.</li>
</ul>
For a code example that implements an <b>IAudioSessionEvents</b> interface, see <a href="https://docs.microsoft.com/windows/desktop/CoreAudio/audio-session-events">Audio Session Events</a>. For a code example that registers a client's <b>IAudioSessionEvents</b> interface to receive notifications, see <a href="https://docs.microsoft.com/windows/desktop/CoreAudio/audio-events-for-legacy-audio-applications">Audio Events for Legacy Audio Applications</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioSessionEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioSessionEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioSessionEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged">OnChannelVolumeChanged</a>
</td>
<td align="left" width="63%">
Notifies the client that the volume level of an audio channel in the session submix has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ondisplaynamechanged">OnDisplayNameChanged</a>
</td>
<td align="left" width="63%">
Notifies the client that the display name for the session has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ongroupingparamchanged">OnGroupingParamChanged</a>
</td>
<td align="left" width="63%">
Notifies the client that the grouping parameter for the session has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-oniconpathchanged">OnIconPathChanged</a>
</td>
<td align="left" width="63%">
Notifies the client that the display icon for the session has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected">OnSessionDisconnected</a>
</td>
<td align="left" width="63%">
Notifies the client that the session has been disconnected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged">OnSimpleVolumeChanged</a>
</td>
<td align="left" width="63%">
Notifies the client that the volume level or muting state of the session has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onstatechanged">OnStateChanged</a>
</td>
<td align="left" width="63%">
Notifies the client that the stream-activity state of the session has changed.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification">IAudioSessionControl::RegisterAudioSessionNotification</a>



<a href="https://docs.microsoft.com/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-unregisteraudiosessionnotification">IAudioSessionControl::UnregisterAudioSessionNotification</a>



<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/wasapi">WASAPI</a>
 

 

