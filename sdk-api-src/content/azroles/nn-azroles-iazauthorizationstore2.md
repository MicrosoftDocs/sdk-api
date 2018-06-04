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

# IAzAuthorizationStore2 interface


## -description


The <b>IAzAuthorizationStore2</b> interface inherits from the <a href="https://msdn.microsoft.com/f848cca6-3838-46bc-b1f4-d6eab5096046">AzAuthorizationStore</a> object and implements methods to create and open <a href="https://msdn.microsoft.com/58f0627e-fa92-4b3b-a0cd-7e437d451606">IAzApplication2</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzAuthorizationStore2</b> interface inherits from <a href="https://msdn.microsoft.com/f848cca6-3838-46bc-b1f4-d6eab5096046">AzAuthorizationStore</a> and <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>. <b>IAzAuthorizationStore2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAzAuthorizationStore2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9af40e4-9ed9-4b81-b808-315eef07a96d">CreateApplication2</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/58f0627e-fa92-4b3b-a0cd-7e437d451606">IAzApplication2</a> object by using the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8705ea59-2419-4af5-9cc2-591221e09073">OpenApplication2</a>
</td>
<td align="left" width="63%">
Opens the <a href="https://msdn.microsoft.com/58f0627e-fa92-4b3b-a0cd-7e437d451606">IAzApplication2</a> object by using the specified name.

</td>
</tr>
</table> 

