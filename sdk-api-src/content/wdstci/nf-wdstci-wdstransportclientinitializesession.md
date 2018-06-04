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

# WdsTransportClientInitializeSession function


## -description


Initiates a multicast file transfer.


## -parameters




### -param pSessionRequest [in]

Pointer to a <a href="https://msdn.microsoft.com/efa1ea12-5234-474b-a859-cd074290e375">WDS_TRANSPORTCLIENT_REQUEST</a> structure that contains all the details required to initiate the multicast session.  The format of this structure is described below.


### -param pCallerData [in]

User supplied pointer that will be provided with every callback for this session.


### -param hSessionKey [out]

Buffer that will receive the address of a handle that the consumer can use to uniquely identify this session to the client.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.




## -remarks



This function only sets up the session, it does not start the transfer.  To start the transfer, call <a href="https://msdn.microsoft.com/aa89899f-8f50-4617-84a1-4013412f0292">WdsTransportClientStartSession</a>.



