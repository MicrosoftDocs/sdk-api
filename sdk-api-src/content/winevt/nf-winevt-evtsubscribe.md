---
UID: NF:winevt.EvtSubscribe
title: EvtSubscribe function (winevt.h)
description: Creates a subscription that will receive current and future events from a channel or log file that match the specified query criteria.
helpviewer_keywords: ["EvtSubscribe","EvtSubscribe function [EventLog]","wes.evtsubscribe","winevt/EvtSubscribe"]
old-location: wes\evtsubscribe.htm
tech.root: wes
ms.assetid: e7c4c5f9-2a5a-4004-8f19-13eb61c4346b
ms.date: 12/05/2018
ms.keywords: EvtSubscribe, EvtSubscribe function [EventLog], wes.evtsubscribe, winevt/EvtSubscribe
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
req.lib: Wevtapi.lib
req.dll: Wevtapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EvtSubscribe
 - winevt/EvtSubscribe
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-wevtapi-eventlog-l1-1-3.dll
 - Wevtapi.dll
 - Ext-MS-Win-WEvtAPI-EventLog-L1-1-0.dll
 - Ext-MS-Win-WEvtAPI-EventLog-L1-1-1.dll
 - Ext-MS-Win-WEvtAPI-EventLog-L1-1-2.dll
api_name:
 - EvtSubscribe
---

# EvtSubscribe function


## -description

Creates a subscription that will receive current and future events from a channel or log file that match the specified query criteria.

## -parameters

### -param Session [in]

A remote session handle that the <a href="/windows/desktop/api/winevt/nf-winevt-evtopensession">EvtOpenSession</a> function returns. Set to <b>NULL</b> to subscribe to events on the local computer.

### -param SignalEvent [in]

The handle to an event object that the service will signal when new events are available that match your query criteria.  This parameter must be <b>NULL</b> if the <i>Callback</i> parameter is not <b>NULL</b>.

### -param ChannelPath [in]

The name of the Admin or Operational channel that contains the events that you want to subscribe to (you cannot subscribe to Analytic or Debug channels). The path is required if the <i>Query</i> parameter contains an XPath query; the path is ignored if the <i>Query</i> parameter contains a structured XML query.

### -param Query [in]

A query that specifies the types of events that you want the subscription service to return. You can specify an XPath 1.0 query or structured XML query. If your XPath contains more than 20 expressions, use a structured XML query. To receive all events, set this parameter to <b>NULL</b> or "*".

### -param Bookmark [in]

A handle to a bookmark that identifies the starting point for the subscription.  To get a bookmark handle, call the <a href="/windows/desktop/api/winevt/nf-winevt-evtcreatebookmark">EvtCreateBookmark</a> function.  You must set this parameter if the <i>Flags</i> parameter contains the EvtSubscribeStartAfterBookmark flag; otherwise, <b>NULL</b>.

### -param Context [in]

A caller-defined context value that the subscription service will pass to the specified callback each time it delivers an event.

### -param Callback [in]

Pointer to your <a href="/windows/desktop/api/winevt/nc-winevt-evt_subscribe_callback">EVT_SUBSCRIBE_CALLBACK</a> callback function that will receive the subscription events. This parameter must be <b>NULL</b> if the <i>SignalEvent</i> parameter is not <b>NULL</b>.

### -param Flags [in]

One or more flags that specify when to start subscribing to events. For example, if you specify EvtSubscribeStartAtOldestRecord, the service will retrieve all current and future events that match your query criteria; however, if you specify EvtSubscribeToFutureEvents, the service returns only future events that match your query criteria. For possible values, see the <a href="/windows/desktop/api/winevt/ne-winevt-evt_subscribe_flags">EVT_SUBSCRIBE_FLAGS</a> enumeration.

## -returns

A handle to the subscription if successful; otherwise, <b>NULL</b>. If the function returns <b>NULL</b>, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function to get the error code. You must call the <a href="/windows/desktop/api/winevt/nf-winevt-evtclose">EvtClose</a> function with the subscription handle when done.

## -remarks

 To cancel the subscription, pass the returned subscription handle to the <a href="/windows/desktop/api/winevt/nf-winevt-evtclose">EvtClose</a> function.

There are two subscription models: the poll model and the push model. In the push model, you implement a subscription callback and set the <i>Callback</i> parameter to your implementation. The service will call your callback for each event that matches your query criteria (or if an error occurs).

In the poll model, you create an event object that the service signals. When signaled, you call the <a href="/windows/desktop/api/winevt/nf-winevt-evtnext">EvtNext</a> function using the subscription handle to enumerate the events. You must call the <a href="/windows/desktop/api/winevt/nf-winevt-evtclose">EvtClose</a> function on each event that you enumerate. You then reset the object and wait for the service to signal again. This process repeats until you cancel the subscription.


#### Examples

For an example that shows how to use this function, see <a href="/windows/desktop/WES/subscribing-to-events">Subscribing to Events</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winevt/nc-winevt-evt_subscribe_callback">EVT_SUBSCRIBE_CALLBACK</a>



<a href="/windows/desktop/api/winevt/nf-winevt-evtquery">EvtQuery</a>