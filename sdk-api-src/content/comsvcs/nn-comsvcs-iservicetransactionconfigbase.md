---
UID: NN:comsvcs.IServiceTransactionConfigBase
title: IServiceTransactionConfigBase
author: windows-sdk-content
description: Configures the transaction services for the work that is done when calling either CoCreateActivity or CoEnterServiceDomain.
old-location: cos\iservicetransactionconfigbase.htm
old-project: cossdk
ms.assetid: e4740bf4-51b1-474f-9637-7c5d78f0def5
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IServiceTransactionConfigBase, IServiceTransactionConfigBase interface [COM+], IServiceTransactionConfigBase interface [COM+],described, _cos_IServiceTransactionConfigBase, comsvcs/IServiceTransactionConfigBase, cos.iservicetransactionconfigbase
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IServiceTransactionConfigBase
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IServiceTransactionConfigBase interface


## -description


Configures the transaction services for the work that is done when calling either <a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a> or <a href="https://msdn.microsoft.com/84640b3b-1f43-4bec-abf6-c295cfb3da8b">CoEnterServiceDomain</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServiceTransactionConfigBase</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IServiceTransactionConfigBase</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/fcd65d90-8855-41e9-a22d-d2b1d46e98fa">BringYourOwnTransaction</a>
</td>
<td align="left" width="63%">
Enables you to run the enclosed code in an existing transaction that you provide.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8277b133-2c0c-4a21-b441-457efb285178">ConfigureTransaction</a>
</td>
<td align="left" width="63%">
Configures how transactions are used in the enclosed work.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4595239b-30e7-4b03-a2c7-7061cbf28bac">IsolationLevel</a>
</td>
<td align="left" width="63%">
Sets the isolation level of the transactions.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ecdc160b-168d-48f4-bbe3-46d654ee8607">NewTransactionDescription</a>
</td>
<td align="left" width="63%">
Sets the name that is used when transaction statistics are displayed.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87943fe9-ef88-49ae-96d0-99d1011478dc">TransactionTimeout</a>
</td>
<td align="left" width="63%">
Sets the transaction time-out for a new transaction.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/492875cb-52a7-484f-810e-bd838373b603">Bring Your Own Transaction (BYOT)</a>



<a href="https://msdn.microsoft.com/40eccce1-a362-4adc-8060-f6923b9162c9">COM+ Transactions</a>



<a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a>
 

 

