---
UID: NN:comsvcs.ITransactionResourcePool
title: ITransactionResourcePool
author: windows-sdk-content
description: Maintains a list of pooled objects, keyed by IObjPool, that are used until the transaction completes.
old-location: cos\itransactionresourcepool.htm
tech.root: cossdk
ms.assetid: bf7ca849-6025-4358-bf2d-629d80e06a04
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: ITransactionResourcePool, ITransactionResourcePool interface [COM+], ITransactionResourcePool interface [COM+],described, _cos_ITransactionResourcePool, comsvcs/ITransactionResourcePool, cos.itransactionresourcepool
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
 - ITransactionResourcePool
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITransactionResourcePool interface


## -description


Maintains a list of pooled objects, keyed by <a href="https://msdn.microsoft.com/d3730a37-933b-4705-b787-4b8bb728a278">IObjPool</a>, that are used until the transaction completes.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITransactionResourcePool</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITransactionResourcePool</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/68e71746-e3a1-4f33-a3b8-fa8bf9608776">GetResource</a>
</td>
<td align="left" width="63%">
Retrieves an object from the list of pooled objects.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e05f075-0fa8-4605-9f68-3ef7fc9f0132">PutResource</a>
</td>
<td align="left" width="63%">
Adds an object to the list of pooled objects.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d3730a37-933b-4705-b787-4b8bb728a278">IObjPool</a>



<a href="https://msdn.microsoft.com/602842ce-abb1-4830-99b3-d361d18ac074">ITransactionProperty</a>
 

 

