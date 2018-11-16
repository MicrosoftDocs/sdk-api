---
UID: NN:relogger.ITraceEvent
title: ITraceEvent
author: windows-sdk-content
description: Provides access to data relating to a specific event.
old-location: etw\ievent.htm
tech.root: ETW
ms.assetid: 29b6f72a-ae81-4292-a023-a4bab16ae143
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ITraceEvent, ITraceEvent interface [ETW], ITraceEvent interface [ETW],described, etw.ievent, relogger/ITraceEvent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITraceEvent interface


## -description


The <b>ITraceEvent</b> interface  provides access to data relating to a specific event.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITraceEvent</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITraceEvent</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/a4fa29f4-a265-4b42-a499-bc53566dc889">Clone</a>
</td>
<td align="left" width="63%">
Creates a duplicate copy of an event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a1c2313-431a-4243-9272-99dec1bf78dd">GetEventRecord</a>
</td>
<td align="left" width="63%">
Retrieves the event record that describes an event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d4d8abd-b48a-487b-bb73-a6fa48c512c7">GetUserContext</a>
</td>
<td align="left" width="63%">
Retrieves the user context (specified by <a href="https://msdn.microsoft.com/2bdf6175-f4c6-4217-a37a-b2af32ad38c6">ITraceRelogger::AddLogfileTraceStream</a>) associated with the stream to which the event belongs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/729a887e-1759-44d5-a7d5-8385d648eebf">SetEventDescriptor</a>
</td>
<td align="left" width="63%">
Sets the event descriptor for an event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49f0b490-d693-4566-9857-43befdd31d56">SetKernelTime</a>
</td>
<td align="left" width="63%">
Sets the elapsed execution time for kernel-mode instructions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/180e0487-5262-45ae-a701-3fcb575637ae">SetPayload</a>
</td>
<td align="left" width="63%">
Sets the payload for an event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c2e5e6bf-cdff-42fa-9352-2f234f39849d">SetProcessId</a>
</td>
<td align="left" width="63%">
Sets the process to which an event belongs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8f151cd5-918c-4380-a870-9a42fb5611b1">SetProcessorNumber</a>
</td>
<td align="left" width="63%">
Sets the processor for an event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dc61ff9e-2af9-4428-82df-84635313ddc6">SetProviderId</a>
</td>
<td align="left" width="63%">
Sets the provider of an event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f5d293e-da87-4b83-9407-fc4179a42a46">SetThreadId</a>
</td>
<td align="left" width="63%">
Sets the identifier of a thread that generates an event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e1f76887-8edd-414e-bee3-36b61709c2b5">SetTimeStamp</a>
</td>
<td align="left" width="63%">
Sets the time at which an event occurred.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a1d95256-9357-44d1-88e3-efc97a65a0d4">SetUserTime</a>
</td>
<td align="left" width="63%">
Sets the elapsed execution time for user-mode instructions.

</td>
</tr>
</table> 


## -remarks



This interface is not supported on Windows 7 for the IA64 architecture.




## -see-also




<a href="https://msdn.microsoft.com/70139402-86e6-43b4-9016-42854ef998fd">ITraceEventCallback</a>



<a href="https://msdn.microsoft.com/08073b9a-5ae0-4e88-a502-647567418005">ITraceRelogger</a>
 

 

