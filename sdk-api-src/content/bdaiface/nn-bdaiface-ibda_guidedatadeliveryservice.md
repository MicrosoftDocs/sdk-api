---
UID: NN:bdaiface.IBDA_GuideDataDeliveryService
title: IBDA_GuideDataDeliveryService (bdaiface.h)
author: windows-sdk-content
description: Retrieves out-of-band guide data from a media transform device (MTD). This interface provides access to a device's Guide Data Delivery Service.
old-location: mstv\ibda_guidedatadeliveryservice.htm
tech.root: mstv
ms.assetid: 5329f725-e77e-49c2-87f5-f7204d022adc
ms.author: windowssdkdev
ms.date: 12/05/2018
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
ms.custom: 19H1
---

# IBDA_GuideDataDeliveryService interface


## -description


Retrieves out-of-band guide data from a media transform device (MTD). This interface provides access to a device's Guide Data Delivery Service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_GuideDataDeliveryService</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBDA_GuideDataDeliveryService</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_guidedatadeliveryservice-getguidedata">GetGuideData</a>
</td>
<td align="left" width="63%">
Gets the next set of guide data that is available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_guidedatadeliveryservice-getguidedatatype">GetGuideDataType</a>
</td>
<td align="left" width="63%">
Gets the format UUID for the data that is being retrieved on this service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_guidedatadeliveryservice-getserviceinfofromtunexml">GetServiceInfoFromTuneXml</a>
</td>
<td align="left" width="63%">
Gets service information from an XML tune request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_guidedatadeliveryservice-getservices">GetServices</a>
</td>
<td align="left" width="63%">
Gets a list of services that are available on the the MTD.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_guidedatadeliveryservice-gettunexmlfromserviceidx">GetTuneXmlFromServiceIdx</a>
</td>
<td align="left" width="63%">
Converts a service identifier into an XML  tune request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_guidedatadeliveryservice-requestguidedataupdate">RequestGuideDataUpdate</a>
</td>
<td align="left" width="63%">
Requests updated guide data from the MTD.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_GuideDataDeliveryService)</code>.



