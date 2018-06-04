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

# MI_DestinationOptions_AddDestinationCredentials function


## -description


Sets the credentials for talking to the destination.


## -parameters




### -param options [in, out]

A pointer to a <a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a> structure that contains the destination options.


### -param credentials [in]

A pointer to a <a href="https://msdn.microsoft.com/30191cd1-00de-42ef-ac95-5e174d273c80">MI_UserCredentials</a> structure that contains the credentials used when communicating with the destination machine.


## -returns



This function returns MI_INLINE MI_Result.




## -remarks



The credentials supported will vary depending on the destination, the protocol and the transport.  If dual-factor authentication is required this method can be called twice.  The default credentials will vary depending on the protocol and transport selected.



