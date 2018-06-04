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

# PowerSettingUnregisterNotification function


## -description


Cancels a registration to receive notification when a power setting changes.


## -parameters




### -param RegistrationHandle [in, out]

A handle to a registration obtained by calling the <a href="https://msdn.microsoft.com/0fbca717-2367-4407-8094-3eb2b717b59c">PowerSettingRegisterNotification</a> function.


## -returns



Returns ERROR_SUCCESS (zero) if the call was successful, and a nonzero value if the call failed.




## -see-also




<a href="https://msdn.microsoft.com/0fbca717-2367-4407-8094-3eb2b717b59c">PowerSettingRegisterNotification</a>
 

 

