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

# _WTS_PROTOCOL_STATUS structure


## -description


Contains information about the status of the protocol.


## -struct-fields




### -field Output

A <a href="https://msdn.microsoft.com/118c5e12-5436-4c0a-a31d-a60c5123e384">WTS_PROTOCOL_COUNTERS</a> structure that contains the output protocol counters.


### -field Input

A <a href="https://msdn.microsoft.com/118c5e12-5436-4c0a-a31d-a60c5123e384">WTS_PROTOCOL_COUNTERS</a> structure that contains the input protocol counters.


### -field Cache

A <a href="https://msdn.microsoft.com/3c29596f-77c6-415b-bf97-529f70b9d9fe">WTS_CACHE_STATS</a> structure that contains protocol cache statistics.


### -field AsyncSignal

An integer that identifies an asynchronous signal for asynchronous protocols.


### -field AsyncSignalMask

An asynchronous signal mask.


### -field Counters

An array of up to 100 counters.


## -remarks



This structure is used by the <a href="https://msdn.microsoft.com/d224877a-649a-4ac2-a5e7-831592e6a0d9">GetProtocolStatus</a> method.



