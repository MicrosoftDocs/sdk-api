---
UID: NF:dvbsiparser.IDvbServiceListDescriptor.GetRecordServiceType
title: IDvbServiceListDescriptor::GetRecordServiceType (dvbsiparser.h)
description: Gets the service_type field value from a Digital Video Broadcast (DVB) service descriptor.
helpviewer_keywords: ["GetRecordServiceType","GetRecordServiceType method [Microsoft TV Technologies]","GetRecordServiceType method [Microsoft TV Technologies]","IDvbServiceListDescriptor interface","IDvbServiceListDescriptor interface [Microsoft TV Technologies]","GetRecordServiceType method","IDvbServiceListDescriptor.GetRecordServiceType","IDvbServiceListDescriptor::GetRecordServiceType","dvbsiparser/IDvbServiceListDescriptor::GetRecordServiceType","mstv.idvbservicelistdescriptor_getrecordservicetype"]
old-location: mstv\idvbservicelistdescriptor_getrecordservicetype.htm
tech.root: mstv
ms.assetid: c9771d79-7f39-463a-aa20-d5377bbba610
ms.date: 12/05/2018
ms.keywords: GetRecordServiceType, GetRecordServiceType method [Microsoft TV Technologies], GetRecordServiceType method [Microsoft TV Technologies],IDvbServiceListDescriptor interface, IDvbServiceListDescriptor interface [Microsoft TV Technologies],GetRecordServiceType method, IDvbServiceListDescriptor.GetRecordServiceType, IDvbServiceListDescriptor::GetRecordServiceType, dvbsiparser/IDvbServiceListDescriptor::GetRecordServiceType, mstv.idvbservicelistdescriptor_getrecordservicetype
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
 - IDvbServiceListDescriptor::GetRecordServiceType
 - dvbsiparser/IDvbServiceListDescriptor::GetRecordServiceType
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
 - IDvbServiceListDescriptor.GetRecordServiceType
---

# IDvbServiceListDescriptor::GetRecordServiceType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the service_type field value from a Digital Video Broadcast (DVB) service descriptor.

## -parameters

### -param bRecordIndex [in]

Specifies the service record number,
  indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbservicelistdescriptor-getcountofrecords">IDvbServiceListDescriptor::GetCountOfRecords</a> method to get the number of records in the logical channel descriptor.

### -param pbVal [out]

Receives the service type. This can be any of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">
Reserved for future use.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
Digital television service. (MPEG-2 SD material should use this type.)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
Digital radio sound service. (MPEG-1 Layer 2 audio material should use this type.)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x03</dt>
</dl>
</td>
<td width="60%">
Teletext service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x04</dt>
</dl>
</td>
<td width="60%">
NVOD reference service. (MPEG-2 SD material should use this type.)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x05</dt>
</dl>
</td>
<td width="60%">
NVOD time-shifted service. (MPEG-2 SD material should use this type.)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x06</dt>
</dl>
</td>
<td width="60%">
Mosaic service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x07 - 0x09</dt>
</dl>
</td>
<td width="60%">
Reserved for future use.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x0A</dt>
</dl>
</td>
<td width="60%">
Advanced codec digital radio sound service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x0B</dt>
</dl>
</td>
<td width="60%">
Advanced codec mosaic service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x0C</dt>
</dl>
</td>
<td width="60%">
Data broadcast service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x0D</dt>
</dl>
</td>
<td width="60%">
Reserved for Common Interface Usage (EN 5022).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x0E</dt>
</dl>
</td>
<td width="60%">
RCS Map (see EN 301 790 [7]).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x0F</dt>
</dl>
</td>
<td width="60%">
RCS FLS (see EN 301 790 [7]).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x10</dt>
</dl>
</td>
<td width="60%">
DVB MHP service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x11</dt>
</dl>
</td>
<td width="60%">
MPEG-2 HD digital television service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x12 - 0x15</dt>
</dl>
</td>
<td width="60%">
Reserved for future use.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x16</dt>
</dl>
</td>
<td width="60%">
Advanced codec SD digital television service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x17</dt>
</dl>
</td>
<td width="60%">
Advanced codec SD NVOD time-shifted service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x18</dt>
</dl>
</td>
<td width="60%">
Advanced codec SD NVOD reference service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x19</dt>
</dl>
</td>
<td width="60%">
Advanced codec HD digital television service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x1A</dt>
</dl>
</td>
<td width="60%">
Advanced codec HD NVOD time-shifted service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x1B</dt>
</dl>
</td>
<td width="60%">
Advanced codec HD NVOD reference service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x1C - 0x7F</dt>
</dl>
</td>
<td width="60%">
Reserved for future use.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x80 - 0xFE</dt>
</dl>
</td>
<td width="60%">
User-defined.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0xFF</dt>
</dl>
</td>
<td width="60%">
Reserved for future use.

</td>
</tr>
</table>

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbservicelistdescriptor">IDvbServiceListDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbservicelistdescriptor-getcountofrecords">IDvbServiceListDescriptor::GetCountOfRecords</a>