---
UID: NF:evntrace.GetTraceEnableLevel
title: GetTraceEnableLevel function
author: windows-sdk-content
description: The GetTraceEnableLevel function retrieves the severity level passed by the controller to indicate the level of logging the provider should perform. Providers can only call this function from their ControlCallback function.
old-location: etw\gettraceenablelevel.htm
tech.root: etw
ms.assetid: 22326fd9-c428-4430-8a92-978d005f6705
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetTraceEnableLevel, GetTraceEnableLevel function [ETW], _evt_gettraceenablelevel, base.gettraceenablelevel, etw.gettraceenablelevel, evntrace/GetTraceEnableLevel
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
 - GetTraceEnableLevel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetTraceEnableLevel
: 
---

# GetTraceEnableLevel function


## -description


The 
<b>GetTraceEnableLevel</b> function retrieves the severity level passed by the controller to indicate the level of logging the provider should perform.
			

Providers can only call this function from their 
<a href="https://msdn.microsoft.com/e9f70ae6-906f-4e55-bca7-4355f1ca6091">ControlCallback</a> function.


## -parameters




### -param TraceHandle

TBD




#### - SessionHandle [in]

Handle to an event tracing session, obtained by calling the 
<a href="https://msdn.microsoft.com/050d3a01-0087-40f1-af35-b9ceeaf47813">GetTraceLoggerHandle</a> function.


## -returns



Returns the value the controller specified in the <i>EnableLevel</i> parameter when calling the 
<a href="https://msdn.microsoft.com/d75f18e1-e5fa-4039-bb74-76dea334b0fd">EnableTrace</a> function. 
						

To determine if the function failed or the controller set the enable flags to 0, follow these steps:<ul>
<li>Call the <a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> function to set the last error to <b>ERROR_SUCCESS</b>.</li>
<li>Call the <b>GetTraceEnableLevel</b> function to retrieve the enable level.</li>
<li>If the enable level value is 0, call the 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function to retrieve the last known error.</li>
<li>If the last known error is <b>ERROR_SUCCESS</b>, the controller set the enable level to 0; otherwise, the <b>GetTraceEnableLevel</b> function failed with the last known error. </li>
</ul>





## -remarks



Providers use this value to control the severity of events that it generates. For example, providers can use this value to determine if it should generate informational, warning, or error events.


#### Examples

For an example that uses 
<b>GetTraceEnableLevel</b>, see 
<a href="https://msdn.microsoft.com/13512236-c416-43ba-bf36-b05c5c08d6c9">Retrieving Event Data Using MOF</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/e5c0f2bf-34da-4555-9556-4c79ee9a73ab">GetTraceEnableFlags</a>



<a href="https://msdn.microsoft.com/050d3a01-0087-40f1-af35-b9ceeaf47813">GetTraceLoggerHandle</a>
 

 

