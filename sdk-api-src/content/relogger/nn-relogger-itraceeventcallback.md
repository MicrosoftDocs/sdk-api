---
UID: NN:relogger.ITraceEventCallback
title: ITraceEventCallback
author: windows-sdk-content
description: Used by ETW to provide information to the relogger as the tracing process starts, ends, and logs events.
old-location: etw\ieventcallback.htm
tech.root: ETW
ms.assetid: 70139402-86e6-43b4-9016-42854ef998fd
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IEventCallback, IEventCallback interface [ETW], IEventCallback interface [ETW],described, ITraceEventCallback, etw.ieventcallback, relogger/ITraceEventCallback
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
 - IEventCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITraceEventCallback interface


## -description


The <b>ITraceEventCallback</b>  interface is used by ETW to provide information to the relogger as the tracing process starts, ends, and logs events.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEventCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITraceEventCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEventCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/acc6b1c4-9be1-490d-8b82-7ae8e73bd929">OnBeginProcessTrace</a>
</td>
<td align="left" width="63%">
Indicates that a trace is about to begin so that relogging can be started. Invoked before starting to process the events of the specified trace stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2099db80-89fd-4ce1-a7ca-e79abbd7b9e5">OnEvent</a>
</td>
<td align="left" width="63%">
Indicates that an event has been received on the trace streams associated with a relogger.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b152b6fd-4af5-4781-9c88-c71364ef86ff">OnFinalizeProcessTrace</a>
</td>
<td align="left" width="63%">
Indicates that a trace is about to end so that relogging can be finalized. Invoked when finished processing the events of the specified trace stream.

</td>
</tr>
</table> 


## -remarks



This interface is not supported on Windows 7 for the IA64 architecture.




## -see-also




<a href="https://msdn.microsoft.com/29b6f72a-ae81-4292-a023-a4bab16ae143">ITraceEvent</a>



<a href="https://msdn.microsoft.com/08073b9a-5ae0-4e88-a502-647567418005">ITraceRelogger</a>
 

 

