---
UID: NN:dvbsiparser.IDvbServiceListDescriptor
title: IDvbServiceListDescriptor (dvbsiparser.h)
description: Implements methods that get data from a Digital Video Broadcast (DVB) service list descriptor. A service list descriptor is part of the DVB network information table (NIT) or bouquet association table (BAT) that lists services by service ID and type.
helpviewer_keywords: ["IDvbServiceListDescriptor","IDvbServiceListDescriptor interface [Microsoft TV Technologies]","IDvbServiceListDescriptor interface [Microsoft TV Technologies]","described","dvbsiparser/IDvbServiceListDescriptor","mstv.idvbservicelistdescriptor"]
old-location: mstv\idvbservicelistdescriptor.htm
tech.root: mstv
ms.assetid: 0d39595b-0297-473d-9b0f-e038a938a196
ms.date: 12/05/2018
ms.keywords: IDvbServiceListDescriptor, IDvbServiceListDescriptor interface [Microsoft TV Technologies], IDvbServiceListDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IDvbServiceListDescriptor, mstv.idvbservicelistdescriptor
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDvbServiceListDescriptor
 - dvbsiparser/IDvbServiceListDescriptor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IDvbServiceListDescriptor
---

# IDvbServiceListDescriptor interface


## -description

Implements methods that get data from a Digital Video Broadcast (DVB) service list descriptor. A service list descriptor is part of the DVB network information table (NIT) or bouquet association table (BAT) that lists services by service ID and type.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbServiceListDescriptor</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDvbServiceListDescriptor</b> also has these types of members:
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
<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbservicelistdescriptor-getcountofrecords">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets the number of service records in a  DVB service list descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbservicelistdescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of a  DVB service list descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbservicelistdescriptor-getrecordserviceid">GetRecordServiceId</a>
</td>
<td align="left" width="63%">
Gets the service_id field value from a  DVB service list descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbservicelistdescriptor-getrecordservicetype">GetRecordServiceType</a>
</td>
<td align="left" width="63%">
Gets the service_type field value from a  DVB service list descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbservicelistdescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag identifying a DVB service list descriptor.

</td>
</tr>
</table>