---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

