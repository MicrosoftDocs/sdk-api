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

# IGetSecurityCallContext interface


## -description


Retrieves a reference to an object created from the <a href="https://msdn.microsoft.com/e8ac05fb-6665-4e57-b64e-82d9799d29d4">SecurityCallContext</a> class that is associated with the current call.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGetSecurityCallContext</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IGetSecurityCallContext</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGetSecurityCallContext</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a386cf6-1f75-4915-8c89-e453c4ebdab8">GetSecurityClassContext</a>
</td>
<td align="left" width="63%">
Retrieves a reference to an object created from the <a href="https://msdn.microsoft.com/e8ac05fb-6665-4e57-b64e-82d9799d29d4">SecurityCallContext</a> class that is associated with the current call.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b82e32c0-840d-402e-90d5-ff678c51faf1">CoGetCallContext</a>



<a href="https://msdn.microsoft.com/cd96ef31-784f-40fa-beb5-92a88823326b">ISecurityCallContext</a>



<a href="https://msdn.microsoft.com/e8ac05fb-6665-4e57-b64e-82d9799d29d4">SecurityCallContext</a>
 

 

