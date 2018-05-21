---
UID: NN:dvbsiparser.IDvbFrequencyListDescriptor
title: IDvbFrequencyListDescriptor
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvbfrequencylistdescriptor.htm
old-project: mstv
ms.assetid: fadf7114-b9e4-4f61-816b-10725b83169a
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IDvbFrequencyListDescriptor, IDvbFrequencyListDescriptor interface [Microsoft TV Technologies], IDvbFrequencyListDescriptor interface [Microsoft TV Technologies],described, IDvbFrequencyListDescriptorInterface, dvbsiparser/IDvbFrequencyListDescriptor, mstv.idvbfrequencylistdescriptor
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IDvbFrequencyListDescriptor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbFrequencyListDescriptor interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IDvbFrequencyListDescriptor</b> interface enables the client to get a frequency list descriptor from a DVB stream. The frequency list descriptor may be present in the network information table (NIT). For more information, refer to ETSI EN 300 468.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbFrequencyListDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDvbFrequencyListDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbFrequencyListDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d458f42-bea5-4503-a2d7-89efd1abc1a8">GetCodingType</a>
</td>
<td align="left" width="63%">
Returns a flag that specifies how the frequency is coded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9bce2abf-2673-49c6-8b87-7c8825544156">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Returns the number of records in the frequency list descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e00542ff-2d28-44cb-8dd5-944f12f2805d">GetLength</a>
</td>
<td align="left" width="63%">
Returns the length of the descriptor body.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb6c3c14-c4b6-412d-ad12-1c7fdb025527">GetRecordCentreFrequency</a>
</td>
<td align="left" width="63%">
Returns the frequency at a specified index in the frequency list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/05c607b4-c5de-4a57-93c0-412c85d9f2fa">GetTag</a>
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
<li>Call <a href="https://msdn.microsoft.com/e4d3da3c-3631-41c2-b463-a90cd54e42f9">IDVB_NIT::GetRecordDescriptorByTag</a> and pass in the frequency list descriptor tag (0x62). If the descriptor is present, the method returns an <a href="https://msdn.microsoft.com/efca0ecf-eb3e-4dcd-a674-b8fe1a66ff84">IGenericDescriptor</a> pointer.</li>
<li>Query the returned <b>IGenericDescriptor</b> pointer for the <b>IDvbFrequencyListDescriptor</b> interface.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

