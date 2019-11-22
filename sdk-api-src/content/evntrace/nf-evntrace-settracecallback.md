---
UID: NF:evntrace.SetTraceCallback
title: SetTraceCallback function (evntrace.h)

description: The SetTraceCallback function specifies an EventClassCallback function to process events for the specified event trace class.
old-location: etw\settracecallback.htm
tech.root: ETW
ms.assetid: 8663f64f-a203-43e5-94e8-337f2d81c3a0

ms.date: 12/05/2018
ms.keywords: SetTraceCallback, SetTraceCallback function [ETW], _evt_settracecallback, base.settracecallback, etw.settracecallback, evntrace/SetTraceCallback
ms.topic: function
f1_keywords: 
 - "evntrace/SetTraceCallback"
dev_langs:
 - c++
req.header: evntrace.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - API-MS-Win-eventing-Obsolete-l1-1-0.dll
 - KernelBase.dll
api_name:
 - SetTraceCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetTraceCallback function


## -description


<p class="CCE_Message">[Do not use this function; it may be unavailable in subsequent versions. Instead, filter 
    for the event trace class in your 
    <a href="https://docs.microsoft.com/windows/desktop/ETW/eventrecordcallback">EventRecordCallback</a> function.]

The <b>SetTraceCallback</b> function specifies an 
    <a href="https://docs.microsoft.com/windows/desktop/ETW/eventclasscallback">EventClassCallback</a> function to process events for 
    the specified event trace class.


## -parameters




### -param pGuid [in]

Pointer to the class GUID of an event trace class for which you want to receive events. For a list of 
      kernel provider class GUIDs, see 
      <a href="https://docs.microsoft.com/windows/desktop/ETW/nt-kernel-logger-constants">NT Kernel Logger Constants</a>.


### -param EventCallback [in]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/ETW/eventclasscallback">EventClassCallback</a> 
      function used to process events belonging to the event trace class.


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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the following is true:

<ul>
<li><i>pGuid</i> is <b>NULL</b>.</li>
<li><i>EventCallback</i> is <b>NULL</b>.</li>
</ul>
</td>
</tr>
</table>
 




## -remarks



Consumers call this function.

You can only specify one callback function for an event trace class. If you specify more than one callback 
    function for the even trace class, the last callback function receives the events for that event trace class.

To stop the callback function from receiving events for the event trace class, call the 
    <a href="https://docs.microsoft.com/windows/desktop/ETW/removetracecallback">RemoveTraceCallback</a> function. The callback 
    automatically stops receiving callbacks when you close the trace.

You can use this function to receive events written using one of the 
    <a href="https://docs.microsoft.com/windows/desktop/ETW/traceevent">TraceEvent</a> functions. You cannot use this function to 
    consume events from a provider that used one of the 
    <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/nf-evntprov-eventwrite">EventWrite</a> functions to log events.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/ETW/eventclasscallback">EventClassCallback</a>



<a href="https://docs.microsoft.com/windows/desktop/ETW/processtrace">ProcessTrace</a>



<a href="https://docs.microsoft.com/windows/desktop/ETW/removetracecallback">RemoveTraceCallback</a>
 

 

