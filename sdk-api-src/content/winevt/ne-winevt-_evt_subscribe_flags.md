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

# _EVT_SUBSCRIBE_FLAGS enumeration


## -description


Defines the possible values that specify when to start subscribing to events.


## -enum-fields




### -field EvtSubscribeToFutureEvents

Subscribe to only future events that match the query criteria.


### -field EvtSubscribeStartAtOldestRecord

Subscribe to all existing and future events that match the query criteria.


### -field EvtSubscribeStartAfterBookmark

Subscribe to all existing and future events that match the query criteria that begin after the bookmarked event. If you include the EvtSubscribeStrict flag, the <a href="https://msdn.microsoft.com/e7c4c5f9-2a5a-4004-8f19-13eb61c4346b">EvtSubscribe</a> function fails if the bookmarked event does not exist. If you do not include the EvtSubscribeStrict flag and the bookmarked event does not exist, the subscription begins with the event that is after the event that is closest to the bookmarked event.


### -field EvtSubscribeOriginMask

A bitmask that you can use to determine which of the following flags is set:

<ul>
<li>EvtSubscribeToFutureEvents</li>
<li>EvtSubscribeStartAtOldestRecord</li>
<li>EvtSubscribeStartAfterBookmark</li>
</ul>

### -field EvtSubscribeTolerateQueryErrors

Complete the subscription even if the part of the query generates an error (is not well formed). The service validates the syntax of the XPath query to determine if it is well formed. If the validation fails, the service parses the XPath into individual expressions. It builds a new XPath beginning with the left most expression. The service validates the expression and if it is valid, the service adds the next expression to the XPath. The service repeats this process until it finds the expression that is failing. It then uses the valid expressions that it found beginning with the leftmost expression as the XPath query (which means that you may not get the events that you expected). If no part of the XPath is valid, the <a href="https://msdn.microsoft.com/e7c4c5f9-2a5a-4004-8f19-13eb61c4346b">EvtSubscribe</a> call fails.


### -field EvtSubscribeStrict

Forces the <a href="https://msdn.microsoft.com/e7c4c5f9-2a5a-4004-8f19-13eb61c4346b">EvtSubscribe</a> call to fail if you specify EvtSubscribeStartAfterBookmark and the bookmarked event is not found (the return value is ERROR_NOT_FOUND). Also, set this flag if you want to receive notification in your callback when event records are missing.


## -remarks



The EvtSubscribeToFutureEvents, EvtSubscribeStartAtOldestRecord, and EvtSubscribeStartAfterBookmark flags are mutually exclusive.




## -see-also




<a href="https://msdn.microsoft.com/e7c4c5f9-2a5a-4004-8f19-13eb61c4346b">EvtSubscribe</a>
 

 

