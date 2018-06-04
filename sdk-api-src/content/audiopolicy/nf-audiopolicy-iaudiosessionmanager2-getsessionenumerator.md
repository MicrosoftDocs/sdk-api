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

# IAudioSessionManager2::GetSessionEnumerator


## -description


The <b>GetSessionEnumerator</b> method gets a pointer to the audio session enumerator object.


## -parameters




### -param SessionEnum






#### - SessionList [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/a7976d13-3391-4747-b83a-cfb9407b34f2">IAudioSessionEnumerator</a> interface of the session enumerator object that the client can use to enumerate audio sessions on the audio device. Through this method, the caller obtains a counted reference to the interface. The caller is responsible for releasing the interface, when it is no longer needed, by calling the interface's <b>Release</b> method. 


## -returns



If the method succeeds, it returns S_OK.




## -remarks



The session manager maintains a collection of audio sessions that are active on the audio device by querying the audio engine.  <b>GetSessionEnumerator</b>  creates a session control for each session in the collection. To get a reference to the <a href="https://msdn.microsoft.com/4446140e-2e61-40ed-b0f9-4c1b90e7c2de">IAudioSessionControl</a> interface of the session in the enumerated collection, the application must call <a href="https://msdn.microsoft.com/1854e7fe-9d5f-42f3-9c4c-f2a27f26ac17">IAudioSessionEnumerator::GetSession</a>. For a code example, see <a href="https://msdn.microsoft.com/a7976d13-3391-4747-b83a-cfb9407b34f2">IAudioSessionEnumerator Interface</a>.

The session enumerator might not be aware of the new sessions that are reported through <a href="https://msdn.microsoft.com/69222168-87d7-4f5a-93b1-6d91263a54bd">IAudioSessionNotification</a>. So if an application exclusively relies on the session enumerator for getting all the sessions for an audio endpoint, the results might not be accurate. To work around this, the application should manually maintain a list. For more information, see <a href="https://msdn.microsoft.com/a7976d13-3391-4747-b83a-cfb9407b34f2">IAudioSessionEnumerator</a>.




## -see-also




<a href="https://msdn.microsoft.com/476dac90-d0c4-499c-973e-33ea55546659">IAudioSessionManager2</a>
 

 

