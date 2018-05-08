---
UID: NC:evntrace.PEVENT_RECORD_CALLBACK
title: PEVENT_RECORD_CALLBACK
author: windows-driver-content
description: Consumers implement this callback to receive events from a session. The PEVENT_RECORD_CALLBACK type defines a pointer to this callback function. EventRecordCallback is a placeholder for the application-defined function name.
old-location: etw\eventrecordcallback.htm
old-project: ETW
ms.assetid: 80a30faf-af1f-4440-8a17-9df44bdb2291
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: EventRecordCallback, EventRecordCallback callback function [ETW], PEVENT_RECORD_CALLBACK, PEVENT_RECORD_CALLBACK callback, etw.eventrecordcallback, evntrace/EventRecordCallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: evntrace.h
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
req.typenames: EVENT_FILTER_LEVEL_KW, *PEVENT_FILTER_LEVEL_KW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Evntrace.h
api_name:
-	EventRecordCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# PEVENT_RECORD_CALLBACK callback function


## -description



			Consumers implement this callback to receive events from a session. 

The <b>PEVENT_RECORD_CALLBACK</b> type defines a pointer to this callback function. <b>EventRecordCallback</b> is a placeholder for the application-defined function name.


## -parameters




### -param EventRecord [in]

Pointer to an 
<a href="https://msdn.microsoft.com/e352c1a7-39a2-43e3-a723-5fc6a3921ee8">EVENT_RECORD</a> structure that contains the event information.


## -returns




						The function does not return a value.
					




## -remarks



To specify the function that ETW calls to deliver events, set the 
<b>EventRecordCallback</b> member of the 
<a href="https://msdn.microsoft.com/179451e9-7e3c-4d3a-bcc6-3ad9d382229a">EVENT_TRACE_LOGFILE</a> structure (you pass this structure to the 
<a href="https://msdn.microsoft.com/505e643b-6b4f-4f93-96c8-7fe8abdd6234">OpenTrace</a> function). You must also set the <b>ProcessTraceMode</b> member to PROCESS_TRACE_MODE_EVENT_RECORD.

This callback receives all events that the session generates from the time you call the 
<a href="https://msdn.microsoft.com/505e643b-6b4f-4f93-96c8-7fe8abdd6234">OpenTrace</a> function. Call the <a href="https://msdn.microsoft.com/aea25a95-f435-4068-9b15-7473f31ebf16">ProcessTrace</a> function to begin receiving the events.

For information on parsing the event data, see <a href="https://msdn.microsoft.com/8164b963-6232-42aa-b15e-071ac389dd27">Retrieving Event Data Using TDH</a>. 




## -see-also




<a href="https://msdn.microsoft.com/0cfe2f62-63dc-45a6-96ce-fb4bf458358f">BufferCallback</a>



<a href="https://msdn.microsoft.com/179451e9-7e3c-4d3a-bcc6-3ad9d382229a">EVENT_TRACE_LOGFILE</a>



<a href="https://msdn.microsoft.com/aea25a95-f435-4068-9b15-7473f31ebf16">ProcessTrace</a>
 

 

