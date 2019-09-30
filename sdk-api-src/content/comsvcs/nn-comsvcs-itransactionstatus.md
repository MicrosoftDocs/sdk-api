---
UID: NN:comsvcs.ITransactionStatus
title: ITransactionStatus (comsvcs.h)
author: windows-sdk-content
description: Used to discover the status of the transaction that is completed by the call to CoLeaveServiceDomain when CServiceConfig is configured to use transactions in the call to CoEnterServiceDomain.
old-location: cos\itransactionstatus.htm
tech.root: cossdk
ms.assetid: df5eba93-6db7-478c-b6d7-831c20398d66
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITransactionStatus, ITransactionStatus interface [COM+], ITransactionStatus interface [COM+],described, _cos_ITransactionStatus, comsvcs/ITransactionStatus, cos.itransactionstatus
ms.topic: interface
f1_keywords: 
 - "comsvcs/ITransactionStatus"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ITransactionStatus
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITransactionStatus interface


## -description


Used to discover the status of the transaction that is completed by the call to <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-coleaveservicedomain">CoLeaveServiceDomain</a> when <a href="https://docs.microsoft.com/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> is configured to use transactions in the call to <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITransactionStatus</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITransactionStatus</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITransactionStatus</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-itransactionstatus-gettransactionstatus">GetTransactionStatus</a>
</td>
<td align="left" width="63%">
Retrieves the transaction status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-itransactionstatus-settransactionstatus">SetTransactionStatus</a>
</td>
<td align="left" width="63%">
Sets the transaction status to either committed or aborted. Do not use this method. It is used only internally by COM+.


</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--transactions">COM+ Transactions</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-coleaveservicedomain">CoLeaveServiceDomain</a>
 

 

