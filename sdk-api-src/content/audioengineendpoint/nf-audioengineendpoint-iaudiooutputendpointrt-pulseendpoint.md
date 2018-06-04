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

# IAudioOutputEndpointRT::PulseEndpoint


## -description



        The <b>PulseEndpoint</b> method is  reserved.

This method is called by the audio engine at the end of a processing pass. The event handle is set by calling the <a href="https://msdn.microsoft.com/9f0f216a-d785-42e9-b07d-f1f2568b5833">IAudioEndpoint::SetEventHandle</a> method.


## -parameters






## -returns



This method does not return a value.




## -remarks



This method can be called from a real-time processing thread. The
    implementation of this method must not block, access paged memory, or call any blocking system routines.

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.




## -see-also




<a href="https://msdn.microsoft.com/b881b2f9-ffe9-46ff-94aa-eef0af172a3e">IAudioOutputEndpointRT</a>
 

 

