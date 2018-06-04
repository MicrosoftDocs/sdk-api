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

# ISCPSecureQuery3 interface


## -description



The <b>ISCPSecureQuery3</b> interface extends <a href="https://msdn.microsoft.com/fe5ae201-355d-4402-8d57-a721aecfdbde">ISCPSecureQuery2</a> by providing a set of new methods for retrieving the rights and making decision on a clear channel. These methods are more efficient because they do not involve encrypting and decrypting of parameters, which happens on a secure channel.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISCPSecureQuery3</b> interface inherits from <a href="https://msdn.microsoft.com/fe5ae201-355d-4402-8d57-a721aecfdbde">ISCPSecureQuery2</a>. <b>ISCPSecureQuery3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISCPSecureQuery3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab64b790-848a-4c7f-9bf9-4a9b40bcc9cb">GetRightsOnClearChannel</a>
</td>
<td align="left" width="63%">
Retrieves the rights on a clear channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63ffa9ec-b8bb-4d5d-b380-e4dbe0fc865a">MakeDecisionOnClearChannel</a>
</td>
<td align="left" width="63%">
Makes decisions on a clear channel.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d5f96629-26a1-4e83-a6a8-2d60c463f407">ISCPSecureQuery Interface</a>



<a href="https://msdn.microsoft.com/fe5ae201-355d-4402-8d57-a721aecfdbde">ISCPSecureQuery2 Interface</a>



<a href="https://msdn.microsoft.com/a3eecdb8-55a9-46e3-95d1-0fb9bd59f393">Interfaces for Secure Content Providers</a>
 

 

