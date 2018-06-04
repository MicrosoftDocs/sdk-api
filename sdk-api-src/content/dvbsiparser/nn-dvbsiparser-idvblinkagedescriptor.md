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

# IDvbLinkageDescriptor interface


## -description


Defines methods that get data from a Digital Video Broadcast (DVB) linkage descriptor. The linkage descriptor appears as part of the DVB service information in the network information table (NIT), bouquet association table (BAT), service description table (SDT), event information table (EIT), or service information table (SIT). 

The linkage descriptor identifies a service that can be presented if the consumer requests additional
information related to a service. The table that contains the linkage descriptor  indicates the entity for which additional information is available. For example, a linkage descriptor in the
NIT points to a service that provides additional information on the network, while a linkage descriptor in the BAT links to a service that provides information  about the bouquet.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbLinkageDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDvbLinkageDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbLinkageDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6a4e072-3abe-4305-811d-2bdb846ce028">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of a DVB linkage descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54e17da4-df93-40a5-a359-274da77f585d">GetLinkageType</a>
</td>
<td align="left" width="63%">
Gets a code that uniquely identifies the linkage type from a DVB linkage descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7c27f45-032a-46d5-b5ae-8a4ef2ee2ebc">GetONId</a>
</td>
<td align="left" width="63%">
Gets the network identifier of the  broadcast system that originates the information service from a DVB linkage descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/959aeb87-b661-4567-a6fd-2d28be6b0a02">GetPrivateData</a>
</td>
<td align="left" width="63%">
Gets the private data from a DVB linkage descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c37a877-5a0e-49ed-bf75-bb8ad73fa783">GetPrivateDataLength</a>
</td>
<td align="left" width="63%">
Gets the length of the private data field from a DVB linkage descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/977c284d-b995-4879-b90a-2bc42b60d1a3">GetServiceId</a>
</td>
<td align="left" width="63%">
Gets the identifier that identifies an information service a DVB linkage descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a01430f-13b2-40ff-a47e-98e1bcdbf4fc">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies a DVB linkage descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/263f3ff1-33a6-4c40-bcdf-049c4dbaf2ef">GetTSId</a>
</td>
<td align="left" width="63%">
Gets the identifier of the  transport stream that contains the information service from a DVB linkage descriptor.

</td>
</tr>
</table> 

