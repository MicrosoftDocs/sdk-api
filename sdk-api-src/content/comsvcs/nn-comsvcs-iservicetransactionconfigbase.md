---
UID: NN:comsvcs.IServiceTransactionConfigBase
title: IServiceTransactionConfigBase (comsvcs.h)
description: Configures the transaction services for the work that is done when calling either CoCreateActivity or CoEnterServiceDomain.
helpviewer_keywords: ["IServiceTransactionConfigBase","IServiceTransactionConfigBase interface [COM+]","IServiceTransactionConfigBase interface [COM+]","described","_cos_IServiceTransactionConfigBase","comsvcs/IServiceTransactionConfigBase","cos.iservicetransactionconfigbase"]
old-location: cos\iservicetransactionconfigbase.htm
tech.root: cos
ms.assetid: e4740bf4-51b1-474f-9637-7c5d78f0def5
ms.date: 12/05/2018
ms.keywords: IServiceTransactionConfigBase, IServiceTransactionConfigBase interface [COM+], IServiceTransactionConfigBase interface [COM+],described, _cos_IServiceTransactionConfigBase, comsvcs/IServiceTransactionConfigBase, cos.iservicetransactionconfigbase
req.header: comsvcs.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IServiceTransactionConfigBase
 - comsvcs/IServiceTransactionConfigBase
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
 - IServiceTransactionConfigBase
---

# IServiceTransactionConfigBase interface


## -description

Configures the transaction services for the work that is done when calling either <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a> or <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServiceTransactionConfigBase</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IServiceTransactionConfigBase</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
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
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iservicetransactionconfigbase-bringyourowntransaction">BringYourOwnTransaction</a>
</td>
<td align="left" width="63%">
Enables you to run the enclosed code in an existing transaction that you provide.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iservicetransactionconfigbase-configuretransaction">ConfigureTransaction</a>
</td>
<td align="left" width="63%">
Configures how transactions are used in the enclosed work.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iservicetransactionconfigbase-isolationlevel">IsolationLevel</a>
</td>
<td align="left" width="63%">
Sets the isolation level of the transactions.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iservicetransactionconfigbase-newtransactiondescription">NewTransactionDescription</a>
</td>
<td align="left" width="63%">
Sets the name that is used when transaction statistics are displayed.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iservicetransactionconfigbase-transactiontimeout">TransactionTimeout</a>
</td>
<td align="left" width="63%">
Sets the transaction time-out for a new transaction.


</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/cossdk/bring-your-own-transaction--byot-">Bring Your Own Transaction (BYOT)</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--transactions">COM+ Transactions</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a>

