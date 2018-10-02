---
UID: NN:comsvcs.IComTransaction2Events
title: IComTransaction2Events
author: windows-sdk-content
description: Notifies the subscriber if a Microsoft Distributed Transaction Coordinator (DTC) transaction starts, commits, or aborts. The subscriber is also notified when the transaction is in the prepare phase of the two-phase commit protocol.
old-location: cos\icomtransaction2events.htm
tech.root: cossdk
ms.assetid: 103776c8-1cdc-46a5-a2ce-54163726e602
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IComTransaction2Events, IComTransaction2Events interface [COM+], IComTransaction2Events interface [COM+],described, _dtc_icomtransaction2events, comsvcs/IComTransaction2Events, cos.icomtransaction2events
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
 - IComTransaction2Events
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComTransaction2Events interface


## -description


Notifies the subscriber if a Microsoft Distributed Transaction Coordinator (DTC) transaction starts, commits, or aborts. The subscriber is also notified when the transaction is in the prepare phase of the two-phase commit protocol. The events are published to the subscriber using the <a href="https://msdn.microsoft.com/en-us/library/ms679237(v=VS.85).aspx">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComTransaction2Events</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IComTransaction2Events</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/ms684160(v=VS.85).aspx">OnTransactionAbort2</a>
</td>
<td align="left" width="63%">
Generated when a transaction aborts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms687601(v=VS.85).aspx">OnTransactionCommit2</a>
</td>
<td align="left" width="63%">
Generated when a transaction commits.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms679214(v=VS.85).aspx">OnTransactionPrepare2</a>
</td>
<td align="left" width="63%">
Generated when the transaction is in the prepare phase of the commit protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686449(v=VS.85).aspx">OnTransactionStart2</a>
</td>
<td align="left" width="63%">
Generated when a Microsoft Distributed Transaction Coordinator (DTC) transaction starts.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms679237(v=VS.85).aspx">COM+ Events</a>



<a href="https://msdn.microsoft.com/en-us/library/ms678896(v=VS.85).aspx">COM+ Instrumentation</a>



<a href="https://msdn.microsoft.com/en-us/library/ms680599(v=VS.85).aspx">COM+ Transactions</a>
 

 

