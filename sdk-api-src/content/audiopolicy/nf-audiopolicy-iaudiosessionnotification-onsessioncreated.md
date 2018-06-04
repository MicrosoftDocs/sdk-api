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

# IAudioSessionNotification::OnSessionCreated


## -description


The <b>OnSessionCreated</b> method notifies the registered processes that the audio session has been created.
      


## -parameters




### -param NewSession [in]

Pointer to the <a href="https://msdn.microsoft.com/4446140e-2e61-40ed-b0f9-4c1b90e7c2de">IAudioSessionControl</a> interface of the audio session that was created.


## -returns



If the method succeeds, it returns S_OK.
          




## -remarks



After registering its <a href="https://msdn.microsoft.com/69222168-87d7-4f5a-93b1-6d91263a54bd">IAudioSessionNotification</a> interface, the application receives event notifications in the form of callbacks through the methods of the interface.

The audio engine calls <b>OnSessionCreated</b> when a new session is activated on the device endpoint.
This method is called from the session manager thread.  This method must take a reference to the session in the <i>NewSession</i> parameter if it wants to keep the reference after this call completes.




## -see-also




<a href="https://msdn.microsoft.com/69222168-87d7-4f5a-93b1-6d91263a54bd">IAudioSessionNotification</a>
 

 

