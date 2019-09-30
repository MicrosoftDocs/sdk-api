---
UID: NF:evntrace.CloseTrace
title: CloseTrace function (evntrace.h)
author: windows-sdk-content
description: The CloseTrace function closes a trace.
old-location: etw\closetrace.htm
tech.root: ETW
ms.assetid: 25f4c4d3-0b70-40fe-bf03-8f9ffd82fbec
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CloseTrace, CloseTrace function [ETW], _evt_closetrace, base.closetrace, etw.closetrace, evntrace/CloseTrace
ms.topic: function
f1_keywords: 
 - "evntrace/CloseTrace"
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
 - CloseTrace
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CloseTrace function


## -description


The <b>CloseTrace</b> function closes a trace.


## -parameters




### -param TraceHandle [in]

Handle to the trace to close. The <a href="https://docs.microsoft.com/windows/desktop/ETW/opentrace">OpenTrace</a> function 
      returns this handle.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is one of the 
       <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>. The following table includes some 
       common errors and their causes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
One of the following is true:

<ul>
<li><i>TraceHandle</i> is <b>NULL</b>.</li>
<li><i>TraceHandle</i> is INVALID_HANDLE_VALUE.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUSY</b></dt>
</dl>
</td>
<td width="60%">
Prior to Windows Vista, you cannot close the trace until the <a href="https://docs.microsoft.com/windows/desktop/ETW/processtrace">ProcessTrace</a> function completes.  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CTX_CLOSE_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The call was successful. The  <a href="https://docs.microsoft.com/windows/desktop/ETW/processtrace">ProcessTrace</a> function will stop after it has processed all real-time events in its buffers (it will not receive any new events).

</td>
</tr>
</table>
 




## -remarks



Consumers call this function.

If you are processing events from a log file, you call this function only after the 
     <a href="https://docs.microsoft.com/windows/desktop/ETW/processtrace">ProcessTrace</a> function returns. However, if you are 
     processing real-time events, you can call this function before 
     <b>ProcessTrace</b> returns. If you call this function before 
     <b>ProcessTrace</b> returns, the 
     <b>CloseTrace</b> function returns ERROR_CTX_CLOSE_PENDING. The 
     ERROR_CTX_CLOSE_PENDING code indicates that the <b>CloseTrace</b> 
     function call was successful; the  <b>ProcessTrace</b> function 
     will stop processing events after it processes all events in its buffers 
     (<b>ProcessTrace</b> will not receive any new events after you 
     call the <b>CloseTrace</b> function). You can call the 
     <b>CloseTrace</b> function from your 
     <a href="https://docs.microsoft.com/windows/desktop/ETW/buffercallback">BufferCallback</a>, 
     <a href="https://docs.microsoft.com/windows/desktop/ETW/eventcallback">EventCallback</a>, or 
     <a href="https://docs.microsoft.com/windows/desktop/ETW/eventclasscallback">EventClassCallback</a> callback.

<b>Prior to Windows Vista:  </b>You can call <b>CloseTrace</b> only after <a href="https://docs.microsoft.com/windows/desktop/ETW/processtrace">ProcessTrace</a> returns.


#### Examples

For an example that uses <b>CloseTrace</b>, see 
     <a href="https://docs.microsoft.com/windows/desktop/ETW/retrieving-event-data-using-mof">Retrieving Event Data Using MOF</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/ETW/opentrace">OpenTrace</a>



<a href="https://docs.microsoft.com/windows/desktop/ETW/processtrace">ProcessTrace</a>
 

 

