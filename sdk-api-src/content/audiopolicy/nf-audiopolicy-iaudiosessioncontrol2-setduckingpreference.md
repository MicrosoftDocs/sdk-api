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

# IAudioSessionControl2::SetDuckingPreference


## -description


The <b>SetDuckingPreference</b> method enables or disables the default stream attenuation experience (auto-ducking) provided by the system.


## -parameters




### -param optOut [in]

A <b>BOOL</b> variable that enables or disables system auto-ducking.


## -returns



If the method succeeds, it returns S_OK.
          If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>AUDCLNT_E_DEVICE_INVALIDATED</dt>
</dl>
</td>
<td width="60%">
The audio session is disconnected on the default audio device.

</td>
</tr>
</table>
 




## -remarks



    By default, the system adjusts the volume for all currently playing sounds when the system starts a communication session and receives a new communication stream on the default communication device. For more information about this feature, see <a href="https://msdn.microsoft.com/bec2127d-fb82-436d-beee-d43e8fef5c35">Using a Communication Device</a>.

If the application passes <b>TRUE</b> in <i>optOut</i>, the system disables the <a href="https://msdn.microsoft.com/2ad9482f-1888-4f19-bc41-9d47a8e0ed15">Default Ducking Experience</a>. For more information, see <a href="https://msdn.microsoft.com/5604b927-99f8-450f-a48c-b38d782584de">Disabling the Default Ducking Experience</a>.

To provide a custom implementation, the application needs to get notifications from the system when it opens or closes the communication stream. To receive the notifications, the application must call this method before registering itself by calling <b>IAudioSessionManager2::RegisterForDuckNotification</b>. For more information and example code, see <a href="https://msdn.microsoft.com/709ad912-6b03-4ad3-bc47-ad8b6bd6de45">Getting Ducking Events</a>.

If the application passes <b>FALSE</b> in <i>optOut</i>, the application provides the default stream attenuation experience provided by the system.

We recommend that the application call <b>SetDuckingPreference</b> during stream creation.  However, this method can be called dynamically during the session to change the initial preference.





## -see-also




<a href="https://msdn.microsoft.com/3bb65edf-103c-4eeb-82b4-7c571cddfcf3">IAudioSessionControl2</a>
 

 

