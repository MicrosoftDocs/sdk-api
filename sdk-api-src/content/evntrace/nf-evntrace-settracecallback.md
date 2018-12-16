---
UID: NF:evntrace.SetTraceCallback
title: SetTraceCallback function
author: windows-sdk-content
description: The SetTraceCallback function specifies an EventClassCallback function to process events for the specified event trace class.
old-location: etw\settracecallback.htm
tech.root: etw
ms.assetid: 8663f64f-a203-43e5-94e8-337f2d81c3a0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetTraceCallback, SetTraceCallback function [ETW], _evt_settracecallback, base.settracecallback, etw.settracecallback, evntrace/SetTraceCallback
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetTraceCallback function


## -description


<p class="CCE_Message">[Do not use this function; it may be unavailable in subsequent versions. Instead, filter 
    for the event trace class in your 
    <a href="https://msdn.microsoft.com/80a30faf-af1f-4440-8a17-9df44bdb2291">EventRecordCallback</a> function.]

The <b>SetTraceCallback</b> function specifies an 
    <a href="https://msdn.microsoft.com/32e94f58-b8b6-4e0a-b53b-716a534ac374">EventClassCallback</a> function to process events for 
    the specified event trace class.


## -parameters




### -param pGuid [in]

Pointer to the class GUID of an event trace class for which you want to receive events. For a list of 
      kernel provider class GUIDs, see 
      <a href="https://msdn.microsoft.com/f64f05c1-b904-4847-8502-4abb9cf4d37f">NT Kernel Logger Constants</a>.


### -param EventCallback [in]

Pointer to an <a href="https://msdn.microsoft.com/32e94f58-b8b6-4e0a-b53b-716a534ac374">EventClassCallback</a> 
      function used to process events belonging to the event trace class.


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
    <a href="https://msdn.microsoft.com/da779e8d-4984-44e3-8731-647a422b55b2">RemoveTraceCallback</a> function. The callback 
    automatically stops receiving callbacks when you close the trace.

You can use this function to receive events written using one of the 
    <a href="https://msdn.microsoft.com/9b21f6f0-dd9b-4f9c-a879-846901a3bab7">TraceEvent</a> functions. You cannot use this function to 
    consume events from a provider that used one of the 
    <a href="https://msdn.microsoft.com/93070eb7-c167-4419-abff-e861877dad07">EventWrite</a> functions to log events.




## -see-also




<a href="https://msdn.microsoft.com/32e94f58-b8b6-4e0a-b53b-716a534ac374">EventClassCallback</a>



<a href="https://msdn.microsoft.com/aea25a95-f435-4068-9b15-7473f31ebf16">ProcessTrace</a>



<a href="https://msdn.microsoft.com/da779e8d-4984-44e3-8731-647a422b55b2">RemoveTraceCallback</a>
 

 

