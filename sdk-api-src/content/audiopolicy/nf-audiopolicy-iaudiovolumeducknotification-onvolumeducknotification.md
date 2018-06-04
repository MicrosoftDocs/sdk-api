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

# IAudioVolumeDuckNotification::OnVolumeDuckNotification


## -description


The <b>OnVolumeDuckNotification</b> method sends a notification about a pending system ducking event. For more information, see <a href="https://msdn.microsoft.com/1b92574e-7cde-49c0-a68e-223492412361">Implementation Considerations for Ducking Notifications</a>.


## -parameters




### -param sessionID [in]

A string containing the session instance identifier of the communications session that raises the  the auto-ducking event. To get the session instance identifier, call <a href="https://msdn.microsoft.com/02350812-7f05-400e-87f7-1d912a23050d">IAudioSessionControl2::GetSessionInstanceIdentifier</a>.


### -param countCommunicationSessions






#### - countCommunicationsSessions [in]

The number of active 
    communications sessions. If there are n sessions, the sessions are numbered from 0 to –1.


## -returns



If the method succeeds, it returns S_OK. 





## -remarks



After the application registers its implementation  of the <a href="https://msdn.microsoft.com/08e90a50-a6ac-4405-ba90-a862b78efaf8">IAudioVolumeDuckNotification</a> interface by calling <a href="https://msdn.microsoft.com/bed27f3f-6293-4a25-baa0-39562d45bddc">IAudioSessionManager2::RegisterDuckNotification</a>, the session manager calls <b>OnVolumeDuckNotification</b> when it wants to send a notification about when ducking begins. The application receives the event notifications in the form of callbacks.




## -see-also




<a href="https://msdn.microsoft.com/08e90a50-a6ac-4405-ba90-a862b78efaf8">IAudioVolumeDuckNotification</a>



<a href="https://msdn.microsoft.com/bec2127d-fb82-436d-beee-d43e8fef5c35">Using a Communication Device</a>
 

 

