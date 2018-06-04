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

# IAudioEndpointRT::SetPinInactive


## -description



        The <b>SetPinInactive</b> method     notifies the endpoint that it must change the state of the underlying stream resources to an inactive state.


## -parameters






## -returns



If the method succeeds, it returns <b>S_OK</b>.




## -remarks



This method enables the audio engine to call into the endpoint to indicate that the endpoint can pause the underlying stream resources.  In most cases, this method can simply return <b>S_OK</b>.

This method can be called from a real-time processing thread. The
    implementation of this method must not block, access
    paged memory, or call any blocking system routines.

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.




## -see-also




<a href="https://msdn.microsoft.com/3fb05ce4-a3be-4c84-8e03-71213f453f74">IAudioEndpointRT</a>
 

 

