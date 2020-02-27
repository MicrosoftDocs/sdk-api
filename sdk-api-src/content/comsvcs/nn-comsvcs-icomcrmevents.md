---
UID: NN:comsvcs.IComCRMEvents
title: IComCRMEvents (comsvcs.h)
description: Notifies the subscriber about activities of the Compensating Resource Manager (CRM) feature of Component Services.
old-location: cos\icomcrmevents.htm
tech.root: cossdk
ms.assetid: 720beffb-8fb5-4c87-9bcf-6db214543b01
ms.date: 12/05/2018
ms.keywords: IComCRMEvents, IComCRMEvents interface [COM+], IComCRMEvents interface [COM+],described, _dtc_icomcrmevents, comsvcs/IComCRMEvents, cos.icomcrmevents
f1_keywords:
- comsvcs/IComCRMEvents
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComCRMEvents interface


## -description


Notifies the subscriber about activities of the Compensating Resource Manager (CRM) feature of Component Services. The events are published to the subscriber using the <a href="https://docs.microsoft.com/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComCRMEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComCRMEvents</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomcrmevents-oncrmabort">OnCRMAbort</a>
</td>
<td align="left" width="63%">
Generated when CRM clerk receives an abort notification to pass on to the CRM compensator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomcrmevents-oncrmanalyze">OnCRMAnalyze</a>
</td>
<td align="left" width="63%">
Generated when a CRM clerk receives a record during the analysis phase of recovery.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomcrmevents-oncrmbegin">OnCRMBegin</a>
</td>
<td align="left" width="63%">
Generated when a CRM clerk is starting, either due to a client registering a compensator or during recovery.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomcrmevents-oncrmcheckpoint">OnCRMCheckpoint</a>
</td>
<td align="left" width="63%">
Generated when a CRM checkpoint occurs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomcrmevents-oncrmcommit">OnCRMCommit</a>
</td>
<td align="left" width="63%">
Generated when CRM clerk receives a commit notification to pass on to the CRM compensator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomcrmevents-oncrmdeliver">OnCRMDeliver</a>
</td>
<td align="left" width="63%">
Generated when a CRM clerk delivers a record to a CRM compensator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomcrmevents-oncrmdone">OnCRMDone</a>
</td>
<td align="left" width="63%">
Generated when CRM clerk is done processing transaction outcome notifications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomcrmevents-oncrmforce">OnCRMForce</a>
</td>
<td align="left" width="63%">
Generated when a CRM clerk receives a request to force log records to disk, either from the CRM worker or from the CRM compensator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomcrmevents-oncrmforget">OnCRMForget</a>
</td>
<td align="left" width="63%">
Generated when a CRM clerk receives a request to forget a log record, either from the CRM worker or from the CRM compensator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomcrmevents-oncrmindoubt">OnCRMIndoubt</a>
</td>
<td align="left" width="63%">
Generated when CRM clerk receives an in-doubt notification to pass on to the CRM compensator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomcrmevents-oncrmprepare">OnCRMPrepare</a>
</td>
<td align="left" width="63%">
Generated when CRM clerk receives a prepare notification to pass on to the CRM compensator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomcrmevents-oncrmrecoverydone">OnCRMRecoveryDone</a>
</td>
<td align="left" width="63%">
Generated when CRM recovery is done.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomcrmevents-oncrmrecoverystart">OnCRMRecoveryStart</a>
</td>
<td align="left" width="63%">
Generated when CRM recovery has started.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomcrmevents-oncrmrelease">OnCRMRelease</a>
</td>
<td align="left" width="63%">
Generated when the CRM clerk is finished and releases its resource locks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomcrmevents-oncrmwrite">OnCRMWrite</a>
</td>
<td align="left" width="63%">
Generated when a CRM clerk receives a request to write a log record, either from the CRM worker or CRM compensator.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>
 

 

