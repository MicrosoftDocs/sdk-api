---
UID: NF:audiopolicy.IAudioVolumeDuckNotification.OnVolumeUnduckNotification
title: IAudioVolumeDuckNotification::OnVolumeUnduckNotification method
author: windows-driver-content
description: The OnVolumeUnduckNotification method sends a notification about a pending system unducking event.
old-location: coreaudio\iaudiovolumeducknotification_onvolumeunducknotification.htm
old-project: CoreAudio
ms.assetid: f25f066e-999f-45ff-8287-afa8acb82a19
ms.author: windowsdriverdev
ms.date: 4/4/2018
ms.keywords: IAudioVolumeDuckNotification, IAudioVolumeDuckNotification interface [Core Audio], OnVolumeUnduckNotification method, IAudioVolumeDuckNotification::OnVolumeUnduckNotification, OnVolumeUnduckNotification method [Core Audio], OnVolumeUnduckNotification method [Core Audio], IAudioVolumeDuckNotification interface, OnVolumeUnduckNotification,IAudioVolumeDuckNotification.OnVolumeUnduckNotification, audiopolicy/IAudioVolumeDuckNotification::OnVolumeUnduckNotification, coreaudio.iaudiovolumeducknotification_onvolumeunducknotification
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: audiopolicy.h
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
req.typenames: UNCOMPRESSEDAUDIOFORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AudioPolicy.h
api_name:
-	IAudioVolumeDuckNotification.OnVolumeUnduckNotification
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioVolumeDuckNotification::OnVolumeUnduckNotification method


## -description


The <b>OnVolumeUnduckNotification</b> method sends a notification about a pending system unducking event. For more information, see <a href="https://msdn.microsoft.com/1b92574e-7cde-49c0-a68e-223492412361">Implementation Considerations for Ducking Notifications</a>.


## -parameters




### -param sessionID [in]

A string containing the session instance identifier of the terminating communications session that intiated the ducking. To get the session instance identifier, call <a href="https://msdn.microsoft.com/02350812-7f05-400e-87f7-1d912a23050d">IAudioSessionControl2::GetSessionInstanceIdentifier</a>.


#### - countCommunicationsSessions [in]

The number of active 
    communications sessions. If there are n sessions, they are numbered from 0 to n-1.


## -returns



If the method succeeds, it returns S_OK. 





## -remarks



After the application registers its implementation  of the <a href="https://msdn.microsoft.com/08e90a50-a6ac-4405-ba90-a862b78efaf8">IAudioVolumeDuckNotification</a> interface by calling <a href="https://msdn.microsoft.com/bed27f3f-6293-4a25-baa0-39562d45bddc">IAudioSessionManager2::RegisterDuckNotification</a>, the session manager calls <b>OnVolumeUnduckNotification</b> when it wants to send a notification about when ducking ends. The application receives the event notifications in the form of callbacks.




## -see-also




<a href="https://msdn.microsoft.com/08e90a50-a6ac-4405-ba90-a862b78efaf8">IAudioVolumeDuckNotification</a>



<a href="https://msdn.microsoft.com/bec2127d-fb82-436d-beee-d43e8fef5c35">Using a Communication Device</a>
 

 

