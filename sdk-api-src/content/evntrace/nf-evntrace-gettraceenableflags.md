---
UID: NF:evntrace.GetTraceEnableFlags
title: GetTraceEnableFlags function (evntrace.h)
description: The GetTraceEnableFlags function retrieves the enable flags passed by the controller to indicate which category of events to trace.Providers can only call this function from their ControlCallback function.
helpviewer_keywords: ["GetTraceEnableFlags","GetTraceEnableFlags function [ETW]","_evt_gettraceenableflags","base.gettraceenableflags","etw.gettraceenableflags","evntrace/GetTraceEnableFlags"]
old-location: etw\gettraceenableflags.htm
tech.root: ETW
ms.assetid: e5c0f2bf-34da-4555-9556-4c79ee9a73ab
ms.date: 12/05/2018
ms.keywords: GetTraceEnableFlags, GetTraceEnableFlags function [ETW], _evt_gettraceenableflags, base.gettraceenableflags, etw.gettraceenableflags, evntrace/GetTraceEnableFlags
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetTraceEnableFlags
 - evntrace/GetTraceEnableFlags
dev_langs:
 - c++
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
---

# GetTraceEnableFlags function


## -description

The 
<b>GetTraceEnableFlags</b> function retrieves the enable flags passed by the controller to indicate which category of events to trace.

Providers can only call this function from their 
<a href="https://docs.microsoft.com/windows/desktop/ETW/controlcallback">ControlCallback</a> function.

## -parameters

### -param TraceHandle [in]

Handle to an event tracing session, obtained by calling the 
<a href="https://docs.microsoft.com/windows/desktop/ETW/gettraceloggerhandle">GetTraceLoggerHandle</a> function.

## -returns

Returns the value the controller specified in the <i>EnableFlag</i> parameter when calling the 
<a href="https://docs.microsoft.com/windows/desktop/ETW/enabletrace">EnableTrace</a> function.
						

To determine if the function failed or the controller set the enable flags to 0, follow these steps:<ul>
<li>Call the <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> function to set the last error to <b>ERROR_SUCCESS</b>.</li>
<li>Call the <b>GetTraceEnableFlags</b> function to retrieve the enable flags.</li>
<li>If the enable flags value is 0, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function to retrieve the last known error.</li>
<li>If the last known error is <b>ERROR_SUCCESS</b>, the controller set the enable flags to 0; otherwise, the <b>GetTraceEnableFlags</b> function failed with the last known error. </li>
</ul>

## -remarks

Providers can use this value to control which events that it generates. For example, a provider can group events into logical categories of events and use this value to enable or disable their generation.


#### Examples

For an example that uses 
<b>GetTraceEnableFlags</b>, see 
<a href="https://docs.microsoft.com/windows/desktop/ETW/retrieving-event-data-using-mof">Retrieving Event Data Using MOF</a>.

<div class="code"></div>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/ETW/gettraceenablelevel">GetTraceEnableLevel</a>



<a href="https://docs.microsoft.com/windows/desktop/ETW/gettraceloggerhandle">GetTraceLoggerHandle</a>

