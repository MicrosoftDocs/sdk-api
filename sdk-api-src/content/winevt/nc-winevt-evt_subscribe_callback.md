---
UID: NC:winevt.EVT_SUBSCRIBE_CALLBACK
title: EVT_SUBSCRIBE_CALLBACK
author: windows-sdk-content
description: Implement this callback if you call the EvtSubscribe function to receive events that match your query.
old-location: wes\evt_subscribe_callback.htm
tech.root: wes
ms.assetid: 935a787c-fd71-492d-a803-80cb2c9019ea
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: EVT_SUBSCRIBE_CALLBACK, EVT_SUBSCRIBE_CALLBACK callback, EVT_SUBSCRIBE_CALLBACK callback function [EventLog], wes.evt_subscribe_callback, winevt/EVT_SUBSCRIBE_CALLBACK
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
 - UserDefined
api_location:
 - WinEvt.h
api_name:
 - EVT_SUBSCRIBE_CALLBACK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EVT_SUBSCRIBE_CALLBACK callback function


## -description


Implement this callback if you call the <a href="https://msdn.microsoft.com/e7c4c5f9-2a5a-4004-8f19-13eb61c4346b">EvtSubscribe</a> function to receive events that match your query. The service calls your callback when events that match your query criteria are raised.


## -parameters




### -param Action

Determines whether the <i>Event</i> parameter contains an event or an error code. For possible notify action values, see the <a href="https://msdn.microsoft.com/75166c22-c55c-41b4-8089-ff9a89ddebf5">EVT_SUBSCRIBE_NOTIFY_ACTION</a> enumeration.


### -param UserContext

The context that the subscriber passed to the <a href="https://msdn.microsoft.com/e7c4c5f9-2a5a-4004-8f19-13eb61c4346b">EvtSubscribe</a> function.


### -param Event

A handle to the event. The event handle is only valid for the duration of the callback function.  You can use this handle with any event log function that takes an event handle (for example, <a href="https://msdn.microsoft.com/521322b6-3424-4321-bcba-fa8dcdc05a76">EvtRender</a> or <a href="https://msdn.microsoft.com/744fe166-b12c-49d4-ab13-b2ef6a6f9625">EvtFormatMessage</a>). 

Do not call <a href="https://msdn.microsoft.com/c4b82d7b-508d-45bf-b990-04e90e846525">EvtClose</a> to close this handle; the service will close the handle when the callback returns.

If the <i>Action</i> parameter is EvtSubscribeActionError, cast <i>Event</i> to a DWORD to access the Win32 error code.


## -returns



The service ignores the return code that you return.




## -remarks



This callback will block other events from being delivered to your callback, so keep your implementation as short as possible.

If the service encounters an error while setting up the subscription, your callback will not receive any notification that an error occurred.

If the <i>Flags</i> parameter of <a href="https://msdn.microsoft.com/e7c4c5f9-2a5a-4004-8f19-13eb61c4346b">EvtSubscribe</a> includes EvtSubscribeStrict, your callback will receive notification when event records are missing. In this case, the value of <i>Event</i> will be ERROR_EVT_QUERY_RESULT_STALE.

To cancel the subscription, you must close the subscription handle that the <a href="https://msdn.microsoft.com/e7c4c5f9-2a5a-4004-8f19-13eb61c4346b">EvtSubscribe</a> function returns.


#### Examples

For an example that implements <b>EVT_SUBSCRIBE_CALLBACK</b> callback function, see <a href="https://msdn.microsoft.com/1e86deeb-fc59-4658-9353-e4ced7ace89a">Subscribing to Events</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/e7c4c5f9-2a5a-4004-8f19-13eb61c4346b">EvtSubscribe</a>
 

 

