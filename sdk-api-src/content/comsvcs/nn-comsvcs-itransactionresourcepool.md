---
UID: NN:comsvcs.ITransactionResourcePool
title: ITransactionResourcePool (comsvcs.h)
description: Maintains a list of pooled objects, keyed by IObjPool, that are used until the transaction completes.
old-location: cos\itransactionresourcepool.htm
tech.root: cossdk
ms.assetid: bf7ca849-6025-4358-bf2d-629d80e06a04
ms.date: 12/05/2018
ms.keywords: ITransactionResourcePool, ITransactionResourcePool interface [COM+], ITransactionResourcePool interface [COM+],described, _cos_ITransactionResourcePool, comsvcs/ITransactionResourcePool, cos.itransactionresourcepool
ms.topic: interface
f1_keywords:
- comsvcs/ITransactionResourcePool
dev_langs:
- c++
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- ComSvcs.h
api_name:
- ITransactionResourcePool
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITransactionResourcePool interface


## -description


Maintains a list of pooled objects, keyed by <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iobjpool">IObjPool</a>, that are used until the transaction completes.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITransactionResourcePool</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITransactionResourcePool</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITransactionResourcePool</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-itransactionresourcepool-getresource">GetResource</a>
</td>
<td align="left" width="63%">
Retrieves an object from the list of pooled objects.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-itransactionresourcepool-putresource">PutResource</a>
</td>
<td align="left" width="63%">
Adds an object to the list of pooled objects.


</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iobjpool">IObjPool</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-itransactionproperty">ITransactionProperty</a>
 

 

