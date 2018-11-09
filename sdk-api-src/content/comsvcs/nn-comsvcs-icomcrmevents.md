---
UID: NN:comsvcs.IComCRMEvents
title: IComCRMEvents
author: windows-sdk-content
description: Notifies the subscriber about activities of the Compensating Resource Manager (CRM) feature of Component Services.
old-location: cos\icomcrmevents.htm
tech.root: cossdk
ms.assetid: 720beffb-8fb5-4c87-9bcf-6db214543b01
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IComCRMEvents, IComCRMEvents interface [COM+], IComCRMEvents interface [COM+],described, _dtc_icomcrmevents, comsvcs/IComCRMEvents, cos.icomcrmevents
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: comsvcs.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IComCRMEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComCRMEvents interface


## -description


Notifies the subscriber about activities of the Compensating Resource Manager (CRM) feature of Component Services. The events are published to the subscriber using the <a href="https://msdn.microsoft.com/en-us/library/ms679237(v=VS.85).aspx">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComCRMEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IComCRMEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComCRMEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9def1696-8bc7-4294-a848-ff8ad2632ed6">OnCRMAbort</a>
</td>
<td align="left" width="63%">
Generated when CRM clerk receives an abort notification to pass on to the CRM compensator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms678903(v=VS.85).aspx">OnCRMAnalyze</a>
</td>
<td align="left" width="63%">
Generated when a CRM clerk receives a record during the analysis phase of recovery.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms683635(v=VS.85).aspx">OnCRMBegin</a>
</td>
<td align="left" width="63%">
Generated when a CRM clerk is starting, either due to a client registering a compensator or during recovery.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms687811(v=VS.85).aspx">OnCRMCheckpoint</a>
</td>
<td align="left" width="63%">
Generated when a CRM checkpoint occurs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms682796(v=VS.85).aspx">OnCRMCommit</a>
</td>
<td align="left" width="63%">
Generated when CRM clerk receives a commit notification to pass on to the CRM compensator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms687642(v=VS.85).aspx">OnCRMDeliver</a>
</td>
<td align="left" width="63%">
Generated when a CRM clerk delivers a record to a CRM compensator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms683621(v=VS.85).aspx">OnCRMDone</a>
</td>
<td align="left" width="63%">
Generated when CRM clerk is done processing transaction outcome notifications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms684235(v=VS.85).aspx">OnCRMForce</a>
</td>
<td align="left" width="63%">
Generated when a CRM clerk receives a request to force log records to disk, either from the CRM worker or from the CRM compensator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms679539(v=VS.85).aspx">OnCRMForget</a>
</td>
<td align="left" width="63%">
Generated when a CRM clerk receives a request to forget a log record, either from the CRM worker or from the CRM compensator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms685962(v=VS.85).aspx">OnCRMIndoubt</a>
</td>
<td align="left" width="63%">
Generated when CRM clerk receives an in-doubt notification to pass on to the CRM compensator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms679188(v=VS.85).aspx">OnCRMPrepare</a>
</td>
<td align="left" width="63%">
Generated when CRM clerk receives a prepare notification to pass on to the CRM compensator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms681301(v=VS.85).aspx">OnCRMRecoveryDone</a>
</td>
<td align="left" width="63%">
Generated when CRM recovery is done.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms685194(v=VS.85).aspx">OnCRMRecoveryStart</a>
</td>
<td align="left" width="63%">
Generated when CRM recovery has started.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms687644(v=VS.85).aspx">OnCRMRelease</a>
</td>
<td align="left" width="63%">
Generated when the CRM clerk is finished and releases its resource locks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms678907(v=VS.85).aspx">OnCRMWrite</a>
</td>
<td align="left" width="63%">
Generated when a CRM clerk receives a request to write a log record, either from the CRM worker or CRM compensator.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms679237(v=VS.85).aspx">COM+ Events</a>



<a href="https://msdn.microsoft.com/en-us/library/ms678896(v=VS.85).aspx">COM+ Instrumentation</a>
 

 

