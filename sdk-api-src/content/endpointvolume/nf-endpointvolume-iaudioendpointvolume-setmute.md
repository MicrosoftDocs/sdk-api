---
UID: NF:endpointvolume.IAudioEndpointVolume.SetMute
title: IAudioEndpointVolume::SetMute
author: windows-sdk-content
description: The SetMute method sets the muting state of the audio stream that enters or leaves the audio endpoint device.
old-location: coreaudio\iaudioendpointvolume_setmute.htm
old-project: CoreAudio
ms.assetid: a0ab4fef-8333-4f21-ae8e-74285788ae0e
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IAudioEndpointVolume interface [Core Audio],SetMute method, IAudioEndpointVolume.SetMute, IAudioEndpointVolume::SetMute, IAudioEndpointVolumeSetMute, SetMute, SetMute method [Core Audio], SetMute method [Core Audio],IAudioEndpointVolume interface, coreaudio.iaudioendpointvolume_setmute, endpointvolume/IAudioEndpointVolume::SetMute
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: endpointvolume.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: ProtType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Endpointvolume.h
api_name:
-	IAudioEndpointVolume.SetMute
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IAudioEndpointVolume::SetMute


## -description



The <b>SetMute</b> method sets the muting state of the audio stream that enters or leaves the audio endpoint device.




## -parameters




### -param bMute [in]

The new muting state. If <i>bMute</i> is <b>TRUE</b>, the method mutes the stream. If <b>FALSE</b>, the method turns off muting.


### -param pguidEventContext [in]

Context value for the <a href="https://msdn.microsoft.com/a8ffad44-c621-4335-a312-16e7d6af2c18">IAudioEndpointVolumeCallback::OnNotify</a> method. This parameter points to an event-context GUID. If the <b>SetMute</b> call changes the muting state of the endpoint, all clients that have registered <a href="https://msdn.microsoft.com/0b631d1b-f89c-4789-a09c-875b24a48a89">IAudioEndpointVolumeCallback</a> interfaces with that endpoint will receive notifications. In its implementation of the <b>OnNotify</b> method, a client can inspect the event-context GUID to discover whether it or another client is the source of the control-change event. If the caller supplies a <b>NULL</b> pointer for this parameter, the notification routine receives the context GUID value GUID_NULL.


## -returns



If the method succeeds and the muting state changes, the method returns S_OK. If the method succeeds and the new muting state is the same as the previous muting state, the method returns S_FALSE. If the method fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
</table>
 




## -remarks



For a code example that calls <b>SetMute</b>, see <a href="https://msdn.microsoft.com/667c3659-69ae-469d-9ae0-e32a189cbc71">Endpoint Volume Controls</a>.




## -see-also




<a href="https://msdn.microsoft.com/5e3e7ffc-8822-4b1b-b9af-206ec1e767e2">IAudioEndpointVolume Interface</a>



<a href="https://msdn.microsoft.com/0b631d1b-f89c-4789-a09c-875b24a48a89">IAudioEndpointVolumeCallback Interface</a>



<a href="https://msdn.microsoft.com/a8ffad44-c621-4335-a312-16e7d6af2c18">IAudioEndpointVolumeCallback::OnNotify</a>
 

 

