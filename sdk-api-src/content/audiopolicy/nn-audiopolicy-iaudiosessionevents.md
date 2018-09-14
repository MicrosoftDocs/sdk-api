---
UID: NN:audiopolicy.IAudioSessionEvents
title: IAudioSessionEvents
author: windows-sdk-content
description: The IAudioSessionEvents interface provides notifications of session-related events such as changes in the volume level, display name, and session state.
old-location: coreaudio\iaudiosessionevents.htm
tech.root: CoreAudio
ms.assetid: fd287ef7-8a37-4342-b4c2-79b84a56c30e
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IAudioSessionEvents, IAudioSessionEvents interface [Core Audio], IAudioSessionEvents interface [Core Audio],described, audiopolicy/IAudioSessionEvents, coreaudio.iaudiosessionevents
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioSessionEvents interface


## -description



The <b>IAudioSessionEvents</b> interface provides notifications of session-related events such as changes in the volume level, display name, and session state. Unlike the other interfaces in this section, which are implemented by the WASAPI system component, a WASAPI client implements the <b>IAudioSessionEvents</b> interface. To receive event notifications, the client passes a pointer to its <b>IAudioSessionEvents</b> interface to the <a href="https://msdn.microsoft.com/f0004eb6-1b3c-4f78-9ab4-17b30dec0d94">IAudioSessionControl::RegisterAudioSessionNotification</a> method.

After registering its <b>IAudioClientSessionEvents</b> interface, the client receives event notifications in the form of callbacks through the methods in the interface.

In implementing the <b>IAudioSessionEvents</b> interface, the client should observe these rules to avoid deadlocks and undefined behavior:

<ul>
<li>The methods in the interface must be nonblocking. The client should never wait on a synchronization object during an event callback.</li>
<li>The client should never call the <a href="https://msdn.microsoft.com/1b496d58-c855-44b8-b437-6cb6017dcc9d">IAudioSessionControl::UnregisterAudioSessionNotification</a> method during an event callback.</li>
<li>The client should never release the final reference on a WASAPI object during an event callback.</li>
</ul>
For a code example that implements an <b>IAudioSessionEvents</b> interface, see <a href="https://msdn.microsoft.com/6943b405-0807-412b-a149-fc3a8ece1b48">Audio Session Events</a>. For a code example that registers a client's <b>IAudioSessionEvents</b> interface to receive notifications, see <a href="https://msdn.microsoft.com/91a93b79-2563-4b25-af5d-ca5f7d35d77b">Audio Events for Legacy Audio Applications</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioSessionEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAudioSessionEvents</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/cdd3ec9b-cf72-4c2e-b874-60370d41447d">OnChannelVolumeChanged</a>
</td>
<td align="left" width="63%">
Notifies the client that the volume level of an audio channel in the session submix has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/65d21f0c-b6f1-4506-975c-6d0308b3fc2f">OnDisplayNameChanged</a>
</td>
<td align="left" width="63%">
Notifies the client that the display name for the session has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f52c9d8a-245b-489a-81c1-cb4715faa8be">OnGroupingParamChanged</a>
</td>
<td align="left" width="63%">
Notifies the client that the grouping parameter for the session has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32669e52-28bf-4739-9f39-6e0175ca779c">OnIconPathChanged</a>
</td>
<td align="left" width="63%">
Notifies the client that the display icon for the session has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9fd653f0-c9d1-4155-9c1e-7e6124b40cca">OnSessionDisconnected</a>
</td>
<td align="left" width="63%">
Notifies the client that the session has been disconnected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e60e8996-3c01-4458-88f2-cd6cb118bd76">OnSimpleVolumeChanged</a>
</td>
<td align="left" width="63%">
Notifies the client that the volume level or muting state of the session has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ec3e676-cf08-4041-b5bf-5cb429569e03">OnStateChanged</a>
</td>
<td align="left" width="63%">
Notifies the client that the stream-activity state of the session has changed.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/f0004eb6-1b3c-4f78-9ab4-17b30dec0d94">IAudioSessionControl::RegisterAudioSessionNotification</a>



<a href="https://msdn.microsoft.com/1b496d58-c855-44b8-b437-6cb6017dcc9d">IAudioSessionControl::UnregisterAudioSessionNotification</a>



<a href="https://msdn.microsoft.com/452b9725-b0b9-4888-bbb5-a23e0067e840">WASAPI</a>
 

 

