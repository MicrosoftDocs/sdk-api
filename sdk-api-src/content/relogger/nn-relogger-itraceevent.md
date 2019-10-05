---
UID: NN:relogger.ITraceEvent
title: ITraceEvent (relogger.h)
author: windows-sdk-content
description: Provides access to data relating to a specific event.
old-location: etw\ievent.htm
tech.root: ETW
ms.assetid: 29b6f72a-ae81-4292-a023-a4bab16ae143
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITraceEvent, ITraceEvent interface [ETW], ITraceEvent interface [ETW],described, etw.ievent, relogger/ITraceEvent
ms.topic: interface
f1_keywords: 
 - "relogger/ITraceEvent"
dev_langs:
 - c++
req.header: relogger.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Relogger.idl
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
 - COM
api_location:
 - Relogger.h
api_name:
 - ITraceEvent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITraceEvent interface


## -description


The <b>ITraceEvent</b> interface  provides access to data relating to a specific event.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITraceEvent</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITraceEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITraceEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/relogger/nf-relogger-itraceevent-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a duplicate copy of an event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/relogger/nf-relogger-itraceevent-geteventrecord">GetEventRecord</a>
</td>
<td align="left" width="63%">
Retrieves the event record that describes an event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/relogger/nf-relogger-itraceevent-getusercontext">GetUserContext</a>
</td>
<td align="left" width="63%">
Retrieves the user context (specified by <a href="https://docs.microsoft.com/windows/desktop/api/relogger/nf-relogger-itracerelogger-addlogfiletracestream">ITraceRelogger::AddLogfileTraceStream</a>) associated with the stream to which the event belongs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/relogger/nf-relogger-itraceevent-seteventdescriptor">SetEventDescriptor</a>
</td>
<td align="left" width="63%">
Sets the event descriptor for an event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh706649(v=vs.85)">SetKernelTime</a>
</td>
<td align="left" width="63%">
Sets the elapsed execution time for kernel-mode instructions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/relogger/nf-relogger-itraceevent-setpayload">SetPayload</a>
</td>
<td align="left" width="63%">
Sets the payload for an event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/relogger/nf-relogger-itraceevent-setprocessid">SetProcessId</a>
</td>
<td align="left" width="63%">
Sets the process to which an event belongs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh706652(v=vs.85)">SetProcessorNumber</a>
</td>
<td align="left" width="63%">
Sets the processor for an event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/relogger/nf-relogger-itraceevent-setproviderid">SetProviderId</a>
</td>
<td align="left" width="63%">
Sets the provider of an event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/relogger/nf-relogger-itraceevent-setthreadid">SetThreadId</a>
</td>
<td align="left" width="63%">
Sets the identifier of a thread that generates an event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/relogger/nf-relogger-itraceevent-settimestamp">SetTimeStamp</a>
</td>
<td align="left" width="63%">
Sets the time at which an event occurred.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh706656(v=vs.85)">SetUserTime</a>
</td>
<td align="left" width="63%">
Sets the elapsed execution time for user-mode instructions.

</td>
</tr>
</table> 


## -remarks



This interface is not supported on Windows 7 for the IA64 architecture.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/relogger/nn-relogger-itraceeventcallback">ITraceEventCallback</a>



<a href="https://docs.microsoft.com/windows/desktop/api/relogger/nn-relogger-itracerelogger">ITraceRelogger</a>
 

 

