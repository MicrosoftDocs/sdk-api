---
UID: NN:comsvcs.IComLTxEvents
title: IComLTxEvents
author: windows-sdk-content
description: Notifies the subscriber of events that relate to COM+ transactions.
old-location: cos\icomltxevents.htm
tech.root: cossdk
ms.assetid: 8be6dddb-ed57-4715-8933-8a0e478095c8
ms.author: windowssdkdev
ms.date: 08/31/2018
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
 - IComLTxEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComLTxEvents interface


## -description


Notifies the subscriber of events that relate to COM+ transactions. The events are published to the subscriber using the <a href="https://msdn.microsoft.com/en-us/library/ms679237(v=VS.85).aspx">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComLTxEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IComLTxEvents</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/ms681213(v=VS.85).aspx">OnLtxTransactionAbort</a>
</td>
<td align="left" width="63%">
Generated when a transaction is aborted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686423(v=VS.85).aspx">OnLtxTransactionCommit</a>
</td>
<td align="left" width="63%">
Generated when a transaction is committed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms679562(v=VS.85).aspx">OnLtxTransactionPrepare</a>
</td>
<td align="left" width="63%">
Generated when COM+ receives a prepare notification for a transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms684391(v=VS.85).aspx">OnLtxTransactionPromote</a>
</td>
<td align="left" width="63%">
Generated when a transaction is promoted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms678925(v=VS.85).aspx">OnLtxTransactionStart</a>
</td>
<td align="left" width="63%">
Generated when a transaction is started.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms679237(v=VS.85).aspx">COM+ Events</a>



<a href="https://msdn.microsoft.com/en-us/library/ms678896(v=VS.85).aspx">COM+ Instrumentation</a>
 

 

