---
UID: NN:comsvcs.IComQCEvents
title: IComQCEvents (comsvcs.h)
description: Notifies the subscriber if a queued message is created, de-queued, or moved to a retry or dead letter queue.
helpviewer_keywords: ["IComQCEvents","IComQCEvents interface [COM+]","IComQCEvents interface [COM+]","described","_dtc_IComQCEvents","comsvcs/IComQCEvents","cos.icomqcevents"]
old-location: cos\icomqcevents.htm
tech.root: cos
ms.assetid: d7c8220d-a302-4f95-b0b6-8d47f9f27da7
ms.date: 12/05/2018
ms.keywords: IComQCEvents, IComQCEvents interface [COM+], IComQCEvents interface [COM+],described, _dtc_IComQCEvents, comsvcs/IComQCEvents, cos.icomqcevents
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IComQCEvents
 - comsvcs/IComQCEvents
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IComQCEvents
---

# IComQCEvents interface


## -description

Notifies the subscriber if a queued message is created, de-queued, or moved to a retry or dead letter queue. The events are published to the subscriber using the <a href="https://docs.microsoft.com/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComQCEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComQCEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComQCEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomqcevents-onqcmovetodeadqueue">OnQCMoveToDeadQueue</a>
</td>
<td align="left" width="63%">
Generated when a message is moved to the dead letter queue and cannot be delivered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomqcevents-onqcmovetoretryqueue">OnQCMoveToReTryQueue</a>
</td>
<td align="left" width="63%">
Generated when a message is moved to a queued components retry queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomqcevents-onqcplayback">OnQCPlayback</a>
</td>
<td align="left" width="63%">
Generated when a messages contents are replayed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomqcevents-onqcqueueopen">OnQCQueueOpen</a>
</td>
<td align="left" width="63%">
Generated when a queued components queue is opened.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomqcevents-onqcreceive">OnQCReceive</a>
</td>
<td align="left" width="63%">
Generated when a message is successfully de-queued even though the queued components service might find something wrong with the contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomqcevents-onqcreceivefail">OnQCReceiveFail</a>
</td>
<td align="left" width="63%">
Generated when the receive message fails.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomqcevents-onqcrecord">OnQCRecord</a>
</td>
<td align="left" width="63%">
Generated when the queued components recorder creates the queued message.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--queued-components">COM+ Queued Components</a>

