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

# IADsDeleteOps interface


## -description


The <b>IADsDeleteOps</b> interface specifies a method an object can use to delete itself from the underlying directory. For a container object, the method deletes its children and the entire subtree.

The interface is designed to offer features that complement  <a href="https://msdn.microsoft.com/6c1d6c7c-e003-47f9-adfa-4a753fb3e9b2">IADsContainer</a>. To remove an object from the directory store, request its parent object to perform the operation. That amounts to calling the  <a href="https://msdn.microsoft.com/2f3873e0-376e-4212-a28d-bd9bc112f6cf">IADsContainer::Delete</a> method on the contained object. When the object also implements the <b>IADsDeleteOps</b> interface, you can instruct the object to remove itself, and all the contained objects, by calling the <a href="https://msdn.microsoft.com/53685f60-9adf-40f0-b6d3-e59a0435f744">IADsDeleteOps::DeleteObject</a> method directly on the object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsDeleteOps</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IADsDeleteOps</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IADsDeleteOps</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/53685f60-9adf-40f0-b6d3-e59a0435f744">DeleteObject</a>
</td>
<td align="left" width="63%">
Deletes the object from the directory.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/87027c25-e3c9-4bad-8df3-cb6205e40ef6">Access Control and Object Deletion</a>



<a href="https://msdn.microsoft.com/6c1d6c7c-e003-47f9-adfa-4a753fb3e9b2">IADsContainer</a>



<a href="https://msdn.microsoft.com/2f3873e0-376e-4212-a28d-bd9bc112f6cf">IADsContainer::Delete</a>



<a href="https://msdn.microsoft.com/821b71c2-e9f5-4ca8-9366-e8a3f1907670">IADsDeleteOps Interface</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

