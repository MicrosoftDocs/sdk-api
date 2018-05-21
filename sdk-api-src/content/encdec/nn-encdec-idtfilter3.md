---
UID: NN:encdec.IDTFilter3
title: IDTFilter3
author: windows-driver-content
description: The IDTFilter3 interface extends the IDTFilter2 interface and is exposed by the Decrypter/Detagger filter.
old-location: mstv\idtfilter3.htm
old-project: mstv
ms.assetid: 88e42006-c387-41b5-a013-e968da0d918b
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IDTFilter3, IDTFilter3 interface [Microsoft TV Technologies], IDTFilter3 interface [Microsoft TV Technologies],described, IDTFilter3Interface, encdec/IDTFilter3, mstv.idtfilter3
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: encdec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ProtType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	encdec.h
api_name:
-	IDTFilter3
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDTFilter3 interface


## -description



The <b>IDTFilter3</b> interface extends the <a href="https://msdn.microsoft.com/351c77ec-fb0c-4780-ad43-8ca6716b208f">IDTFilter2</a> interface and is exposed by the Decrypter/Detagger filter.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDTFilter3</b> interface inherits from <a href="https://msdn.microsoft.com/351c77ec-fb0c-4780-ad43-8ca6716b208f">IDTFilter2</a>. <b>IDTFilter3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDTFilter3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b1e4186-de85-4de8-b309-82644c8b1269">GetProtectionType</a>
</td>
<td align="left" width="63%">
Retrieves the type of content protection that is currently in effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/712be51a-27ed-4ede-bef6-9223c57f446f">LicenseHasExpirationDate</a>
</td>
<td align="left" width="63%">
Queries whether the license for the content has an expiration date.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d5c93f87-6988-4ca8-b50a-b6c7bdf3e76c">SetRights</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IDTFilter3)</code>.




## -see-also




<a href="https://msdn.microsoft.com/351c77ec-fb0c-4780-ad43-8ca6716b208f">IDTFilter2</a>



<a href="https://msdn.microsoft.com/abe939a3-5f43-4fdf-9d4d-34b7be8893eb">TV Ratings Interfaces</a>
 

 

