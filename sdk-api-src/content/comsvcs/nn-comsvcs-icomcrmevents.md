---
UID: NN:comsvcs.IComCRMEvents
title: IComCRMEvents
author: windows-sdk-content
description: Notifies the subscriber about activities of the Compensating Resource Manager (CRM) feature of Component Services.
old-location: cos\icomcrmevents.htm
old-project: cossdk
ms.assetid: 720beffb-8fb5-4c87-9bcf-6db214543b01
ms.author: windowssdkdev
ms.date: 05/16/2018
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
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IComCRMEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComCRMEvents interface


## -description


Notifies the subscriber about activities of the Compensating Resource Manager (CRM) feature of Component Services. The events are published to the subscriber using the <a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


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
<a href="https://msdn.microsoft.com/08bdc192-f1f8-4d0d-a432-cf6316d8033a">OnCRMAnalyze</a>
</td>
<td align="left" width="63%">
Generated when a CRM clerk receives a record during the analysis phase of recovery.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8975cb5e-024f-40bf-acd7-c5af0abd88a0">OnCRMBegin</a>
</td>
<td align="left" width="63%">
Generated when a CRM clerk is starting, either due to a client registering a compensator or during recovery.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f1a91d24-0a78-4d4f-a686-817d0609e2b1">OnCRMCheckpoint</a>
</td>
<td align="left" width="63%">
Generated when a CRM checkpoint occurs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76b87452-fa29-49f7-acc8-2ae2039757b0">OnCRMCommit</a>
</td>
<td align="left" width="63%">
Generated when CRM clerk receives a commit notification to pass on to the CRM compensator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e93e5548-b833-43a9-a73e-1ccad9d252b6">OnCRMDeliver</a>
</td>
<td align="left" width="63%">
Generated when a CRM clerk delivers a record to a CRM compensator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8845fd4d-a1a8-40cf-9359-5a2900432f32">OnCRMDone</a>
</td>
<td align="left" width="63%">
Generated when CRM clerk is done processing transaction outcome notifications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92f2088b-4d74-4d33-9953-0f5229f6303c">OnCRMForce</a>
</td>
<td align="left" width="63%">
Generated when a CRM clerk receives a request to force log records to disk, either from the CRM worker or from the CRM compensator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e6c5bb1-aa99-434a-9376-c853b1fb1d12">OnCRMForget</a>
</td>
<td align="left" width="63%">
Generated when a CRM clerk receives a request to forget a log record, either from the CRM worker or from the CRM compensator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b1144b7c-097f-4a1c-b7d7-d71b8108625b">OnCRMIndoubt</a>
</td>
<td align="left" width="63%">
Generated when CRM clerk receives an in-doubt notification to pass on to the CRM compensator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16ecd4a5-6ca6-443d-ab03-f9ceb951ed13">OnCRMPrepare</a>
</td>
<td align="left" width="63%">
Generated when CRM clerk receives a prepare notification to pass on to the CRM compensator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/533148f3-ecb4-495c-81c4-c75db7284ded">OnCRMRecoveryDone</a>
</td>
<td align="left" width="63%">
Generated when CRM recovery is done.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac958f4b-1af4-4cfc-8fb4-92e89fdba771">OnCRMRecoveryStart</a>
</td>
<td align="left" width="63%">
Generated when CRM recovery has started.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e97b6cbf-1e78-475b-9dc7-baa4c05f1a6b">OnCRMRelease</a>
</td>
<td align="left" width="63%">
Generated when the CRM clerk is finished and releases its resource locks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/095452e3-a38d-4602-a925-8fa6445ddbc8">OnCRMWrite</a>
</td>
<td align="left" width="63%">
Generated when a CRM clerk receives a request to write a log record, either from the CRM worker or CRM compensator.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a>



<a href="https://msdn.microsoft.com/07f68734-a382-4fe5-86af-90805f61c68d">COM+ Instrumentation</a>
 

 

