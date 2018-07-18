---
UID: NN:comsvcs.IServiceSysTxnConfig
title: IServiceSysTxnConfig
author: windows-sdk-content
description: Enables you to run a set of code in the scope of an existing transaction that you specify with a transaction proxy.
old-location: cos\iservicesystxnconfig.htm
old-project: cossdk
ms.assetid: 8e721496-fc2b-46b8-ae28-432da6c429e6
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IServiceSysTxnConfig, IServiceSysTxnConfig interface [COM+], IServiceSysTxnConfig interface [COM+],described, comsvcs/IServiceSysTxnConfig, cos.iservicesystxnconfig
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IServiceSysTxnConfig
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IServiceSysTxnConfig interface


## -description


Enables you to run a set of code in the scope of an existing transaction that you specify with a transaction proxy.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServiceSysTxnConfig</b> interface inherits from <a href="https://msdn.microsoft.com/7f31c590-8290-4556-9fcf-e27db01bad93">IServiceTransactionConfig</a>. <b>IServiceSysTxnConfig</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/6023e756-7797-489b-96fd-9cf2d9f2cb2b">ConfigureBYOTSysTxn</a>
</td>
<td align="left" width="63%">
Enables you to run the enclosed code in the scope of an existing transaction that you specify with a transaction proxy.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/7f31c590-8290-4556-9fcf-e27db01bad93">IServiceTransactionConfig</a>
 

 

