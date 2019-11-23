---
UID: NN:comsvcs.IServiceTransactionConfig
title: IServiceTransactionConfig (comsvcs.h)

description: Configures the transaction services for the work that is done when calling either CoCreateActivity or CoEnterServiceDomain.
old-location: cos\iservicetransactionconfig.htm
tech.root: cossdk
ms.assetid: 7f31c590-8290-4556-9fcf-e27db01bad93

ms.date: 12/05/2018
ms.keywords: IServiceTransactionConfig, IServiceTransactionConfig interface [COM+], IServiceTransactionConfig interface [COM+],described, _cos_IServiceTransactionConfig, comsvcs/IServiceTransactionConfig, cos.iservicetransactionconfig
ms.topic: interface
f1_keywords: 
 - "comsvcs/IServiceTransactionConfig"
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
 - IServiceTransactionConfig
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IServiceTransactionConfig interface


## -description


Configures the transaction services for the work that is done when calling either <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a> or <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a>. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServiceTransactionConfig</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iservicetransactionconfigbase">IServiceTransactionConfigBase</a>. <b>IServiceTransactionConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IServiceTransactionConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iservicetransactionconfig-configurebyot">ConfigureBYOT</a>
</td>
<td align="left" width="63%">
Enables you to configure the transaction that you use when you bring your own transaction.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/bring-your-own-transaction--byot-">Bring Your Own Transaction (BYOT)</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--transactions">COM+ Transactions</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iservicetransactionconfigbase">IServiceTransactionConfigBase</a>
 

 

