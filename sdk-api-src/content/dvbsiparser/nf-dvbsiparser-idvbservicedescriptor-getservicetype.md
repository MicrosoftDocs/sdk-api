---
UID: NF:dvbsiparser.IDvbServiceDescriptor.GetServiceType
title: IDvbServiceDescriptor::GetServiceType (dvbsiparser.h)
description: Gets the service_type field value from a Digital Video Broadcast (DVB) service descriptor.
helpviewer_keywords: ["GetServiceType","GetServiceType method [Microsoft TV Technologies]","GetServiceType method [Microsoft TV Technologies]","IDvbServiceDescriptor interface","IDvbServiceDescriptor interface [Microsoft TV Technologies]","GetServiceType method","IDvbServiceDescriptor.GetServiceType","IDvbServiceDescriptor::GetServiceType","dvbsiparser/IDvbServiceDescriptor::GetServiceType","mstv.idvbservicedescriptor_getservicetype"]
old-location: mstv\idvbservicedescriptor_getservicetype.htm
tech.root: mstv
ms.assetid: f13b6b0e-d4bb-42a6-9bab-dc3e13bc26e9
ms.date: 12/05/2018
ms.keywords: GetServiceType, GetServiceType method [Microsoft TV Technologies], GetServiceType method [Microsoft TV Technologies],IDvbServiceDescriptor interface, IDvbServiceDescriptor interface [Microsoft TV Technologies],GetServiceType method, IDvbServiceDescriptor.GetServiceType, IDvbServiceDescriptor::GetServiceType, dvbsiparser/IDvbServiceDescriptor::GetServiceType, mstv.idvbservicedescriptor_getservicetype
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
 - IDvbServiceDescriptor::GetServiceType
 - dvbsiparser/IDvbServiceDescriptor::GetServiceType
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
 - IDvbServiceDescriptor.GetServiceType
---

# IDvbServiceDescriptor::GetServiceType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the service_type field value from a Digital Video Broadcast (DVB) service descriptor.

## -parameters

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
Digital television service. (MPEG-2 standard-definition [SD] material should use this type.)

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
Near-video-on-demand (NVOD) reference service. (MPEG-2 SD material should use this type.)

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
Mosaic service

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x07-0x09</dt>
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
Reserved for Common Interface Usage (see <a href="http://broadcasting.ru/pdf-standard-specifications/interfacing/dvb-ci/en50221.pdf">CENELEC EN 50221: "Common interface specification for conditional access and other digital
video broadcasting decoder applications"</a> ) 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x0E</dt>
</dl>
</td>
<td width="60%">
Return Channel Satellite (RCS) Map (see <a href="http://www.dvb.org/technology/standards/a054r4.1.dEn301790.V1.5.1.pdf">Digital Video Broadcasting (DVB);
Interaction channel for satellite distribution systems, ETSI EN 301 790</a> ).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x0F</dt>
</dl>
</td>
<td width="60%">
RCS Forward Link Signalling (FLS) (see <a href="http://www.dvb.org/technology/standards/a054r4.1.dEn301790.V1.5.1.pdf">EN 301 790</a>).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x10</dt>
</dl>
</td>
<td width="60%">
DVB Multimedia Home Platform (MHP) service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x11</dt>
</dl>
</td>
<td width="60%">
MPEG-2 high-definition (HD) digital television service

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x12-0x15</dt>
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
Advanced codec  HD NVOD time-shifted service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x1C - 0x7F</dt>
</dl>
</td>
<td width="60%">
Reserved for future use

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x80 - 0xFE</dt>
</dl>
</td>
<td width="60%">
User-defined

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0xFF</dt>
</dl>
</td>
<td width="60%">
Reserved for future use

</td>
</tr>
</table>

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbservicedescriptor">IDvbServiceDescriptor</a>