---
UID: NF:dvbsiparser.IDvbSubtitlingDescriptor.GetRecordSubtitlingType
title: IDvbSubtitlingDescriptor::GetRecordSubtitlingType (dvbsiparser.h)
description: Gets the subtitling component type from a DVB subtitling descriptor.
helpviewer_keywords: ["GetRecordSubtitlingType","GetRecordSubtitlingType method [Microsoft TV Technologies]","GetRecordSubtitlingType method [Microsoft TV Technologies]","IDvbSubtitlingDescriptor interface","IDvbSubtitlingDescriptor interface [Microsoft TV Technologies]","GetRecordSubtitlingType method","IDvbSubtitlingDescriptor.GetRecordSubtitlingType","IDvbSubtitlingDescriptor::GetRecordSubtitlingType","dvbsiparser/IDvbSubtitlingDescriptor::GetRecordSubtitlingType","mstv.idvbsubtitlingdescriptor_getrecordsubtitlingtype"]
old-location: mstv\idvbsubtitlingdescriptor_getrecordsubtitlingtype.htm
tech.root: mstv
ms.assetid: 5ab91508-9afe-4ab7-957f-5467e87ce7ee
ms.date: 12/05/2018
ms.keywords: GetRecordSubtitlingType, GetRecordSubtitlingType method [Microsoft TV Technologies], GetRecordSubtitlingType method [Microsoft TV Technologies],IDvbSubtitlingDescriptor interface, IDvbSubtitlingDescriptor interface [Microsoft TV Technologies],GetRecordSubtitlingType method, IDvbSubtitlingDescriptor.GetRecordSubtitlingType, IDvbSubtitlingDescriptor::GetRecordSubtitlingType, dvbsiparser/IDvbSubtitlingDescriptor::GetRecordSubtitlingType, mstv.idvbsubtitlingdescriptor_getrecordsubtitlingtype
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
 - IDvbSubtitlingDescriptor::GetRecordSubtitlingType
 - dvbsiparser/IDvbSubtitlingDescriptor::GetRecordSubtitlingType
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
 - IDvbSubtitlingDescriptor.GetRecordSubtitlingType
---

# IDvbSubtitlingDescriptor::GetRecordSubtitlingType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the subtitling component type from a DVB subtitling descriptor.

## -parameters

### -param bRecordIndex [in]

Zero-based index of the descriptor to return. To get the number of descriptors, call <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsubtitlingdescriptor-getcountofrecords">IDvbSubtitlingDescriptor::GetCountOfRecords</a>

### -param pbVal [out]

Receives the subtitling component type code. This can be any of the following values:

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
European Broadcasting Union (EBU) teletext subtitles

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
Associated EBU teletext

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x03</dt>
</dl>
</td>
<td width="60%">
Vertical blanking interval (VBI) data

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x04 - 0x0F</dt>
</dl>
</td>
<td width="60%">
Reserved for future use

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x10</dt>
</dl>
</td>
<td width="60%">
DVB subtitles (normal) with no monitor aspect ratio criticality

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x11</dt>
</dl>
</td>
<td width="60%">
DVB subtitles (normal) for display on 4:3 aspect ratio monitor

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x12</dt>
</dl>
</td>
<td width="60%">
DVB subtitles (normal) for display on 16:9 aspect ratio monitor

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x13</dt>
</dl>
</td>
<td width="60%">
DVB subtitles (normal) for display on 2.21:1 aspect ratio monitor

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x14 - 0x1F</dt>
</dl>
</td>
<td width="60%">
Reserved for future use

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x20</dt>
</dl>
</td>
<td width="60%">
DVB subtitles (for the hard-of-hearing) with no monitor aspect ratio criticality

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x21</dt>
</dl>
</td>
<td width="60%">
DVB subtitles (for the hard-of-hearing) for display on 4:3 aspect ratio monitor

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x22</dt>
</dl>
</td>
<td width="60%">
DVB subtitles (for the hard-of-hearing)  for display on 16:9 aspect ratio monitor

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x23</dt>
</dl>
</td>
<td width="60%">
DVB subtitles (for the hard-of-hearing)  for display on 2.21:1 aspect ratio monitor

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x24 - 0xAF</dt>
</dl>
</td>
<td width="60%">
Reserved for future use

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0xB0 - 0xFE</dt>
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

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbsubtitlingdescriptor">IDvbSubtitlingDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsubtitlingdescriptor-getcountofrecords">IDvbSubtitlingDescriptor::GetCountOfRecords</a>