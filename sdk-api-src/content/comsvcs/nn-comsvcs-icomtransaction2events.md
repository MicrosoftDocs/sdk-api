---
UID: NN:comsvcs.IComTransaction2Events
title: IComTransaction2Events
author: windows-driver-content
description: Notifies the subscriber if a Microsoft Distributed Transaction Coordinator (DTC) transaction starts, commits, or aborts. The subscriber is also notified when the transaction is in the prepare phase of the two-phase commit protocol.
old-location: cos\icomtransaction2events.htm
old-project: cossdk
ms.assetid: 103776c8-1cdc-46a5-a2ce-54163726e602
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: IComTransaction2Events, IComTransaction2Events interface [COM+], IComTransaction2Events interface [COM+], described, _dtc_icomtransaction2events, comsvcs/IComTransaction2Events, cos.icomtransaction2events
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IComTransaction2Events
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComTransaction2Events interface


## -description


Notifies the subscriber if a Microsoft Distributed Transaction Coordinator (DTC) transaction starts, commits, or aborts. The subscriber is also notified when the transaction is in the prepare phase of the two-phase commit protocol. The events are published to the subscriber using the <a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComTransaction2Events</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IComTransaction2Events</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComTransaction2Events</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c74410c-c9a0-4115-876b-4b4db798e54f">OnTransactionAbort2</a>
</td>
<td align="left" width="63%">
Generated when a transaction aborts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e68ba7be-876b-446a-8f82-a6e7af503b2c">OnTransactionCommit2</a>
</td>
<td align="left" width="63%">
Generated when a transaction commits.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b2ea10f-7b74-474e-bdf1-040d789fa7c9">OnTransactionPrepare2</a>
</td>
<td align="left" width="63%">
Generated when the transaction is in the prepare phase of the commit protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c7666b9f-5485-47da-9027-25668e73f73b">OnTransactionStart2</a>
</td>
<td align="left" width="63%">
Generated when a Microsoft Distributed Transaction Coordinator (DTC) transaction starts.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a>



<a href="https://msdn.microsoft.com/07f68734-a382-4fe5-86af-90805f61c68d">COM+ Instrumentation</a>



<a href="https://msdn.microsoft.com/40eccce1-a362-4adc-8060-f6923b9162c9">COM+ Transactions</a>
 

 

