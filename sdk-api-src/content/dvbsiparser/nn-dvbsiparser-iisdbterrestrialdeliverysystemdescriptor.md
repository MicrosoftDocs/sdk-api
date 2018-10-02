---
UID: NN:dvbsiparser.IIsdbTerrestrialDeliverySystemDescriptor
title: IIsdbTerrestrialDeliverySystemDescriptor
author: windows-sdk-content
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) terrestrial delivery system descriptor.
old-location: mstv\iisdbterrestrialdeliverysystemdescriptor.htm
tech.root: MSTV
ms.assetid: 32bde3dd-05e0-466b-9f04-4b55b0d7f374
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IIsdbTerrestrialDeliverySystemDescriptor, IIsdbTerrestrialDeliverySystemDescriptor interface [Microsoft TV Technologies], IIsdbTerrestrialDeliverySystemDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IIsdbTerrestrialDeliverySystemDescriptor, mstv.iisdbterrestrialdeliverysystemdescriptor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
---

# IIsdbTerrestrialDeliverySystemDescriptor interface


## -description


Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) terrestrial delivery system descriptor. The terrestrial delivery system descriptor appears in the network information table (NIT) as part of the ISDB service information and indicates the physical characteristics of the terrestrial transmission path. This descriptor is required for all ISDB terrestrial broadcasting.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIsdbTerrestrialDeliverySystemDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IIsdbTerrestrialDeliverySystemDescriptor</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/14ba763d-c21c-48c1-b5d9-d29cc1108a58">GetAreaCode</a>
</td>
<td align="left" width="63%">
 Gets the service area code from an ISDB terrestrial delivery system descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d13cadd3-561f-4d4e-8260-7a1d56dfa578">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
 Gets the number of records in an ISDB terrestrial delivery system descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f1016fd4-bcd9-4678-b59c-c6c8207f242d">GetGuardInterval</a>
</td>
<td align="left" width="63%">
 Gets a code that indicates the guard interval from an ISDB terrestrial delivery system descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4c01c512-03b4-45f1-99e0-853aa42b79a8">GetLength</a>
</td>
<td align="left" width="63%">
 Gets the body length of an ISDB terrestrial delivery system descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9040dcc9-49c8-4c3b-ad86-7dc38d1722b9">GetRecordFrequency</a>
</td>
<td align="left" width="63%">
 Gets the center frequency from an ISDB terrestrial delivery system descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/15b70e2e-21e0-406c-9d7a-32031114d50b">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies an ISDB terrestrial delivery system descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d7f4659f-0aa6-46a6-a352-da801d132866">GetTransmissionMode</a>
</td>
<td align="left" width="63%">
 Gets a code that indicates the transmission mode from an ISDB terrestrial delivery system descriptor.

</td>
</tr>
</table> 

