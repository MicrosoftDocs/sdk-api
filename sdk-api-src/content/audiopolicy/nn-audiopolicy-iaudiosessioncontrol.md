---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IAudioSessionControl interface


## -description



The <b>IAudioSessionControl</b> interface enables a client to configure the control parameters for an <a href="https://msdn.microsoft.com/b8a1b656-a582-4112-99e9-bd575719ebb3">audio session</a> and to monitor events in the session. The <a href="https://msdn.microsoft.com/eb778503-06f8-4705-9f8d-9a4fd886ae27">IAudioClient::Initialize</a> method initializes a stream object and assigns the stream to an audio session. The client obtains a reference to the <b>IAudioSessionControl</b> interface on a stream object by calling the <a href="https://msdn.microsoft.com/233d4471-037f-4df9-bef6-57f2544dedb5">IAudioClient::GetService</a> method with parameter <i>riid</i> set to <b>REFIID</b> IID_IAudioSessionControl.

Alternatively, a client can obtain the <b>IAudioSessionControl</b> interface of an existing session without having to first create a stream object and add the stream to the session. Instead, the client calls the <a href="https://msdn.microsoft.com/42de66dd-46df-40af-9d8a-39ee9f91b468">IAudioSessionManager::GetAudioSessionControl</a> method with parameter <i>AudioSessionGuid</i> set to the session GUID.

The client can register to receive notification from the session manager when clients change session parameters through the methods in the <b>IAudioSessionControl</b> interface.

When releasing an <b>IAudioSessionControl</b> interface instance, the client must call the interface's <b>Release</b> method from the same thread as the call to <b>IAudioClient::GetService</b> that created the object.

The <b>IAudioSessionControl</b> interface controls an audio session. An audio session is a collection of shared-mode streams. This interface does not work with exclusive-mode streams.

For a code example that uses the <b>IAudioSessionControl</b> interface, see <a href="https://msdn.microsoft.com/91a93b79-2563-4b25-af5d-ca5f7d35d77b">Audio Events for Legacy Audio Applications</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioSessionControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAudioSessionControl</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/28493e3a-ee5a-4331-b5b5-ba0bf2ee3370">GetDisplayName</a>
</td>
<td align="left" width="63%">
Retrieves the display name for the audio session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d636aad7-c8b3-4179-ac32-5cb283611499">GetGroupingParam</a>
</td>
<td align="left" width="63%">
Retrieves the grouping parameter of the audio session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5b2721a-fd0a-483d-a94c-6e1520f5764c">GetIconPath</a>
</td>
<td align="left" width="63%">
Retrieves the path for the display icon for the audio session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c0188a1-7982-40f0-9040-bda00473160c">GetState</a>
</td>
<td align="left" width="63%">
Retrieves the current state of the audio session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f0004eb6-1b3c-4f78-9ab4-17b30dec0d94">RegisterAudioSessionNotification</a>
</td>
<td align="left" width="63%">
Registers the client to receive notifications of session events, including changes in the session state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d12c12ed-a556-4743-952e-2eb4f58ee0eb">SetDisplayName</a>
</td>
<td align="left" width="63%">
Assigns a display name to the current audio session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/990bebd9-c37d-4f72-b349-a43a074d8992">SetGroupingParam</a>
</td>
<td align="left" width="63%">
Assigns a session to a grouping of sessions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25b27a65-7204-4a12-ae4e-ad216a22e4e1">SetIconPath</a>
</td>
<td align="left" width="63%">
Assigns a display icon to the current session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b496d58-c855-44b8-b437-6cb6017dcc9d">UnregisterAudioSessionNotification</a>
</td>
<td align="left" width="63%">
Deletes a previous registration by the client to receive notifications.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/233d4471-037f-4df9-bef6-57f2544dedb5">IAudioClient::GetService</a>



<a href="https://msdn.microsoft.com/eb778503-06f8-4705-9f8d-9a4fd886ae27">IAudioClient::Initialize</a>



<a href="https://msdn.microsoft.com/42de66dd-46df-40af-9d8a-39ee9f91b468">IAudioSessionManager::GetAudioSessionControl</a>



<a href="https://msdn.microsoft.com/452b9725-b0b9-4888-bbb5-a23e0067e840">WASAPI</a>
 

 

