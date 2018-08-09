---
UID: NN:dvbsiparser.IDvbSatelliteDeliverySystemDescriptor
title: IDvbSatelliteDeliverySystemDescriptor
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvbsatellitedeliverysystemdescriptor.htm
old-project: mstv
ms.assetid: 814becf0-c98a-4419-aca6-d9b22d273e97
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IDvbSatelliteDeliverySystemDescriptor, IDvbSatelliteDeliverySystemDescriptor interface [Microsoft TV Technologies], IDvbSatelliteDeliverySystemDescriptor interface [Microsoft TV Technologies],described, IDvbSatelliteDeliverySystemDescriptorInterface, dvbsiparser/IDvbSatelliteDeliverySystemDescriptor, mstv.idvbsatellitedeliverysystemdescriptor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dvbsiparser.h
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
tech.root: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IDvbSatelliteDeliverySystemDescriptor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbSatelliteDeliverySystemDescriptor interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IDvbSatelliteDeliverySystemDescriptor</b> interface enables the client to get a satellite delivery system descriptor from a DVB stream. The satellite delivery system descriptor may be present in the network information table (NIT). For more information, refer to ETSI EN 300 468.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbSatelliteDeliverySystemDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDvbSatelliteDeliverySystemDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbSatelliteDeliverySystemDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe90fcd7-e77b-42c8-935f-4cf02957400f">GetFECInner</a>
</td>
<td align="left" width="63%">
Returns the inner forward error correction (FEC) scheme.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dc298f61-f7f1-42dc-a585-bfe9f58b1629">GetFrequency</a>
</td>
<td align="left" width="63%">
Returns the frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd3ce6ba-e9a7-495d-80e7-532e5cf5e94c">GetLength</a>
</td>
<td align="left" width="63%">
Returns the length of the descriptor body.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66578df9-35f7-4a2b-91ce-3f60cab16dd3">GetModulation</a>
</td>
<td align="left" width="63%">
Returns the modulation scheme.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1fc3f934-5a9f-4e76-ae1c-e74ea332e8e6">GetOrbitalPosition</a>
</td>
<td align="left" width="63%">
Returns the orbital position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe063a08-74bd-40c4-a185-3cc932a0a06d">GetPolarization</a>
</td>
<td align="left" width="63%">
Returns the polarization of the transmitted signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/184b1cb6-432a-4227-b711-e05201f80bf1">GetSymbolRate</a>
</td>
<td align="left" width="63%">
Returns the symbol rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/217b49b8-8e98-4784-837d-67471fda2ea5">GetTag</a>
</td>
<td align="left" width="63%">
Returns the descriptor tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/533a2ed4-f5ac-4f41-a03b-0b274f327436">GetWestEastFlag</a>
</td>
<td align="left" width="63%">
Returns a flag that specifies whether the satellite is in the western or eastern part of the orbit.

</td>
</tr>
</table> 


## -remarks



To obtain a pointer to this interface, do the following:

<ol>
<li>Call <a href="https://msdn.microsoft.com/a7c802ad-908f-4778-b8db-02fff4f3a13e">IDvbSiParser::GetNIT</a> to get the <a href="https://msdn.microsoft.com/70b638ae-0152-4a44-aeb1-f3ac382c19ce">IDVB_NIT</a> interface.</li>
<li>Call <a href="https://msdn.microsoft.com/e4d3da3c-3631-41c2-b463-a90cd54e42f9">IDVB_NIT::GetRecordDescriptorByTag</a> and pass in the satellite delivery system descriptor tag (0x43). If the descriptor is present, the method returns an <a href="https://msdn.microsoft.com/efca0ecf-eb3e-4dcd-a674-b8fe1a66ff84">IGenericDescriptor</a> pointer.</li>
<li>Query the returned <b>IGenericDescriptor</b> pointer for the <b>IDvbSatelliteDeliverySystemDescriptor</b> interface.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

