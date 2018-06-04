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

# IQueryContinue interface


## -description


Exposes a method that provides a simple, standard mechanism for objects to query a client for permission to continue an operation. Clients of <a href="https://msdn.microsoft.com/24ff171c-e9e2-4d62-8a8c-d62e5d7a92ad">IUserNotification</a>, for example, must pass an implementation of <b>IQueryContinue</b> to the <a href="https://msdn.microsoft.com/1f908581-9635-4090-9e52-1dfb9a206d38">IUserNotification::Show</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IQueryContinue</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IQueryContinue</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IQueryContinue</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9beabfc9-56b9-4778-8027-939aa986086a">QueryContinue</a>
</td>
<td align="left" width="63%">
Returns S_OK if the operation associated with the current instance of this interface should continue.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/24ff171c-e9e2-4d62-8a8c-d62e5d7a92ad">IUserNotification</a>
 

 

