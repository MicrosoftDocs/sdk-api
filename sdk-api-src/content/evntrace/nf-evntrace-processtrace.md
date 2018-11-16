---
UID: NF:evntrace.ProcessTrace
title: ProcessTrace function
author: windows-sdk-content
description: The ProcessTrace function delivers events from one or more event tracing sessions to the consumer.
old-location: etw\processtrace.htm
tech.root: ETW
ms.assetid: aea25a95-f435-4068-9b15-7473f31ebf16
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ProcessTrace, ProcessTrace function [ETW], _evt_processtrace, base.processtrace, etw.processtrace, evntrace/ProcessTrace
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
req.lib: Sechost.lib on Windows 8.1 and Windows Server 2012 R2; Advapi32.lib on Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista and Windows XP
req.dll: Sechost.dll on Windows 8.1 and Windows Server 2012 R2; Advapi32.dll on Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista and Windows XP
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Sechost.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvAPI32-l2-1-1.dll
 - API-MS-Win-Eventing-Consumer-l1-1-0.dll
 - KernelBase.dll
api_name:
 - ProcessTrace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ProcessTrace
: 
---

# ProcessTrace function


## -description


The <b>ProcessTrace</b> function delivers events from one or 
   more event tracing sessions to the consumer.


## -parameters




### -param HandleArray [in]

Pointer to an array of trace handles obtained from earlier calls to the 
       <a href="https://msdn.microsoft.com/505e643b-6b4f-4f93-96c8-7fe8abdd6234">OpenTrace</a> function. The number of handles that you can 
       specify is limited to 64.

The array can contain the handles to multiple log files, but only one real-time trace session.


### -param HandleCount [in]

Number of elements in <i>HandleArray</i>.


### -param StartTime [in]

Pointer to an optional <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that 
      specifies the beginning time period for which you want to receive events. The function does not deliver events 
      recorded prior to <i>StartTime</i>.


### -param EndTime [in]

Pointer to an optional <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that 
       specifies the ending time period for which you want to receive events. The function does not deliver events 
       recorded after  <i>EndTime</i>.

<b>Windows Server 2003:  </b>This value is ignored for real-time event delivery.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is one of the 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>. The following table includes some 
       common errors and their causes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_LENGTH</b></dt>
</dl>
</td>
<td width="60%">
<i>HandleCount</i> is not valid or the number of handles is greater than 64.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
An element of <i>HandleArray</i> is not a valid event tracing session handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_TIME</b></dt>
</dl>
</td>
<td width="60%">
<i>EndTime</i> is less than <i>StartTime</i>.
       

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
<i>HandleArray</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOACCESS</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred in one of the callback functions that receives the events.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
Indicates the consumer canceled processing by returning <b>FALSE</b> in their 
        <a href="https://msdn.microsoft.com/0cfe2f62-63dc-45a6-96ce-fb4bf458358f">BufferCallback</a> function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WMI_INSTANCE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The session from which you are trying to consume events in real time is not running or does not have the 
        real-time trace mode enabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WMI_ALREADY_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
The <i>HandleArray</i> parameter contains the handle to more than one real-time 
        session.

</td>
</tr>
</table>
 




## -remarks



Consumers call this function.

You must call the <a href="https://msdn.microsoft.com/505e643b-6b4f-4f93-96c8-7fe8abdd6234">OpenTrace</a> function prior to 
    calling <b>ProcessTrace</b>.

The <b>ProcessTrace</b> function delivers the events to the 
    consumer's  <a href="https://msdn.microsoft.com/0cfe2f62-63dc-45a6-96ce-fb4bf458358f">BufferCallback</a>, 
    <a href="https://msdn.microsoft.com/9312eaed-2997-4d44-952a-fcae3b262947">EventCallback</a>, and 
    <a href="https://msdn.microsoft.com/32e94f58-b8b6-4e0a-b53b-716a534ac374">EventClassCallback</a> callback functions.

The <b>ProcessTrace</b> function sorts the events 
    chronologically and delivers all events generated between <i>StartTime</i> and 
    <i>EndTime</i>. Note that events can appear out of order if the session specifies system time 
    as the clock (low resolution) and the volume of events is high. In this case, it is possible for multiple events 
    to contain the same time stamp. If multiple events contain the same time stamp, ETW cannot guarantee the order of 
    those events.

The <b>ProcessTrace</b> function blocks the thread until it 
     delivers all events, the <a href="https://msdn.microsoft.com/0cfe2f62-63dc-45a6-96ce-fb4bf458358f">BufferCallback</a> 
     function returns <b>FALSE</b>, or you call 
     <a href="https://msdn.microsoft.com/25f4c4d3-0b70-40fe-bf03-8f9ffd82fbec">CloseTrace</a>. If the consumer is consuming events in real 
     time, the <b>ProcessTrace</b> function returns after the 
     controller stops the trace session. (Note that there may be a several-second delay before the function 
     returns.)

<b>Windows Server 2003:  </b>You can call <a href="https://msdn.microsoft.com/25f4c4d3-0b70-40fe-bf03-8f9ffd82fbec">CloseTrace</a> only after 
      <b>ProcessTrace</b> returns.


#### Examples

For an example that uses <b>ProcessTrace</b>, see 
     <a href="https://msdn.microsoft.com/5ebd500c-420e-4979-a03a-49b687464b0e">Using TdhFormatProperty to Consume Event Data</a> 
     or <a href="https://msdn.microsoft.com/13512236-c416-43ba-bf36-b05c5c08d6c9">Retrieving Event Data Using MOF</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0cfe2f62-63dc-45a6-96ce-fb4bf458358f">BufferCallback</a>



<a href="https://msdn.microsoft.com/9312eaed-2997-4d44-952a-fcae3b262947">EventCallback</a>



<a href="https://msdn.microsoft.com/32e94f58-b8b6-4e0a-b53b-716a534ac374">EventClassCallback</a>



<a href="https://msdn.microsoft.com/505e643b-6b4f-4f93-96c8-7fe8abdd6234">OpenTrace</a>



<a href="https://msdn.microsoft.com/8663f64f-a203-43e5-94e8-337f2d81c3a0">SetTraceCallback</a>
 

 

