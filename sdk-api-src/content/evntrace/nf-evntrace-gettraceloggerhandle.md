---
UID: NF:evntrace.GetTraceLoggerHandle
title: GetTraceLoggerHandle function
author: windows-sdk-content
description: The GetTraceLoggerHandle function retrieves the handle of the event tracing session. Providers can only call this function from their ControlCallback function.
old-location: etw\gettraceloggerhandle.htm
tech.root: ETW
ms.assetid: 050d3a01-0087-40f1-af35-b9ceeaf47813
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetTraceLoggerHandle, GetTraceLoggerHandle function [ETW], _evt_gettraceloggerhandle, base.gettraceloggerhandle, etw.gettraceloggerhandle, evntrace/GetTraceLoggerHandle
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
 - GetTraceLoggerHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetTraceLoggerHandle function


## -description


The 
<b>GetTraceLoggerHandle</b> function retrieves the handle of the event tracing session.
			

Providers can only call this function from their 
<a href="https://msdn.microsoft.com/e9f70ae6-906f-4e55-bca7-4355f1ca6091">ControlCallback</a> function.


## -parameters




### -param Buffer [in]

Pointer to a 
<a href="https://msdn.microsoft.com/862a8f46-a326-48c6-92b7-8bb667837bb7">WNODE_HEADER</a> structure. ETW passes this structure to the provider's 
<a href="https://msdn.microsoft.com/e9f70ae6-906f-4e55-bca7-4355f1ca6091">ControlCallback</a> function in the <i>Buffer</i> parameter.

The <b>HistoricalContext</b> member of <a href="https://msdn.microsoft.com/862a8f46-a326-48c6-92b7-8bb667837bb7">WNODE_HEADER</a> contains the session's handle.


## -returns



If the function succeeds, it returns the event tracing session handle.
						

If the function fails, it returns <b>INVALID_HANDLE_VALUE</b>. To get extended error information, call the 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



You use the handle when calling the 
<a href="https://msdn.microsoft.com/e5c0f2bf-34da-4555-9556-4c79ee9a73ab">GetTraceEnableFlags</a> and 
<a href="https://msdn.microsoft.com/22326fd9-c428-4430-8a92-978d005f6705">GetTraceEnableLevel</a> functions to retrieve the enable flags and level values passed to the <a href="https://msdn.microsoft.com/d75f18e1-e5fa-4039-bb74-76dea334b0fd">EnableTrace</a> function.


#### Examples

For an example that uses 
<b>GetTraceLoggerHandle</b>, see 
<a href="https://msdn.microsoft.com/13512236-c416-43ba-bf36-b05c5c08d6c9">Retrieving Event Data Using MOF</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/e5c0f2bf-34da-4555-9556-4c79ee9a73ab">GetTraceEnableFlags</a>



<a href="https://msdn.microsoft.com/22326fd9-c428-4430-8a92-978d005f6705">GetTraceEnableLevel</a>
 

 

