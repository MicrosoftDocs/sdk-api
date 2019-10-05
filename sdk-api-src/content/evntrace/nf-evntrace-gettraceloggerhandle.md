---
UID: NF:evntrace.GetTraceLoggerHandle
title: GetTraceLoggerHandle function (evntrace.h)
author: windows-sdk-content
description: The GetTraceLoggerHandle function retrieves the handle of the event tracing session. Providers can only call this function from their ControlCallback function.
old-location: etw\gettraceloggerhandle.htm
tech.root: ETW
ms.assetid: 050d3a01-0087-40f1-af35-b9ceeaf47813
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetTraceLoggerHandle, GetTraceLoggerHandle function [ETW], _evt_gettraceloggerhandle, base.gettraceloggerhandle, etw.gettraceloggerhandle, evntrace/GetTraceLoggerHandle
ms.topic: function
f1_keywords: 
 - "evntrace/GetTraceLoggerHandle"
dev_langs:
 - c++
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
 - GetTraceLoggerHandle
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetTraceLoggerHandle function


## -description


The 
<b>GetTraceLoggerHandle</b> function retrieves the handle of the event tracing session.
			

Providers can only call this function from their 
<a href="https://docs.microsoft.com/windows/desktop/ETW/controlcallback">ControlCallback</a> function.


## -parameters




### -param Buffer [in]

Pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/ETW/wnode-header">WNODE_HEADER</a> structure. ETW passes this structure to the provider's 
<a href="https://docs.microsoft.com/windows/desktop/ETW/controlcallback">ControlCallback</a> function in the <i>Buffer</i> parameter.

The <b>HistoricalContext</b> member of <a href="https://docs.microsoft.com/windows/desktop/ETW/wnode-header">WNODE_HEADER</a> contains the session's handle.


## -returns



If the function succeeds, it returns the event tracing session handle.
						

If the function fails, it returns <b>INVALID_HANDLE_VALUE</b>. To get extended error information, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.




## -remarks



You use the handle when calling the 
<a href="https://docs.microsoft.com/windows/desktop/ETW/gettraceenableflags">GetTraceEnableFlags</a> and 
<a href="https://docs.microsoft.com/windows/desktop/ETW/gettraceenablelevel">GetTraceEnableLevel</a> functions to retrieve the enable flags and level values passed to the <a href="https://docs.microsoft.com/windows/desktop/ETW/enabletrace">EnableTrace</a> function.


#### Examples

For an example that uses 
<b>GetTraceLoggerHandle</b>, see 
<a href="https://docs.microsoft.com/windows/desktop/ETW/retrieving-event-data-using-mof">Retrieving Event Data Using MOF</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/ETW/gettraceenableflags">GetTraceEnableFlags</a>



<a href="https://docs.microsoft.com/windows/desktop/ETW/gettraceenablelevel">GetTraceEnableLevel</a>
 

 

