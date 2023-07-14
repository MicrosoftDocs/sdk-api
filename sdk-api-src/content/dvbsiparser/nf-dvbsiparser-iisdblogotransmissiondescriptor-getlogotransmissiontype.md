---
UID: NF:dvbsiparser.IIsdbLogoTransmissionDescriptor.GetLogoTransmissionType
title: IIsdbLogoTransmissionDescriptor::GetLogoTransmissionType (dvbsiparser.h)
description: Gets the value of the logo_transmission_type field from an Integrated Services Digital Broadcasting (ISDB) logo transmission descriptor. This field contains a code that indicates the logo transmission type.
helpviewer_keywords: ["GetLogoTransmissionType","GetLogoTransmissionType method [Microsoft TV Technologies]","GetLogoTransmissionType method [Microsoft TV Technologies]","IIsdbLogoTransmissionDescriptor interface","IIsdbLogoTransmissionDescriptor interface [Microsoft TV Technologies]","GetLogoTransmissionType method","IIsdbLogoTransmissionDescriptor.GetLogoTransmissionType","IIsdbLogoTransmissionDescriptor::GetLogoTransmissionType","dvbsiparser/IIsdbLogoTransmissionDescriptor::GetLogoTransmissionType","mstv.iisdblogotransmissiondescriptor_getlogotransmissiontype"]
old-location: mstv\iisdblogotransmissiondescriptor_getlogotransmissiontype.htm
tech.root: mstv
ms.assetid: a8f824ec-36f7-4af0-bce3-295b8403e431
ms.date: 12/05/2018
ms.keywords: GetLogoTransmissionType, GetLogoTransmissionType method [Microsoft TV Technologies], GetLogoTransmissionType method [Microsoft TV Technologies],IIsdbLogoTransmissionDescriptor interface, IIsdbLogoTransmissionDescriptor interface [Microsoft TV Technologies],GetLogoTransmissionType method, IIsdbLogoTransmissionDescriptor.GetLogoTransmissionType, IIsdbLogoTransmissionDescriptor::GetLogoTransmissionType, dvbsiparser/IIsdbLogoTransmissionDescriptor::GetLogoTransmissionType, mstv.iisdblogotransmissiondescriptor_getlogotransmissiontype
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
 - IIsdbLogoTransmissionDescriptor::GetLogoTransmissionType
 - dvbsiparser/IIsdbLogoTransmissionDescriptor::GetLogoTransmissionType
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
 - IIsdbLogoTransmissionDescriptor.GetLogoTransmissionType
---

# IIsdbLogoTransmissionDescriptor::GetLogoTransmissionType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the value of the logo_transmission_type field from an Integrated Services Digital Broadcasting (ISDB) logo transmission descriptor. This field contains a code that indicates the logo transmission type.

## -parameters

### -param pbVal [out]

Receives the logo transmission type. This can be any of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
Common data table (CDT) transmission scheme 1, which refers to CDT
directly using download data identification.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
CDT transmission scheme 2, which refers to CDT
indirectly using download data identification.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x03</dt>
</dl>
</td>
<td width="60%">
Simple logo system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x04-0xFF</dt>
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

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdblogotransmissiondescriptor">IIsdbLogoTransmissionDescriptor</a>