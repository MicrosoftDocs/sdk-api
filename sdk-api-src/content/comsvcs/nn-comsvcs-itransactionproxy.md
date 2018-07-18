---
UID: NN:comsvcs.ITransactionProxy
title: ITransactionProxy
author: windows-sdk-content
description: Provides a way for a COM+ transaction context to work with a non-DTC transaction.
old-location: cos\itransactionproxy.htm
old-project: cossdk
ms.assetid: 58d40456-fd4f-4690-a679-3fa58b2f3cda
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: ITransactionProxy, ITransactionProxy interface [COM+], ITransactionProxy interface [COM+],described, comsvcs/ITransactionProxy, cos.itransactionproxy
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
 - ITransactionProxy
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ITransactionProxy interface


## -description


Provides a way for a COM+ transaction context to work with a non-DTC transaction.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITransactionProxy</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITransactionProxy</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITransactionProxy</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/15ad94ac-311f-486d-988b-9071396f6e34">Abort</a>
</td>
<td align="left" width="63%">
Aborts the transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439717">Commit</a>
</td>
<td align="left" width="63%">
Commits the transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd837082-881e-4f7e-b71e-c0f6068e3cdb">CreateVoter</a>
</td>
<td align="left" width="63%">
Provides a ballot so that a COM+ transaction context can vote on the transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8045989b-7b66-4340-a06e-4b4102d09784">GetIdentifier</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of the non-DTC transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a2b0e99a-0d35-4103-b7a0-407d09a2746e">GetIsolationLevel</a>
</td>
<td align="left" width="63%">
Retrieves the isolation level of the non-DTC transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c642d329-c996-4207-bdcf-7c79d955b2c4">IsReusable</a>
</td>
<td align="left" width="63%">
Indicates whether the non-DTC transaction context can be reused for multiple transactions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/861103b4-b5fa-4543-b26b-ad0c89d4473d">Promote</a>
</td>
<td align="left" width="63%">
Promotes a non-DTC transaction to a DTC transaction.

</td>
</tr>
</table> 

