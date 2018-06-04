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

# ISharedProperty interface


## -description


Exposes property methods that you can use to set or retrieve the value of a shared property. A shared property can contain any data type that can be represented by a <b>Variant</b>.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISharedProperty</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ISharedProperty</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISharedProperty</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b8e297c-db65-41b2-a5ee-3a63a4ff31fb">get_Value</a>
</td>
<td align="left" width="63%">
Retrieves the value of a shared property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d193990c-a804-41aa-81d7-75aced274f73">put_Value</a>
</td>
<td align="left" width="63%">
Sets the value of a shared property.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e7f23c83-40d3-4b08-a185-cd6e3260e0a9">ISharedPropertyGroup</a>



<a href="https://msdn.microsoft.com/71c0a1de-5ea5-4496-b0e9-56d0cc8129a9">ISharedPropertyGroupManager</a>
 

 

