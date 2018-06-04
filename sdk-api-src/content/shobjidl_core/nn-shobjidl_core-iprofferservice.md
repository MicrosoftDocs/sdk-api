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

# IProfferService interface


## -description


Exposes a general mechanism for objects to offer services to other objects on the same host.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IProfferService</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IProfferService</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IProfferService</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ebd6003d-ac8f-4e5e-9d90-c7e5688bedaa">ProfferService</a>
</td>
<td align="left" width="63%">
Makes a service available to other objects on the same host.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90868bbb-6fcd-4de1-a853-524542b74701">RevokeService</a>
</td>
<td align="left" width="63%">
Makes a service unavailable that had previously been available to other objects through <a href="https://msdn.microsoft.com/ebd6003d-ac8f-4e5e-9d90-c7e5688bedaa">IProfferService::ProfferService</a>.
		

</td>
</tr>
</table> 


## -remarks



Objects that expose a service first call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on their host for this interface, then execute <a href="https://msdn.microsoft.com/ebd6003d-ac8f-4e5e-9d90-c7e5688bedaa">IProfferService::ProfferService</a>.
			




## -see-also




<a href="https://msdn.microsoft.com/e688136e-e06b-46ba-bec9-b8db2f9c468d">IObjectWithSite</a>
 

 

