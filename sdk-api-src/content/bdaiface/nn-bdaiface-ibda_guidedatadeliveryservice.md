---
UID: NN:bdaiface.IBDA_GuideDataDeliveryService
title: IBDA_GuideDataDeliveryService (bdaiface.h)
author: windows-sdk-content
description: Retrieves out-of-band guide data from a media transform device (MTD). This interface provides access to a device's Guide Data Delivery Service.
old-location: mstv\ibda_guidedatadeliveryservice.htm
tech.root: mstv
ms.assetid: 5329f725-e77e-49c2-87f5-f7204d022adc
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBDA_GuideDataDeliveryService, IBDA_GuideDataDeliveryService interface [Microsoft TV Technologies], IBDA_GuideDataDeliveryService interface [Microsoft TV Technologies],described, bdaiface/IBDA_GuideDataDeliveryService, mstv.ibda_guidedatadeliveryservice
ms.topic: interface
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bdaiface.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_GuideDataDeliveryService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/en-us/library/Dd693369(v=VS.85).aspx">GetGuideData</a>
</td>
<td align="left" width="63%">
Gets the next set of guide data that is available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693370(v=VS.85).aspx">GetGuideDataType</a>
</td>
<td align="left" width="63%">
Gets the format UUID for the data that is being retrieved on this service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693371(v=VS.85).aspx">GetServiceInfoFromTuneXml</a>
</td>
<td align="left" width="63%">
Gets service information from an XML tune request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693372(v=VS.85).aspx">GetServices</a>
</td>
<td align="left" width="63%">
Gets a list of services that are available on the the MTD.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693373(v=VS.85).aspx">GetTuneXmlFromServiceIdx</a>
</td>
<td align="left" width="63%">
Converts a service identifier into an XML  tune request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693374(v=VS.85).aspx">RequestGuideDataUpdate</a>
</td>
<td align="left" width="63%">
Requests updated guide data from the MTD.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_GuideDataDeliveryService)</code>.



