---
UID: NF:evntrace.GetTraceEnableFlags
title: GetTraceEnableFlags function
author: windows-sdk-content
description: The GetTraceEnableFlags function retrieves the enable flags passed by the controller to indicate which category of events to trace.Providers can only call this function from their ControlCallback function.
old-location: etw\gettraceenableflags.htm
tech.root: etw
ms.assetid: e5c0f2bf-34da-4555-9556-4c79ee9a73ab
ms.author: windowssdkdev
ms.date: 08/08/2018
ms.keywords: GetTraceEnableFlags, GetTraceEnableFlags function [ETW], _evt_gettraceenableflags, base.gettraceenableflags, etw.gettraceenableflags, evntrace/GetTraceEnableFlags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: evntrace.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-eventing-classicprovider-l1-1-0.dll
api_name:
 - GetTraceEnableFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetTraceEnableFlags function


## -description


The 
<b>GetTraceEnableFlags</b> function retrieves the enable flags passed by the controller to indicate which category of events to trace.

Providers can only call this function from their 
<a href="https://msdn.microsoft.com/e9f70ae6-906f-4e55-bca7-4355f1ca6091">ControlCallback</a> function.


## -parameters




### -param TraceHandle

TBD




#### - SessionHandle [in]

Handle to an event tracing session, obtained by calling the 
<a href="https://msdn.microsoft.com/050d3a01-0087-40f1-af35-b9ceeaf47813">GetTraceLoggerHandle</a> function.


## -returns



Returns the value the controller specified in the <i>EnableFlag</i> parameter when calling the 
<a href="https://msdn.microsoft.com/d75f18e1-e5fa-4039-bb74-76dea334b0fd">EnableTrace</a> function.
						

To determine if the function failed or the controller set the enable flags to 0, follow these steps:<ul>
<li>Call the <a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> function to set the last error to <b>ERROR_SUCCESS</b>.</li>
<li>Call the <b>GetTraceEnableFlags</b> function to retrieve the enable flags.</li>
<li>If the enable flags value is 0, call the 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function to retrieve the last known error.</li>
<li>If the last known error is <b>ERROR_SUCCESS</b>, the controller set the enable flags to 0; otherwise, the <b>GetTraceEnableFlags</b> function failed with the last known error. </li>
</ul>





## -remarks



Providers can use this value to control which events that it generates. For example, a provider can group events into logical categories of events and use this value to enable or disable their generation.


#### Examples

For an example that uses 
<b>GetTraceEnableFlags</b>, see 
<a href="https://msdn.microsoft.com/13512236-c416-43ba-bf36-b05c5c08d6c9">Retrieving Event Data Using MOF</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/22326fd9-c428-4430-8a92-978d005f6705">GetTraceEnableLevel</a>



<a href="https://msdn.microsoft.com/050d3a01-0087-40f1-af35-b9ceeaf47813">GetTraceLoggerHandle</a>
 

 

