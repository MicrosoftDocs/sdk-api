---
UID: NN:mswmdm.ISCPSecureQuery3
title: ISCPSecureQuery3
author: windows-driver-content
description: The ISCPSecureQuery3 interface extends ISCPSecureQuery2 by providing a set of new methods for retrieving the rights and making decision on a clear channel.
old-location: wmdm\iscpsecurequery3.htm
old-project: WMDM
ms.assetid: 3d600ae9-5d5b-48f6-a162-e52f78beb983
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: ISCPSecureQuery3, ISCPSecureQuery3 interface [windows Media Device Manager], ISCPSecureQuery3 interface [windows Media Device Manager],described, ISCPSecureQuery3Interface, mswmdm/ISCPSecureQuery3, wmdm.iscpsecurequery3
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
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
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mswmdm.h
api_name:
-	ISCPSecureQuery3
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

