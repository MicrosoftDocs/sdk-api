---
UID: NN:dvbsiparser.IIsdbTerrestrialDeliverySystemDescriptor
title: IIsdbTerrestrialDeliverySystemDescriptor (dvbsiparser.h)
author: windows-sdk-content
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) terrestrial delivery system descriptor.
old-location: mstv\iisdbterrestrialdeliverysystemdescriptor.htm
tech.root: mstv
ms.assetid: 32bde3dd-05e0-466b-9f04-4b55b0d7f374
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IIsdbTerrestrialDeliverySystemDescriptor, IIsdbTerrestrialDeliverySystemDescriptor interface [Microsoft TV Technologies], IIsdbTerrestrialDeliverySystemDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IIsdbTerrestrialDeliverySystemDescriptor, mstv.iisdbterrestrialdeliverysystemdescriptor
ms.topic: interface
f1_keywords: ["dvbsiparser/IIsdbTerrestrialDeliverySystemDescriptor"]
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
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
 - IIsdbTerrestrialDeliverySystemDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbTerrestrialDeliverySystemDescriptor interface


## -description


Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) terrestrial delivery system descriptor. The terrestrial delivery system descriptor appears in the network information table (NIT) as part of the ISDB service information and indicates the physical characteristics of the terrestrial transmission path. This descriptor is required for all ISDB terrestrial broadcasting.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIsdbTerrestrialDeliverySystemDescriptor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IIsdbTerrestrialDeliverySystemDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IIsdbTerrestrialDeliverySystemDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbterrestrialdeliverysystemdescriptor-getareacode">GetAreaCode</a>
</td>
<td align="left" width="63%">
 Gets the service area code from an ISDB terrestrial delivery system descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbterrestrialdeliverysystemdescriptor-getcountofrecords">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
 Gets the number of records in an ISDB terrestrial delivery system descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbterrestrialdeliverysystemdescriptor-getguardinterval">GetGuardInterval</a>
</td>
<td align="left" width="63%">
 Gets a code that indicates the guard interval from an ISDB terrestrial delivery system descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbterrestrialdeliverysystemdescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
 Gets the body length of an ISDB terrestrial delivery system descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbterrestrialdeliverysystemdescriptor-getrecordfrequency">GetRecordFrequency</a>
</td>
<td align="left" width="63%">
 Gets the center frequency from an ISDB terrestrial delivery system descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbterrestrialdeliverysystemdescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies an ISDB terrestrial delivery system descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbterrestrialdeliverysystemdescriptor-gettransmissionmode">GetTransmissionMode</a>
</td>
<td align="left" width="63%">
 Gets a code that indicates the transmission mode from an ISDB terrestrial delivery system descriptor.

</td>
</tr>
</table> 

