---
UID: NN:comsvcs.IObjPool
title: IObjPool (comsvcs.h)
description: Represents the key to each object in the transaction resource pool.
helpviewer_keywords: ["IObjPool","IObjPool interface [COM+]","IObjPool interface [COM+]","described","_cos_IObjPool","comsvcs/IObjPool","cos.iobjpool"]
old-location: cos\iobjpool.htm
tech.root: cos
ms.assetid: d3730a37-933b-4705-b787-4b8bb728a278
ms.date: 12/05/2018
ms.keywords: IObjPool, IObjPool interface [COM+], IObjPool interface [COM+],described, _cos_IObjPool, comsvcs/IObjPool, cos.iobjpool
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IObjPool
 - comsvcs/IObjPool
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
 - IObjPool
---

# IObjPool interface


## -description

Represents the key to each object in the transaction resource pool.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IObjPool</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IObjPool</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IObjPool</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjpool-putendtx">PutEndTx</a>
</td>
<td align="left" width="63%">
Destroys the pooled object when the transaction ends.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-itransactionproperty">ITransactionProperty</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-itransactionresourcepool">ITransactionResourcePool</a>