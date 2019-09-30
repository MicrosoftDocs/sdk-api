---
UID: NF:evntrace.RemoveTraceCallback
title: RemoveTraceCallback function (evntrace.h)
author: windows-sdk-content
description: The RemoveTraceCallback function stops an EventClassCallback function from receiving events for an event trace class.
old-location: etw\removetracecallback.htm
tech.root: ETW
ms.assetid: da779e8d-4984-44e3-8731-647a422b55b2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RemoveTraceCallback, RemoveTraceCallback function [ETW], _evt_removetracecallback, base.removetracecallback, etw.removetracecallback, evntrace/RemoveTraceCallback
ms.topic: function
f1_keywords: 
 - "evntrace/RemoveTraceCallback"
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
 - API-MS-Win-Eventing-Obsolete-l1-1-0.dll
 - KernelBase.dll
api_name:
 - RemoveTraceCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RemoveTraceCallback function


## -description


<p class="CCE_Message">[Do not use this function; it may be unavailable in subsequent versions.]

The <b>RemoveTraceCallback</b> function stops an 
    <a href="https://docs.microsoft.com/windows/desktop/ETW/eventclasscallback">EventClassCallback</a> function from receiving events 
    for an event trace class.


## -parameters




### -param pGuid [in]

Pointer to the class GUID of the event trace class for which the callback receives events. Use the same 
      class GUID that you passed to the <a href="https://docs.microsoft.com/windows/desktop/ETW/settracecallback">SetTraceCallback</a> 
      to begin receiving the events.


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
The <i>pGuid</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WMI_GUID_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
There is no <a href="https://docs.microsoft.com/windows/desktop/ETW/eventclasscallback">EventClassCallback</a> 
        function associated with the event trace class.

</td>
</tr>
</table>
 




## -remarks



Consumers call this function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/ETW/eventclasscallback">EventClassCallback</a>



<a href="https://docs.microsoft.com/windows/desktop/ETW/processtrace">ProcessTrace</a>



<a href="https://docs.microsoft.com/windows/desktop/ETW/settracecallback">SetTraceCallback</a>
 

 

