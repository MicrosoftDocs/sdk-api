---
UID: NN:dvbsiparser.IDvbServiceListDescriptor
title: IDvbServiceListDescriptor
author: windows-sdk-content
description: Implements methods that get data from a Digital Video Broadcast (DVB) service list descriptor. A service list descriptor is part of the DVB network information table (NIT) or bouquet association table (BAT) that lists services by service ID and type.
old-location: mstv\idvbservicelistdescriptor.htm
tech.root: MSTV
ms.assetid: 0d39595b-0297-473d-9b0f-e038a938a196
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IDvbServiceListDescriptor, IDvbServiceListDescriptor interface [Microsoft TV Technologies], IDvbServiceListDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IDvbServiceListDescriptor, mstv.idvbservicelistdescriptor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
 - IDvbServiceListDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvbServiceListDescriptor interface


## -description


Implements methods that get data from a Digital Video Broadcast (DVB) service list descriptor. A service list descriptor is part of the DVB network information table (NIT) or bouquet association table (BAT) that lists services by service ID and type.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbServiceListDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDvbServiceListDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbServiceListDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8a3dd6b9-a7a1-49fd-806d-05c726bbe99e">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets the number of service records in a  DVB service list descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06c161ce-b830-4375-8ed6-19403857f433">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of a  DVB service list descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c98d032a-0a3c-4e27-a5b7-ee594024ac9d">GetRecordServiceId</a>
</td>
<td align="left" width="63%">
Gets the service_id field value from a  DVB service list descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c9771d79-7f39-463a-aa20-d5377bbba610">GetRecordServiceType</a>
</td>
<td align="left" width="63%">
Gets the service_type field value from a  DVB service list descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e16ab7f-25df-461e-b3aa-73de613e45b6">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag identifying a DVB service list descriptor.

</td>
</tr>
</table> 

