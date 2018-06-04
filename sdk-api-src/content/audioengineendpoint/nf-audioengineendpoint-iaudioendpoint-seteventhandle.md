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

# IAudioEndpoint::SetEventHandle


## -description


The <b>SetEventHandle</b> method sets the handle for the event that the endpoint uses to signal that it has completed processing of a buffer.


## -parameters




### -param eventHandle [in]

The event handle used to invoke a buffer completion
    callback.


## -returns



If the method succeeds, it returns <b>S_OK</b>. If it fails, possible return codes include, but are not limited to, the following.




## -remarks



The <b>SetEventHandle</b> method sets the audio engine event handle on the endpoint. In this implementation, the caller should receive an error response of <b>AEERR_NOT_INITIALIZED</b> if the audio endpoint is not initialized or the buffer is not set by the <a href="https://msdn.microsoft.com/library/windows/hardware/jj983423">SetBuffer</a> method.

To get event notifications, the audio engine will have  set the <b>AUDCLNT_STREAMFLAGS_EVENTCALLBACK</b> flag on the endpoint. To set this flag, the audio engine calls  the <a href="https://msdn.microsoft.com/f6713912-ba7e-4e3e-95d9-8318c40a7042">IAudioEndpoint::SetStreamFlags</a> method.

This method must not be called from a real-time processing thread.

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.




## -see-also




<a href="https://msdn.microsoft.com/a1bb3fe4-6051-4b9c-8270-70375e700f01">IAudioEndpoint</a>
 

 

