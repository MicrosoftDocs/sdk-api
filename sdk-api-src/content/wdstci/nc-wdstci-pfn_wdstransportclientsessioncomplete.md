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

# PFN_WdsTransportClientSessionComplete callback function


## -description


The PFN_WdsTransportClientSessionCompete callback is used by the client to indicate that no more callbacks will be sent to the consumer and that the session either completed successfully or encountered a non-recoverable error.


## -parameters




### -param hSessionKey [in]

The handle belonging to the session that is being started.


### -param pCallerData [in]

Pointer to the caller specific data for this session.  This data was specified in the call to <a href="https://msdn.microsoft.com/aa89899f-8f50-4617-84a1-4013412f0292">WdsTransportClientStartSession</a> function.


### -param dwError [in]

The overall status of the file transfer.  If the session succeeded, this value will be set to <b>ERROR_SUCCESS</b>.  If the session did not succeed, the error code for the session will be set.


## -returns



This callback function does not return a value.




## -remarks



This will be the last callback a consumer receives.  The consumer will always receive this callback, even if the session is canceled.  



