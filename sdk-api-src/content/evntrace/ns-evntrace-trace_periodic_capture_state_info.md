---
UID: NS:evntrace._TRACE_PERIODIC_CAPTURE_STATE_INFO
title: TRACE_PERIODIC_CAPTURE_STATE_INFO (evntrace.h)
author: windows-sdk-content
description: Information relating to a periodic capture state.
old-location: etw\trace_periodic_capture_state_info.htm
tech.root: ETW
ms.assetid: 6C032D97-4B37-48D2-BD1A-35B8BA48B8AB
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PTRACE_PERIODIC_CAPTURE_STATE_INFO, PTRACE_PERIODIC_CAPTURE_STATE_INFO, PTRACE_PERIODIC_CAPTURE_STATE_INFO structure pointer [ETW], TRACE_PERIODIC_CAPTURE_STATE_INFO, TRACE_PERIODIC_CAPTURE_STATE_INFO structure [ETW], _TRACE_PERIODIC_CAPTURE_STATE_INFO, etw.trace_periodic_capture_state_info, evntrace/PTRACE_PERIODIC_CAPTURE_STATE_INFO, evntrace/TRACE_PERIODIC_CAPTURE_STATE_INFO"
ms.topic: struct
req.header: evntrace.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - HeaderDef
api_location:
 - Evntrace.h
api_name:
 - TRACE_PERIODIC_CAPTURE_STATE_INFO
product: Windows
targetos: Windows
req.typenames: TRACE_PERIODIC_CAPTURE_STATE_INFO, *PTRACE_PERIODIC_CAPTURE_STATE_INFO
req.redist: 
ms.custom: 19H1
---

# TRACE_PERIODIC_CAPTURE_STATE_INFO structure


## -description


Information relating to a periodic capture state.


## -struct-fields




### -field CaptureStateFrequencyInSeconds

The frequency of state captures in seconds. 


### -field ProviderCount

The number of providers.


### -field Reserved

Reserved for future use.


## -remarks



Periodic capture state is a way to allow capture state notifications to be routinely sent to providers. When this is enabled,  notifications will only be sent to provider registrations that have been previously enabled to the current session. Each provider can define its own response (if any) to a notification. Note that events logged by the provider in response to a notification will be sent to every ETW session that the provider is enabled to, similar to a manually requested capture state.

 To use periodic capture state:<ul>
<li>Allocate a buffer of type <b>TRACE_PERIODIC_CAPTURE_STATE_INFO</b>. The size of the buffer should be: sizeof(<b>TRACE_PERIODIC_CAPTURE_STATE_INFO</b>) + (x * sizeof(GUID)), where x is the number of providers you would like to enable.</li>
<li>Call <a href="https://docs.microsoft.com/windows/desktop/ETW/tracequeryinformation">TraceQueryInformation</a> using <b>TracePeriodicCaptureStateInfo</b> for the <a href="https://docs.microsoft.com/windows/desktop/ETW/trace-info-class">TRACE_INFO_CLASS</a> enumeration. Pass the buffer and its size as the <i>TraceInformation</i> and <i>InformationLength</i> parameters of <b>TraceQueryInformation</b>.</li>
<li>Set <b>CaptureStateFrequencyInSeconds</b> from <b>TRACE_PERIODIC_CAPTURE_STATE_INFO</b> to the minimum frequency supported by the version of Windows. This value may change in the future, so hard coding it is not recommended. If the frequency is below the minimum, the call to <a href="https://docs.microsoft.com/windows/desktop/ETW/tracesetinformation">TraceSetInformation</a> will fail. </li>
<li>Set the <b>ProviderCount</b> from  <b>TRACE_PERIODIC_CAPTURE_STATE_INFO</b> to the number of provider GUIDs being passed. </li>
<li>Add the GUIDs of each provider after the end of the <b>TRACE_PERIODIC_CAPTURE_STATE_INFO</b> structure. This uses the extra space allocated from (x * sizeof(GUID) from the first step.</li>
<li>Call <a href="https://docs.microsoft.com/windows/desktop/ETW/tracesetinformation">TraceSetInformation</a> using <b>TracePeriodicCaptureStateListInfo</b> from the <a href="https://docs.microsoft.com/windows/desktop/ETW/trace-info-class">TRACE_INFO_CLASS</a> enumeration. </li>
<li>To turn periodic capture state off, call <a href="https://docs.microsoft.com/windows/desktop/ETW/tracesetinformation">TraceSetInformation</a> again with <b>TracePeriodicCaptureStateListInfo</b> from the <a href="https://docs.microsoft.com/windows/desktop/ETW/trace-info-class">TRACE_INFO_CLASS</a>, NULL for the <b>TraceInformation</b>, and 0 as the <b>InformationLength</b>.</li>
</ul>




