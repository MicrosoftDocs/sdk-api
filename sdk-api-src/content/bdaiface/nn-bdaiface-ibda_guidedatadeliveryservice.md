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

# IBDA_GuideDataDeliveryService interface


## -description


Retrieves out-of-band guide data from a media transform device (MTD). This interface provides access to a device's Guide Data Delivery Service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_GuideDataDeliveryService</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBDA_GuideDataDeliveryService</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBDA_GuideDataDeliveryService</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c261d20e-3760-4bf9-905b-f5620df4166b">GetGuideData</a>
</td>
<td align="left" width="63%">
Gets the next set of guide data that is available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74370ba8-2104-41f9-aa02-02b6790236da">GetGuideDataType</a>
</td>
<td align="left" width="63%">
Gets the format UUID for the data that is being retrieved on this service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8084e4dd-a5d5-48a0-a052-24310a79df78">GetServiceInfoFromTuneXml</a>
</td>
<td align="left" width="63%">
Gets service information from an XML tune request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82133fc5-0f42-4b24-abf6-bc46e72650ac">GetServices</a>
</td>
<td align="left" width="63%">
Gets a list of services that are available on the the MTD.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f429473-6a48-4298-b8f4-61809604ffbd">GetTuneXmlFromServiceIdx</a>
</td>
<td align="left" width="63%">
Converts a service identifier into an XML  tune request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e9aee857-237a-4bfd-85c2-3d5850f37ce7">RequestGuideDataUpdate</a>
</td>
<td align="left" width="63%">
Requests updated guide data from the MTD.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_GuideDataDeliveryService)</code>.



