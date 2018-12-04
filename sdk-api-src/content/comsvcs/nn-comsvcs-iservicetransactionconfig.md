---
UID: NN:comsvcs.IServiceTransactionConfig
title: IServiceTransactionConfig
author: windows-sdk-content
description: Configures the transaction services for the work that is done when calling either CoCreateActivity or CoEnterServiceDomain.
old-location: cos\iservicetransactionconfig.htm
tech.root: cossdk
ms.assetid: 7f31c590-8290-4556-9fcf-e27db01bad93
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IServiceTransactionConfig, IServiceTransactionConfig interface [COM+], IServiceTransactionConfig interface [COM+],described, _cos_IServiceTransactionConfig, comsvcs/IServiceTransactionConfig, cos.iservicetransactionconfig
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IServiceTransactionConfig interface


## -description


Configures the transaction services for the work that is done when calling either <a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a> or <a href="https://msdn.microsoft.com/84640b3b-1f43-4bec-abf6-c295cfb3da8b">CoEnterServiceDomain</a>. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServiceTransactionConfig</b> interface inherits from <a href="https://msdn.microsoft.com/e4740bf4-51b1-474f-9637-7c5d78f0def5">IServiceTransactionConfigBase</a>. <b>IServiceTransactionConfig</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/be4fa727-962e-4254-8615-58f6ced15fc3">ConfigureBYOT</a>
</td>
<td align="left" width="63%">
Enables you to configure the transaction that you use when you bring your own transaction.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/492875cb-52a7-484f-810e-bd838373b603">Bring Your Own Transaction (BYOT)</a>



<a href="https://msdn.microsoft.com/40eccce1-a362-4adc-8060-f6923b9162c9">COM+ Transactions</a>



<a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a>



<a href="https://msdn.microsoft.com/e4740bf4-51b1-474f-9637-7c5d78f0def5">IServiceTransactionConfigBase</a>
 

 

