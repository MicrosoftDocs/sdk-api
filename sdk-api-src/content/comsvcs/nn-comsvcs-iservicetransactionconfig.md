---
UID: NN:comsvcs.IServiceTransactionConfig
title: IServiceTransactionConfig
author: windows-sdk-content
description: Configures the transaction services for the work that is done when calling either CoCreateActivity or CoEnterServiceDomain.
old-location: cos\iservicetransactionconfig.htm
tech.root: cossdk
ms.assetid: 7f31c590-8290-4556-9fcf-e27db01bad93
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IServiceTransactionConfig, IServiceTransactionConfig interface [COM+], IServiceTransactionConfig interface [COM+],described, _cos_IServiceTransactionConfig, comsvcs/IServiceTransactionConfig, cos.iservicetransactionconfig
ms.prod: windows
ms.technology: windows-sdk
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


Configures the transaction services for the work that is done when calling either <a href="https://msdn.microsoft.com/en-us/library/ms679553(v=VS.85).aspx">CoCreateActivity</a> or <a href="https://msdn.microsoft.com/en-us/library/ms683559(v=VS.85).aspx">CoEnterServiceDomain</a>. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServiceTransactionConfig</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/ms687570(v=VS.85).aspx">IServiceTransactionConfigBase</a>. <b>IServiceTransactionConfig</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/ms686096(v=VS.85).aspx">ConfigureBYOT</a>
</td>
<td align="left" width="63%">
Enables you to configure the transaction that you use when you bring your own transaction.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms681215(v=VS.85).aspx">Bring Your Own Transaction (BYOT)</a>



<a href="https://msdn.microsoft.com/en-us/library/ms680599(v=VS.85).aspx">COM+ Transactions</a>



<a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a>



<a href="https://msdn.microsoft.com/en-us/library/ms687570(v=VS.85).aspx">IServiceTransactionConfigBase</a>
 

 

