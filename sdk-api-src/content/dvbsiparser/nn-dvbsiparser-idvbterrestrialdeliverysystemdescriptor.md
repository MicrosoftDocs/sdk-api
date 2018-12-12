---
UID: NN:dvbsiparser.IDvbTerrestrialDeliverySystemDescriptor
title: IDvbTerrestrialDeliverySystemDescriptor
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvbterrestrialdeliverysystemdescriptor.htm
tech.root: mstv
ms.assetid: 7000f937-2f58-43c1-b0e1-60d3171485b0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDvbTerrestrialDeliverySystemDescriptor, IDvbTerrestrialDeliverySystemDescriptor interface [Microsoft TV Technologies], IDvbTerrestrialDeliverySystemDescriptor interface [Microsoft TV Technologies],described, IDvbTerrestrialDeliverySystemDescriptorInterface, dvbsiparser/IDvbTerrestrialDeliverySystemDescriptor, mstv.idvbterrestrialdeliverysystemdescriptor
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IDvbTerrestrialDeliverySystemDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvbTerrestrialDeliverySystemDescriptor interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IDvbTerrestrialDeliverySystemDescriptor</b> interface enables the client to get a terrestrial delivery system descriptor from a DVB stream. The terrestrial delivery system descriptor may be present in the network information table (NIT). For more information, refer to ETSI EN 300 468.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbTerrestrialDeliverySystemDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDvbTerrestrialDeliverySystemDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbTerrestrialDeliverySystemDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60efabb7-82bd-4b1f-991e-854c1a8b75ce">GetBandwidth</a>
</td>
<td align="left" width="63%">
Returns the bandwidth in use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80ce6831-afb0-4fdd-844d-1aa400449110">GetCentreFrequency</a>
</td>
<td align="left" width="63%">
Returns the center frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/84cc3e77-aa46-40b0-ad04-27541216bb6f">GetCodeRateHPStream</a>
</td>
<td align="left" width="63%">
Returns the code rate for the high-priority (HP) stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dc4a1eef-1dd3-4946-8dad-6c8993290ca2">GetCodeRateLPStream</a>
</td>
<td align="left" width="63%">
Returns the code rate for the low-priority (LP) stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a34de19-c684-4778-a164-5ddde87443b0">GetConstellation</a>
</td>
<td align="left" width="63%">
Returns the constellation pattern.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6c3e121-7214-49cc-b88e-6a1269f5bdbd">GetGuardInterval</a>
</td>
<td align="left" width="63%">
Returns the guard interval.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ad35924-b6e0-47b1-9873-14bf48574669">GetHierarchyInformation</a>
</td>
<td align="left" width="63%">
Returns the hierarchy alpha information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14677ccd-fe8a-4d0f-9229-891bb0b5c35a">GetLength</a>
</td>
<td align="left" width="63%">
Returns the length of the descriptor body.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1462004c-7605-430e-bf9a-beb1776adb6c">GetOtherFrequencyFlag</a>
</td>
<td align="left" width="63%">
Returns a flag that specifies whether other frequencies are in use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a4076176-6e24-4469-b2f3-52c1e8f388bb">GetTag</a>
</td>
<td align="left" width="63%">
Returns the descriptor tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d825f933-0da6-4e8e-bc28-b9e2db575a12">GetTransmissionMode</a>
</td>
<td align="left" width="63%">
Returns the transmission mode.

</td>
</tr>
</table> 


## -remarks



To obtain a pointer to this interface, do the following:

<ol>
<li>Call <a href="https://msdn.microsoft.com/a7c802ad-908f-4778-b8db-02fff4f3a13e">IDvbSiParser::GetNIT</a> to get the <a href="https://msdn.microsoft.com/70b638ae-0152-4a44-aeb1-f3ac382c19ce">IDVB_NIT</a> interface.</li>
<li>Call <a href="https://msdn.microsoft.com/e4d3da3c-3631-41c2-b463-a90cd54e42f9">IDVB_NIT::GetRecordDescriptorByTag</a> and pass in the terrestrial delivery system descriptor tag (0x5A). If the descriptor is present, the method returns an <a href="https://msdn.microsoft.com/en-us/library/Dd694093(v=VS.85).aspx">IGenericDescriptor</a> pointer.</li>
<li>Query the returned <b>IGenericDescriptor</b> pointer for the <b>IDvbTerrestrialDeliverySystemDescriptor</b> interface.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

