---
UID: NN:comsvcs.IServiceTransactionConfigBase
title: IServiceTransactionConfigBase
author: windows-sdk-content
description: Configures the transaction services for the work that is done when calling either CoCreateActivity or CoEnterServiceDomain.
old-location: cos\iservicetransactionconfigbase.htm
old-project: cossdk
ms.assetid: e4740bf4-51b1-474f-9637-7c5d78f0def5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IServiceTransactionConfigBase, IServiceTransactionConfigBase interface [COM+], IServiceTransactionConfigBase interface [COM+],described, _cos_IServiceTransactionConfigBase, comsvcs/IServiceTransactionConfigBase, cos.iservicetransactionconfigbase
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: comsvcs.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IServiceTransactionConfigBase
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IServiceTransactionConfigBase interface


## -description


Configures the transaction services for the work that is done when calling either <a href="https://msdn.microsoft.com/en-us/library/ms679553(v=VS.85).aspx">CoCreateActivity</a> or <a href="https://msdn.microsoft.com/en-us/library/ms683559(v=VS.85).aspx">CoEnterServiceDomain</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServiceTransactionConfigBase</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IServiceTransactionConfigBase</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>IServiceTransactionConfigBase</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms688489(v=VS.85).aspx">BringYourOwnTransaction</a>
</td>
<td align="left" width="63%">
Enables you to run the enclosed code in an existing transaction that you provide.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms683501(v=VS.85).aspx">ConfigureTransaction</a>
</td>
<td align="left" width="63%">
Configures how transactions are used in the enclosed work.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms681162(v=VS.85).aspx">IsolationLevel</a>
</td>
<td align="left" width="63%">
Sets the isolation level of the transactions.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms687732(v=VS.85).aspx">NewTransactionDescription</a>
</td>
<td align="left" width="63%">
Sets the name that is used when transaction statistics are displayed.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms683606(v=VS.85).aspx">TransactionTimeout</a>
</td>
<td align="left" width="63%">
Sets the transaction time-out for a new transaction.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms681215(v=VS.85).aspx">Bring Your Own Transaction (BYOT)</a>



<a href="https://msdn.microsoft.com/en-us/library/ms680599(v=VS.85).aspx">COM+ Transactions</a>



<a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a>
 

 

