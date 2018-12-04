---
UID: NN:relogger.ITraceRelogger
title: ITraceRelogger
author: windows-sdk-content
description: Provides access to the relogging functionality, allowing you to manipulate and relog events from an ETW trace stream.
old-location: etw\itracerelogger.htm
tech.root: etw
ms.assetid: 08073b9a-5ae0-4e88-a502-647567418005
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ITraceRelogger, ITraceRelogger interface [ETW], ITraceRelogger interface [ETW],described, etw.itracerelogger, relogger/ITraceRelogger
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
 - ITraceRelogger
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITraceRelogger interface


## -description


The <b>ITraceRelogger</b>  interface provides access to the relogging functionality, allowing you to manipulate and relog events from an ETW trace stream.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITraceRelogger</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITraceRelogger</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITraceRelogger</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2bdf6175-f4c6-4217-a37a-b2af32ad38c6">AddLogfileTraceStream</a>
</td>
<td align="left" width="63%">
Adds a new logfile-based ETW trace stream to the relogger.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/68bb5715-49b8-45bc-ae98-0b4a519c8e62">AddRealtimeTraceStream</a>
</td>
<td align="left" width="63%">
Adds a new real-time ETW trace stream to the relogger.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d195f746-7f56-443f-9232-e95a6b026331">Cancel</a>
</td>
<td align="left" width="63%">
Terminates the relogging process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a000e38-018d-4077-bf4c-0bfec6cdb676">CreateEventInstance</a>
</td>
<td align="left" width="63%">
Generates a new event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c9d19ad9-182d-469e-b783-2061b7150933">Inject</a>
</td>
<td align="left" width="63%">
Injects a non-system-generated event into the event stream being written to the output file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab844b34-0e06-447f-a0b7-dd56ca0b50ed">ProcessTrace</a>
</td>
<td align="left" width="63%">
Delivers events from the associated trace streams to the consumer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3c739bd-9285-49ec-b2cf-d607f3d9be0c">RegisterCallback</a>
</td>
<td align="left" width="63%">
Registers an implementation of <a href="https://msdn.microsoft.com/70139402-86e6-43b4-9016-42854ef998fd">ITraceEventCallback</a> with the relogger in order to signal trace activity.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2a758af0-2316-4c4b-8717-ee1ebad205ee">SetCompressionMode</a>
</td>
<td align="left" width="63%">
Enables or disables compression on the relogged trace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed3f8bcd-88c7-4d05-a396-41ee8f35bc97">SetOutputFilename</a>
</td>
<td align="left" width="63%">
Indicates the file to which ETW should write the new, relogged trace.

</td>
</tr>
</table> 


## -remarks



This interface is not supported on Windows 7 for the IA64 architecture.




## -see-also




<a href="https://msdn.microsoft.com/29b6f72a-ae81-4292-a023-a4bab16ae143">ITraceEvent</a>



<a href="https://msdn.microsoft.com/70139402-86e6-43b4-9016-42854ef998fd">ITraceEventCallback</a>
 

 

