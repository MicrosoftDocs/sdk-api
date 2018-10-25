---
UID: NN:comsvcs.IComTransactionEvents
title: IComTransactionEvents
author: windows-sdk-content
description: Notifies the subscriber if the Microsoft Distributed Transaction Coordinator (DTC) transaction starts, commits, or aborts.
old-location: cos\icomtransactionevents.htm
tech.root: cossdk
ms.assetid: f28a0ef5-1c9a-4fdc-bb10-2c381f22f5e3
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IComTransactionEvents, IComTransactionEvents interface [COM+], IComTransactionEvents interface [COM+],described, _dtc_IComTransactionEvents, comsvcs/IComTransactionEvents, cos.icomtransactionevents
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
 - IComTransactionEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComTransactionEvents interface


## -description


Notifies the subscriber if the Microsoft Distributed Transaction Coordinator (DTC) transaction starts, commits, or aborts. The subscriber is also notified when the resource manager retrieves prepare information from the transaction manager. The events are published to the subscriber using the <a href="https://msdn.microsoft.com/en-us/library/ms679237(v=VS.85).aspx">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComTransactionEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IComTransactionEvents</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>IComTransactionEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms679236(v=VS.85).aspx">OnTransactionAbort</a>
</td>
<td align="left" width="63%">
Generated when a transaction aborts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686452(v=VS.85).aspx">OnTransactionCommit</a>
</td>
<td align="left" width="63%">
Generated when a transaction commits.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms685190(v=VS.85).aspx">OnTransactionPrepare</a>
</td>
<td align="left" width="63%">
Generated when the prepare phase of the two-phase commit protocol of the transaction is completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms687782(v=VS.85).aspx">OnTransactionStart</a>
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
 

 

