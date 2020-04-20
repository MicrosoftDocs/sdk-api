---
UID: NN:relogger.ITraceRelogger
title: ITraceRelogger (relogger.h)
description: Provides access to the relogging functionality, allowing you to manipulate and relog events from an ETW trace stream.helpviewer_keywords: ["ITraceRelogger","ITraceRelogger interface [ETW]","ITraceRelogger interface [ETW]","described","etw.itracerelogger","relogger/ITraceRelogger"]
old-location: etw\itracerelogger.htm
tech.root: ETW
ms.assetid: 08073b9a-5ae0-4e88-a502-647567418005
ms.date: 12/05/2018
ms.keywords: ITraceRelogger, ITraceRelogger interface [ETW], ITraceRelogger interface [ETW],described, etw.itracerelogger, relogger/ITraceRelogger
f1_keywords:
- relogger/ITraceRelogger
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
- ITraceRelogger
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITraceRelogger interface


## -description


The <b>ITraceRelogger</b>  interface provides access to the relogging functionality, allowing you to manipulate and relog events from an ETW trace stream.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITraceRelogger</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITraceRelogger</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/relogger/nf-relogger-itracerelogger-addlogfiletracestream">AddLogfileTraceStream</a>
</td>
<td align="left" width="63%">
Adds a new logfile-based ETW trace stream to the relogger.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/relogger/nf-relogger-itracerelogger-addrealtimetracestream">AddRealtimeTraceStream</a>
</td>
<td align="left" width="63%">
Adds a new real-time ETW trace stream to the relogger.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/relogger/nf-relogger-itracerelogger-cancel">Cancel</a>
</td>
<td align="left" width="63%">
Terminates the relogging process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/relogger/nf-relogger-itracerelogger-createeventinstance">CreateEventInstance</a>
</td>
<td align="left" width="63%">
Generates a new event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/relogger/nf-relogger-itracerelogger-inject">Inject</a>
</td>
<td align="left" width="63%">
Injects a non-system-generated event into the event stream being written to the output file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/relogger/nf-relogger-itracerelogger-processtrace">ProcessTrace</a>
</td>
<td align="left" width="63%">
Delivers events from the associated trace streams to the consumer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/relogger/nf-relogger-itracerelogger-registercallback">RegisterCallback</a>
</td>
<td align="left" width="63%">
Registers an implementation of <a href="https://docs.microsoft.com/windows/desktop/api/relogger/nn-relogger-itraceeventcallback">ITraceEventCallback</a> with the relogger in order to signal trace activity.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/relogger/nf-relogger-itracerelogger-setcompressionmode">SetCompressionMode</a>
</td>
<td align="left" width="63%">
Enables or disables compression on the relogged trace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/relogger/nf-relogger-itracerelogger-setoutputfilename">SetOutputFilename</a>
</td>
<td align="left" width="63%">
Indicates the file to which ETW should write the new, relogged trace.

</td>
</tr>
</table> 


## -remarks



This interface is not supported on Windows 7 for the IA64 architecture.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/relogger/nn-relogger-itraceevent">ITraceEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/relogger/nn-relogger-itraceeventcallback">ITraceEventCallback</a>
 

 

