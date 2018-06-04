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

# OnDemandUnRegisterNotification function


## -description


The <b>OnDemandUnregisterNotification</b> function allows an application to unregister for notifications and clean up resources.


## -parameters




### -param registrationHandle

TBD




#### - RegistrationHandle [in]

A HANDLE obtained from a successful <a href="https://msdn.microsoft.com/1C9BB656-B1A7-49A6-97B9-414946BF9BE0">OnDemandRegisterNotification</a>  call.


## -returns



Returns S_OK on success.




## -see-also




<a href="https://msdn.microsoft.com/1C9BB656-B1A7-49A6-97B9-414946BF9BE0">OnDemandRegisterNotification</a>
 

 

