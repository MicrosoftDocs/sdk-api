---
UID: NN:comsvcs.IServicePoolConfig
title: IServicePoolConfig (comsvcs.h)
description: Used to configure an object pool.
helpviewer_keywords: ["IServicePoolConfig","IServicePoolConfig interface [COM+]","IServicePoolConfig interface [COM+]","described","_cos_IServicePoolConfig","comsvcs/IServicePoolConfig","cos.iservicepoolconfig"]
old-location: cos\iservicepoolconfig.htm
tech.root: cossdk
ms.assetid: 026abfcf-56b5-4821-a9d4-37beeb3a052b
ms.date: 12/05/2018
ms.keywords: IServicePoolConfig, IServicePoolConfig interface [COM+], IServicePoolConfig interface [COM+],described, _cos_IServicePoolConfig, comsvcs/IServicePoolConfig, cos.iservicepoolconfig
f1_keywords:
- comsvcs/IServicePoolConfig
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
- IServicePoolConfig
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IServicePoolConfig interface


## -description


Used to configure an object pool.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServicePoolConfig</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IServicePoolConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IServicePoolConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iservicepoolconfig-get_classfactory">get_ClassFactory</a>
</td>
<td align="left" width="63%">
Retrieves a class factory for the pooled objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iservicepoolconfig-get_creationtimeout">get_CreationTimeout</a>
</td>
<td align="left" width="63%">
Retrieves the time-out interval for activating a pooled object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iservicepoolconfig-get_maxpoolsize">get_MaxPoolSize</a>
</td>
<td align="left" width="63%">
Retrieves the maximum number of objects in the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iservicepoolconfig-get_minpoolsize">get_MinPoolSize</a>
</td>
<td align="left" width="63%">
Retrieves the minimum number of objects in the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iservicepoolconfig-put_classfactory">get_TransactionAffinity</a>
</td>
<td align="left" width="63%">
Determines whether objects involved in transactions are held until the transaction completes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iservicepoolconfig-put_classfactory">put_ClassFactory</a>
</td>
<td align="left" width="63%">
Sets a class factory for the pooled objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iservicepoolconfig-put_creationtimeout">put_CreationTimeout</a>
</td>
<td align="left" width="63%">
Sets the time-out interval for activating a pooled object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iservicepoolconfig-put_maxpoolsize">put_MaxPoolSize</a>
</td>
<td align="left" width="63%">
Sets the maximum number of objects in the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iservicepoolconfig-put_minpoolsize">put_MinPoolSize</a>
</td>
<td align="left" width="63%">
Sets the minimum number of objects in the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iservicepoolconfig-put_transactionaffinity">put_TransactionAffinity</a>
</td>
<td align="left" width="63%">
Sets whether objects involved in transactions are held until the transaction completes.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iservicepool">IServicePool</a>
 

 

