---
UID: NF:dvbsiparser.IDvbTeletextDescriptor.GetRecordTeletextType
title: IDvbTeletextDescriptor::GetRecordTeletextType (dvbsiparser.h)
description: Gets the teletext type code from from a Digital Video Broadcast (DVB) teletext descriptor.
helpviewer_keywords: ["GetRecordTeletextType","GetRecordTeletextType method [Microsoft TV Technologies]","GetRecordTeletextType method [Microsoft TV Technologies]","IDvbTeletextDescriptor interface","IDvbTeletextDescriptor interface [Microsoft TV Technologies]","GetRecordTeletextType method","IDvbTeletextDescriptor.GetRecordTeletextType","IDvbTeletextDescriptor::GetRecordTeletextType","dvbsiparser/IDvbTeletextDescriptor::GetRecordTeletextType","mstv.idvbteletextdescriptor_getrecordteletexttype"]
old-location: mstv\idvbteletextdescriptor_getrecordteletexttype.htm
tech.root: mstv
ms.assetid: 4272d95a-406f-4afc-92b9-abfd618f41ab
ms.date: 12/05/2018
ms.keywords: GetRecordTeletextType, GetRecordTeletextType method [Microsoft TV Technologies], GetRecordTeletextType method [Microsoft TV Technologies],IDvbTeletextDescriptor interface, IDvbTeletextDescriptor interface [Microsoft TV Technologies],GetRecordTeletextType method, IDvbTeletextDescriptor.GetRecordTeletextType, IDvbTeletextDescriptor::GetRecordTeletextType, dvbsiparser/IDvbTeletextDescriptor::GetRecordTeletextType, mstv.idvbteletextdescriptor_getrecordteletexttype
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
 - IDvbTeletextDescriptor::GetRecordTeletextType
 - dvbsiparser/IDvbTeletextDescriptor::GetRecordTeletextType
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
 - IDvbTeletextDescriptor.GetRecordTeletextType
---

# IDvbTeletextDescriptor::GetRecordTeletextType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the teletext type code from from a Digital Video Broadcast (DVB) teletext descriptor.

## -parameters

### -param bRecordIndex [in]

Zero-based index of the descriptor to return. To get the number of descriptors, call <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbteletextdescriptor-getcountofrecords">IDvbTeletextDescriptor::GetCountOfRecords</a>

### -param pbVal [out]

Receives the teletext type code. This can have any of the following values:

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
Reserved for future use

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
Initial teletext page

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
Teletext subtitle page

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x03</dt>
</dl>
</td>
<td width="60%">
Additional information page

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x04</dt>
</dl>
</td>
<td width="60%">
Program schedule page

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x05</dt>
</dl>
</td>
<td width="60%">
Teletext subtitle page for hearing-impaired people

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x06 - 0x1F</dt>
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

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbteletextdescriptor">IDvbTeletextDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbteletextdescriptor-getcountofrecords">IDvbTeletextDescriptor::GetCountOfRecords</a>