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

# IAudioSessionManager interface


## -description



The <b>IAudioSessionManager</b> interface enables a client to access the session controls and volume controls for both cross-process and process-specific audio sessions. The client obtains a reference to an <b>IAudioSessionManager</b> interface by calling the <a href="https://msdn.microsoft.com/12e4a117-1fa3-49c8-949b-8973edf7e12e">IMMDevice::Activate</a> method with parameter <i>iid</i> set to <b>REFIID</b> IID_IAudioSessionManager.

This interface enables clients to access the controls for an existing session without first opening a stream. This capability is useful for clients of higher-level APIs that are built on top of WASAPI and use session controls internally but do not give their clients access to session controls.

In Windows Vista, the higher-level APIs that use WASAPI include Media Foundation, DirectSound, the Windows multimedia <b>waveInXxx</b>, <b>waveOutXxx</b>, and <b>mciXxx</b> functions, and third-party APIs.

When a client creates an audio stream through a higher-level API, that API typically adds the stream to the default audio session for the client's process (the session that is identified by the session GUID value, GUID_NULL), but the same API might not provide a means for the client to access the controls for that session. In that case, the client can access the controls through the <b>IAudioSessionManager</b> interface.

For a code example that uses the <b>IAudioSessionManager</b> interface, see <a href="https://msdn.microsoft.com/91a93b79-2563-4b25-af5d-ca5f7d35d77b">Audio Events for Legacy Audio Applications</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioSessionManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAudioSessionManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioSessionManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42de66dd-46df-40af-9d8a-39ee9f91b468">GetAudioSessionControl</a>
</td>
<td align="left" width="63%">
Retrieves an audio session control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f3c5a40-308f-48b4-b35c-aebd0cc6b849">GetSimpleAudioVolume</a>
</td>
<td align="left" width="63%">
Retrieves a simple audio volume control.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/12e4a117-1fa3-49c8-949b-8973edf7e12e">IMMDevice::Activate</a>



<a href="https://msdn.microsoft.com/452b9725-b0b9-4888-bbb5-a23e0067e840">WASAPI</a>
 

 

