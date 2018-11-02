---
UID: NF:winevt.EvtSubscribe
title: EvtSubscribe function
author: windows-sdk-content
description: Creates a subscription that will receive current and future events from a channel or log file that match the specified query criteria.
old-location: wes\evtsubscribe.htm
tech.root: wes
ms.assetid: e7c4c5f9-2a5a-4004-8f19-13eb61c4346b
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: EvtSubscribe, EvtSubscribe function [EventLog], wes.evtsubscribe, winevt/EvtSubscribe
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wevtapi.dll
 - Ext-MS-Win-WEvtAPI-EventLog-L1-1-0.dll
 - Ext-MS-Win-WEvtAPI-EventLog-L1-1-1.dll
 - Ext-MS-Win-WEvtAPI-EventLog-L1-1-2.dll
api_name:
 - EvtSubscribe
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EvtSubscribe function


## -description


Creates a subscription that will receive current and future events from a channel or log file that match the specified query criteria.


## -parameters




### -param Session [in]

A remote session handle that the <a href="https://msdn.microsoft.com/26f1745c-dcca-4452-872e-1fffe20f049c">EvtOpenSession</a> function returns. Set to <b>NULL</b> to subscribe to events on the local computer.


### -param SignalEvent [in]

The handle to an event object that the service will signal when new events are available that match your query criteria.  This parameter must be <b>NULL</b> if the <i>Callback</i> parameter is not <b>NULL</b>.


### -param ChannelPath [in]

The name of the Admin or Operational channel that contains the events that you want to subscribe to (you cannot subscribe to Analytic or Debug channels). The path is required if the <i>Query</i> parameter contains an XPath query; the path is ignored if the <i>Query</i> parameter contains a structured XML query.


### -param Query [in]

A query that specifies the types of events that you want the subscription service to return. You can specify an XPath 1.0 query or structured XML query. If your XPath contains more than 20 expressions, use a structured XML query. To receive all events, set this parameter to <b>NULL</b> or "*".


### -param Bookmark [in]

A handle to a bookmark that identifies the starting point for the subscription.  To get a bookmark handle, call the <a href="https://msdn.microsoft.com/1020d923-090b-48fc-96c2-394db5cd241e">EvtCreateBookmark</a> function.  You must set this parameter if the <i>Flags</i> parameter contains the EvtSubscribeStartAfterBookmark flag; otherwise, <b>NULL</b>.


### -param Context [in]

A caller-defined context value that the subscription service will pass to the specified callback each time it delivers an event.


### -param Callback [in]

Pointer to your <a href="https://msdn.microsoft.com/935a787c-fd71-492d-a803-80cb2c9019ea">EVT_SUBSCRIBE_CALLBACK</a> callback function that will receive the subscription events. This parameter must be <b>NULL</b> if the <i>SignalEvent</i> parameter is not <b>NULL</b>.


### -param Flags [in]

One or more flags that specify when to start subscribing to events. For example, if you specify EvtSubscribeStartAtOldestRecord, the service will retrieve all current and future events that match your query criteria; however, if you specify EvtSubscribeToFutureEvents, the service returns only future events that match your query criteria. For possible values, see the <a href="https://msdn.microsoft.com/2e0d5442-c9ac-4165-96ae-6f4122a5ce0a">EVT_SUBSCRIBE_FLAGS</a> enumeration.


## -returns



A handle to the subscription if successful; otherwise, <b>NULL</b>. If the function returns <b>NULL</b>, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function to get the error code. You must call the <a href="https://msdn.microsoft.com/c4b82d7b-508d-45bf-b990-04e90e846525">EvtClose</a> function with the subscription handle when done.




## -remarks



 To cancel the subscription, pass the returned subscription handle to the <a href="https://msdn.microsoft.com/c4b82d7b-508d-45bf-b990-04e90e846525">EvtClose</a> function.

There are two subscription models: the poll model and the push model. In the push model, you implement a subscription callback and set the <i>Callback</i> parameter to your implementation. The service will call your callback for each event that matches your query criteria (or if an error occurs).

In the poll model, you create an event object that the service signals. When signaled, you call the <a href="https://msdn.microsoft.com/46d40734-f022-4775-aa4f-13f4069c43c8">EvtNext</a> function using the subscription handle to enumerate the events. You must call the <a href="https://msdn.microsoft.com/c4b82d7b-508d-45bf-b990-04e90e846525">EvtClose</a> function on each event that you enumerate. You then reset the object and wait for the service to signal again. This process repeats until you cancel the subscription.


#### Examples

For an example that shows how to use this function, see <a href="https://msdn.microsoft.com/1e86deeb-fc59-4658-9353-e4ced7ace89a">Subscribing to Events</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/935a787c-fd71-492d-a803-80cb2c9019ea">EVT_SUBSCRIBE_CALLBACK</a>



<a href="https://msdn.microsoft.com/06b67ec4-74ab-47d7-b7b9-1180e7dee725">EvtQuery</a>
 

 

