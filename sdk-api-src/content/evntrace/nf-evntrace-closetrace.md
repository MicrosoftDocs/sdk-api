---
UID: NF:evntrace.CloseTrace
title: CloseTrace function
author: windows-sdk-content
description: The CloseTrace function closes a trace.
old-location: etw\closetrace.htm
tech.root: etw
ms.assetid: 25f4c4d3-0b70-40fe-bf03-8f9ffd82fbec
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: CloseTrace, CloseTrace function [ETW], _evt_closetrace, base.closetrace, etw.closetrace, evntrace/CloseTrace
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
 - CloseTrace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CloseTrace function


## -description


The <b>CloseTrace</b> function closes a trace.


## -parameters




### -param TraceHandle [in]

Handle to the trace to close. The <a href="https://msdn.microsoft.com/505e643b-6b4f-4f93-96c8-7fe8abdd6234">OpenTrace</a> function 
      returns this handle.


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
Prior to Windows Vista, you cannot close the trace until the <a href="https://msdn.microsoft.com/aea25a95-f435-4068-9b15-7473f31ebf16">ProcessTrace</a> function completes.  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CTX_CLOSE_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The call was successful. The  <a href="https://msdn.microsoft.com/aea25a95-f435-4068-9b15-7473f31ebf16">ProcessTrace</a> function will stop after it has processed all real-time events in its buffers (it will not receive any new events).

</td>
</tr>
</table>
 




## -remarks



Consumers call this function.

If you are processing events from a log file, you call this function only after the 
     <a href="https://msdn.microsoft.com/aea25a95-f435-4068-9b15-7473f31ebf16">ProcessTrace</a> function returns. However, if you are 
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
     <a href="https://msdn.microsoft.com/0cfe2f62-63dc-45a6-96ce-fb4bf458358f">BufferCallback</a>, 
     <a href="https://msdn.microsoft.com/9312eaed-2997-4d44-952a-fcae3b262947">EventCallback</a>, or 
     <a href="https://msdn.microsoft.com/32e94f58-b8b6-4e0a-b53b-716a534ac374">EventClassCallback</a> callback.

<b>Prior to Windows Vista:  </b>You can call <b>CloseTrace</b> only after <a href="https://msdn.microsoft.com/aea25a95-f435-4068-9b15-7473f31ebf16">ProcessTrace</a> returns.


#### Examples

For an example that uses <b>CloseTrace</b>, see 
     <a href="https://msdn.microsoft.com/13512236-c416-43ba-bf36-b05c5c08d6c9">Retrieving Event Data Using MOF</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/505e643b-6b4f-4f93-96c8-7fe8abdd6234">OpenTrace</a>



<a href="https://msdn.microsoft.com/aea25a95-f435-4068-9b15-7473f31ebf16">ProcessTrace</a>
 

 

