---
UID: NE:winevt._EVT_SUBSCRIBE_FLAGS
title: "_EVT_SUBSCRIBE_FLAGS"
author: windows-sdk-content
description: Defines the possible values that specify when to start subscribing to events.
old-location: wes\evt_subscribe_flags.htm
tech.root: WES
ms.assetid: 2e0d5442-c9ac-4165-96ae-6f4122a5ce0a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: EVT_SUBSCRIBE_FLAGS, EVT_SUBSCRIBE_FLAGS enumeration [EventLog], EvtSubscribeOriginMask, EvtSubscribeStartAfterBookmark, EvtSubscribeStartAtOldestRecord, EvtSubscribeStrict, EvtSubscribeToFutureEvents, EvtSubscribeTolerateQueryErrors, _EVT_SUBSCRIBE_FLAGS, wes.evt_subscribe_flags, winevt/EVT_SUBSCRIBE_FLAGS, winevt/EvtSubscribeOriginMask, winevt/EvtSubscribeStartAfterBookmark, winevt/EvtSubscribeStartAtOldestRecord, winevt/EvtSubscribeStrict, winevt/EvtSubscribeToFutureEvents, winevt/EvtSubscribeTolerateQueryErrors
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: winevt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinEvt.h
api_name:
 - EVT_SUBSCRIBE_FLAGS
product: Windows
targetos: Windows
req.typenames: EVT_SUBSCRIBE_FLAGS
req.redist: 
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
 

 

