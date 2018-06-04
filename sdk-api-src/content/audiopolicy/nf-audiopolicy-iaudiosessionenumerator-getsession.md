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

# IAudioSessionEnumerator::GetSession


## -description


The <b>GetSession</b> method gets the audio session specified by an audio session number.


## -parameters




### -param SessionCount [in]

The session number. If there are <i>n</i> sessions, the sessions are numbered from 0 to <i>n</i> – 1. To get the number of sessions, call the <a href="https://msdn.microsoft.com/a1fbfbf5-a79b-40bc-97c7-a76a181bbfec">IAudioSessionEnumerator::GetCount</a> method.




### -param Session [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/4446140e-2e61-40ed-b0f9-4c1b90e7c2de">IAudioSessionControl</a> interface of the session object in the collection that is maintained by the session enumerator. The caller must release the interface pointer.


## -returns



If the method succeeds, it returns S_OK.




## -see-also




<a href="https://msdn.microsoft.com/a7976d13-3391-4747-b83a-cfb9407b34f2">IAudioSessionEnumerator</a>
 

 

