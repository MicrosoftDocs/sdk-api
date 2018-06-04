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

# IManagedActivationEvents interface


## -description


Used to create and destroy stubs for managed objects within the current COM+ context.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IManagedActivationEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IManagedActivationEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IManagedActivationEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a2ba7ece-ac17-42fb-b22f-976ad849eca5">CreateManagedStub</a>
</td>
<td align="left" width="63%">
Creates a stub for a managed object within the current COM+ context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aabc8192-d499-441e-be5d-9a51108bd344">DestroyManagedStub</a>
</td>
<td align="left" width="63%">
Destroys a stub that was created by <a href="https://msdn.microsoft.com/a2ba7ece-ac17-42fb-b22f-976ad849eca5">CreateManagedStub</a>.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/cffd18c4-6e37-447b-b749-64793711ea56">GetManagedExtensions</a>



<a href="https://msdn.microsoft.com/7fa5f76e-df07-41b3-8fb0-62b84a034aa5">IManagedObjectInfo</a>



<a href="https://msdn.microsoft.com/6c29bbe0-840f-4eaf-97ad-40b0f89cadfd">IManagedPoolAction</a>



<a href="https://msdn.microsoft.com/04853859-5d85-4b88-9e1b-422e3454fd3f">IManagedPooledObj</a>
 

 

