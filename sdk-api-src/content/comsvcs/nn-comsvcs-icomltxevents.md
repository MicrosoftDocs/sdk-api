---
UID: NN:comsvcs.IComLTxEvents
title: IComLTxEvents
author: windows-sdk-content
description: Notifies the subscriber of events that relate to COM+ transactions.
old-location: cos\icomltxevents.htm
old-project: cossdk
ms.assetid: 8be6dddb-ed57-4715-8933-8a0e478095c8
ms.author: windowssdkdev
ms.date: 06/18/2018
ms.keywords: IComLTxEvents, IComLTxEvents interface [COM+], IComLTxEvents interface [COM+],described, comsvcs/IComLTxEvents, cos.icomltxevents
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IComLTxEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComLTxEvents interface


## -description


Notifies the subscriber of events that relate to COM+ transactions. The events are published to the subscriber using the <a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComLTxEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IComLTxEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComLTxEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49117b74-e84b-497c-ae13-6037e8243e79">OnLtxTransactionAbort</a>
</td>
<td align="left" width="63%">
Generated when a transaction is aborted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3462a79-6056-4a57-b971-78d8b4bd2a70">OnLtxTransactionCommit</a>
</td>
<td align="left" width="63%">
Generated when a transaction is committed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31915d4c-7ac0-406b-b2d2-ab96b317be3f">OnLtxTransactionPrepare</a>
</td>
<td align="left" width="63%">
Generated when COM+ receives a prepare notification for a transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9cd9927c-355c-4d9f-b679-278e4b6897e1">OnLtxTransactionPromote</a>
</td>
<td align="left" width="63%">
Generated when a transaction is promoted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d063e3f-d7f8-45b1-995f-29903c42ec37">OnLtxTransactionStart</a>
</td>
<td align="left" width="63%">
Generated when a transaction is started.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a>



<a href="https://msdn.microsoft.com/07f68734-a382-4fe5-86af-90805f61c68d">COM+ Instrumentation</a>
 

 

