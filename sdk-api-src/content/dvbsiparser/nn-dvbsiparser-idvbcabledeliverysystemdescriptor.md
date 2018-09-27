---
UID: NN:dvbsiparser.IDvbCableDeliverySystemDescriptor
title: IDvbCableDeliverySystemDescriptor
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvbcabledeliverysystemdescriptor.htm
tech.root: MSTV
ms.assetid: b4fb2fd0-e32a-4737-8095-7d4df40a26a0
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IDvbCableDeliverySystemDescriptor, IDvbCableDeliverySystemDescriptor interface [Microsoft TV Technologies], IDvbCableDeliverySystemDescriptor interface [Microsoft TV Technologies],described, IDvbCableDeliverySystemDescriptorInterface, dvbsiparser/IDvbCableDeliverySystemDescriptor, mstv.idvbcabledeliverysystemdescriptor
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
 - IDvbCableDeliverySystemDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvbCableDeliverySystemDescriptor interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IDvbCableDeliverySystemDescriptor</b> interface enables the client to get a cable delivery system descriptor from a DVB stream. The cable delivery system descriptor may be present in the network information table (NIT). For more information, refer to ETSI EN 300 468.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbCableDeliverySystemDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDvbCableDeliverySystemDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbCableDeliverySystemDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b16b904-58aa-4f28-83aa-80dd625d387a">GetFECInner</a>
</td>
<td align="left" width="63%">
Returns the inner forward error correction (FEC) scheme.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf6d094f-d394-43a3-b74e-a167759d5a10">GetFECOuter</a>
</td>
<td align="left" width="63%">
Returns the output FEC scheme.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2077940c-7835-48c5-a288-825d4c9ca0e6">GetFrequency</a>
</td>
<td align="left" width="63%">
Returns the frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f6c0a4c-6f0e-4217-b6a0-af709a75d24d">GetLength</a>
</td>
<td align="left" width="63%">
Returns the length of the descriptor body.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/896c9ff6-8333-4fb4-bd25-fda9d12129e8">GetModulation</a>
</td>
<td align="left" width="63%">
Returns the modulation scheme.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0484e12d-6b93-4ed6-865a-d4992ad1de75">GetSymbolRate</a>
</td>
<td align="left" width="63%">
Returns the symbol rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eedc30b7-f51a-472a-8d6f-4a8f7be6d2dc">GetTag</a>
</td>
<td align="left" width="63%">
Returns the descriptor tag.

</td>
</tr>
</table> 


## -remarks



To obtain a pointer to this interface, do the following:

<ol>
<li>Call <a href="https://msdn.microsoft.com/a7c802ad-908f-4778-b8db-02fff4f3a13e">IDvbSiParser::GetNIT</a> to get the <a href="https://msdn.microsoft.com/70b638ae-0152-4a44-aeb1-f3ac382c19ce">IDVB_NIT</a> interface.</li>
<li>Call <a href="https://msdn.microsoft.com/e4d3da3c-3631-41c2-b463-a90cd54e42f9">IDVB_NIT::GetRecordDescriptorByTag</a> and pass in the cable delivery system descriptor tag (0x44). If the descriptor is present, the method returns an <a href="https://msdn.microsoft.com/efca0ecf-eb3e-4dcd-a674-b8fe1a66ff84">IGenericDescriptor</a> pointer.</li>
<li>Query the returned <b>IGenericDescriptor</b> pointer for the <b>IDvbCableDeliverySystemDescriptor</b> interface.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

