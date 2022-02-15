---
UID: NE:winevt._EVT_SUBSCRIBE_FLAGS
title: EVT_SUBSCRIBE_FLAGS (winevt.h)
description: Defines the possible values that specify when to start subscribing to events.
helpviewer_keywords: ["EVT_SUBSCRIBE_FLAGS","EVT_SUBSCRIBE_FLAGS enumeration [EventLog]","EvtSubscribeOriginMask","EvtSubscribeStartAfterBookmark","EvtSubscribeStartAtOldestRecord","EvtSubscribeStrict","EvtSubscribeToFutureEvents","EvtSubscribeTolerateQueryErrors","wes.evt_subscribe_flags","winevt/EVT_SUBSCRIBE_FLAGS","winevt/EvtSubscribeOriginMask","winevt/EvtSubscribeStartAfterBookmark","winevt/EvtSubscribeStartAtOldestRecord","winevt/EvtSubscribeStrict","winevt/EvtSubscribeToFutureEvents","winevt/EvtSubscribeTolerateQueryErrors"]
old-location: wes\evt_subscribe_flags.htm
tech.root: wes
ms.assetid: 2e0d5442-c9ac-4165-96ae-6f4122a5ce0a
ms.date: 12/05/2018
ms.keywords: EVT_SUBSCRIBE_FLAGS, EVT_SUBSCRIBE_FLAGS enumeration [EventLog], EvtSubscribeOriginMask, EvtSubscribeStartAfterBookmark, EvtSubscribeStartAtOldestRecord, EvtSubscribeStrict, EvtSubscribeToFutureEvents, EvtSubscribeTolerateQueryErrors, wes.evt_subscribe_flags, winevt/EVT_SUBSCRIBE_FLAGS, winevt/EvtSubscribeOriginMask, winevt/EvtSubscribeStartAfterBookmark, winevt/EvtSubscribeStartAtOldestRecord, winevt/EvtSubscribeStrict, winevt/EvtSubscribeToFutureEvents, winevt/EvtSubscribeTolerateQueryErrors
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
targetos: Windows
req.typenames: EVT_SUBSCRIBE_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EVT_SUBSCRIBE_FLAGS
 - winevt/_EVT_SUBSCRIBE_FLAGS
 - EVT_SUBSCRIBE_FLAGS
 - winevt/EVT_SUBSCRIBE_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinEvt.h
api_name:
 - EVT_SUBSCRIBE_FLAGS
---

# EVT_SUBSCRIBE_FLAGS enumeration


## -description

Defines the possible values that specify when to start subscribing to events.

## -enum-fields

### -field EvtSubscribeToFutureEvents:1

Subscribe to only future events that match the query criteria.

### -field EvtSubscribeStartAtOldestRecord:2

Subscribe to all existing and future events that match the query criteria.

### -field EvtSubscribeStartAfterBookmark:3

Subscribe to all existing and future events that match the query criteria that begin after the bookmarked event. If you include the EvtSubscribeStrict flag, the <a href="/windows/desktop/api/winevt/nf-winevt-evtsubscribe">EvtSubscribe</a> function fails if the bookmarked event does not exist. If you do not include the EvtSubscribeStrict flag and the bookmarked event does not exist, the subscription begins with the event that is after the event that is closest to the bookmarked event.

### -field EvtSubscribeOriginMask:3

A bitmask that you can use to determine which of the following flags is set:

<ul>
<li>EvtSubscribeToFutureEvents</li>
<li>EvtSubscribeStartAtOldestRecord</li>
<li>EvtSubscribeStartAfterBookmark</li>
</ul>

### -field EvtSubscribeTolerateQueryErrors:0x1000

Complete the subscription even if the part of the query generates an error (is not well formed). The service validates the syntax of the XPath query to determine if it is well formed. If the validation fails, the service parses the XPath into individual expressions. It builds a new XPath beginning with the left most expression. The service validates the expression and if it is valid, the service adds the next expression to the XPath. The service repeats this process until it finds the expression that is failing. It then uses the valid expressions that it found beginning with the leftmost expression as the XPath query (which means that you may not get the events that you expected). If no part of the XPath is valid, the <a href="/windows/desktop/api/winevt/nf-winevt-evtsubscribe">EvtSubscribe</a> call fails.

### -field EvtSubscribeStrict:0x10000

Forces the <a href="/windows/desktop/api/winevt/nf-winevt-evtsubscribe">EvtSubscribe</a> call to fail if you specify EvtSubscribeStartAfterBookmark and the bookmarked event is not found (the return value is ERROR_NOT_FOUND). Also, set this flag if you want to receive notification in your callback when event records are missing.

## -remarks

The EvtSubscribeToFutureEvents, EvtSubscribeStartAtOldestRecord, and EvtSubscribeStartAfterBookmark flags are mutually exclusive.

## -see-also

<a href="/windows/desktop/api/winevt/nf-winevt-evtsubscribe">EvtSubscribe</a>
