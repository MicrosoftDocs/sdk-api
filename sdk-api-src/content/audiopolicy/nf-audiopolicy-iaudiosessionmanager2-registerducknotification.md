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

# IAudioSessionManager2::RegisterDuckNotification


## -description


The <b>RegisterDuckNotification</b> method registers the application with the session manager to receive ducking notifications.


## -parameters




### -param sessionID




### -param duckNotification

Pointer to the application's implementation of the <a href="https://msdn.microsoft.com/08e90a50-a6ac-4405-ba90-a862b78efaf8">IAudioVolumeDuckNotification</a> interface. The implementation is called when ducking events are raised by the audio system and  notifications are sent to the registered applications. 


#### - SessionID

Pointer to a null-terminated string that contains a  session instance identifier. Applications that are playing a media stream and want to provide custom stream attenuation or ducking behavior, pass their own session instance identifier.  For more information, see Remarks.

Other applications
    that do not want to alter their streams but want to get all the ducking notifications
    must pass <b>NULL</b>.


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
<dt>E_POINTER</dt>
</dl>
</td>
<td width="60%">
<i>duckNotification</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_OUTOFMEMORY</dt>
</dl>
</td>
<td width="60%">
Internal object could not be created due to insufficient memory.

</td>
</tr>
</table>
 




## -remarks



<i>Stream Attenuation</i> or <i>ducking</i> is a new feature in Windows 7. An application playing a media stream can make the stream behave differently when a new communication stream is opened on the default communication device. For example, the original media stream can be paused while the new communication stream is open. To provide this custom implementation for stream attenuation, the application can opt out of the default stream attenuation experience by calling <a href="https://msdn.microsoft.com/6689d7e4-9c45-483d-9f46-14d157726b02">IAudioSessionControl::SetDuckingPreference</a> and then register itself to receive notifications when session events occur. For stream attenuation, a session event is raised by the system when a communication stream is opened or closed on the default communication device. For more information about this feature, see <a href="https://msdn.microsoft.com/1b92574e-7cde-49c0-a68e-223492412361">Getting Ducking Events</a>.

To begin receiving notifications, the application calls the <b>RegisterDuckNotification</b> method to register its <a href="https://msdn.microsoft.com/08e90a50-a6ac-4405-ba90-a862b78efaf8">IAudioVolumeDuckNotification</a> interface with the session manager. When the application no longer requires notifications, it calls the <a href="https://msdn.microsoft.com/0ab0f5d0-8831-41a2-bfee-3e88a3d92156">IAudioSessionManager2::UnregisterDuckNotification</a> method to delete the registration.

The application receives notifications about the ducking events through the methods of the <a href="https://msdn.microsoft.com/08e90a50-a6ac-4405-ba90-a862b78efaf8">IAudioVolumeDuckNotification</a> interface. The application implements <b>IAudioVolumeDuckNotification</b>. After the registration call has succeeded, the system calls the methods of this interface when session events occur.






## -see-also




<a href="https://msdn.microsoft.com/476dac90-d0c4-499c-973e-33ea55546659">IAudioSessionManager2</a>



<a href="https://msdn.microsoft.com/bec2127d-fb82-436d-beee-d43e8fef5c35">Using a Communication Device</a>
 

 

