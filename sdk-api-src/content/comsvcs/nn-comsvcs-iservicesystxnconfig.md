---
UID: NN:comsvcs.IServiceSysTxnConfig
title: IServiceSysTxnConfig (comsvcs.h)
description: Enables you to run a set of code in the scope of an existing transaction that you specify with a transaction proxy.
helpviewer_keywords: ["IServiceSysTxnConfig","IServiceSysTxnConfig interface [COM+]","IServiceSysTxnConfig interface [COM+]","described","comsvcs/IServiceSysTxnConfig","cos.iservicesystxnconfig"]
old-location: cos\iservicesystxnconfig.htm
tech.root: cos
ms.assetid: 8e721496-fc2b-46b8-ae28-432da6c429e6
ms.date: 12/05/2018
ms.keywords: IServiceSysTxnConfig, IServiceSysTxnConfig interface [COM+], IServiceSysTxnConfig interface [COM+],described, comsvcs/IServiceSysTxnConfig, cos.iservicesystxnconfig
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IServiceSysTxnConfig
 - comsvcs/IServiceSysTxnConfig
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
 - IServiceSysTxnConfig
---

# IServiceSysTxnConfig interface


## -description

Enables you to run a set of code in the scope of an existing transaction that you specify with a transaction proxy.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServiceSysTxnConfig</b> interface inherits from <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicetransactionconfig">IServiceTransactionConfig</a>. <b>IServiceSysTxnConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IServiceSysTxnConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/comsvcs/nf-comsvcs-iservicesystxnconfig-configurebyotsystxn">ConfigureBYOTSysTxn</a>
</td>
<td align="left" width="63%">
Enables you to run the enclosed code in the scope of an existing transaction that you specify with a transaction proxy.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicetransactionconfig">IServiceTransactionConfig</a>