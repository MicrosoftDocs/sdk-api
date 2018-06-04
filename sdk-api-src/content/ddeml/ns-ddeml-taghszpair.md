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

# tagHSZPAIR structure


## -description


Contains a DDE service name and topic name. A DDE server application can use this structure during an <a href="https://msdn.microsoft.com/4651e14f-ca13-412e-853d-326a13db78e4">XTYP_WILDCONNECT</a> transaction to enumerate the service-topic pairs that it supports. 


## -struct-fields




### -field hszSvc

Type: <b>HSZ</b>

A handle to the service name. 


### -field hszTopic

Type: <b>HSZ</b>

A handle to the topic name. 


## -see-also




<a href="https://msdn.microsoft.com/0bcd8de4-a6f0-4f2a-8b9d-0b1b638925fb">About Dynamic Data Exchange</a>
 

 

