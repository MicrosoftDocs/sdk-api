---
UID: NF:atscpsipparser.IATSC_VCT.GetRecordTransportStreamId
title: IATSC_VCT::GetRecordTransportStreamId (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetRecordTransportStreamId","GetRecordTransportStreamId method [Microsoft TV Technologies]","GetRecordTransportStreamId method [Microsoft TV Technologies]","IATSC_VCT interface","IATSC_VCT interface [Microsoft TV Technologies]","GetRecordTransportStreamId method","IATSC_VCT.GetRecordTransportStreamId","IATSC_VCT::GetRecordTransportStreamId","IATSC_VCTGetRecordTransportStreamId","atscpsipparser/IATSC_VCT::GetRecordTransportStreamId","mstv.iatsc_vct_getrecordtransportstreamid"]
old-location: mstv\iatsc_vct_getrecordtransportstreamid.htm
tech.root: mstv
ms.assetid: f0ecd931-d789-41cd-8056-675e6162a5f1
ms.date: 12/05/2018
ms.keywords: GetRecordTransportStreamId, GetRecordTransportStreamId method [Microsoft TV Technologies], GetRecordTransportStreamId method [Microsoft TV Technologies],IATSC_VCT interface, IATSC_VCT interface [Microsoft TV Technologies],GetRecordTransportStreamId method, IATSC_VCT.GetRecordTransportStreamId, IATSC_VCT::GetRecordTransportStreamId, IATSC_VCTGetRecordTransportStreamId, atscpsipparser/IATSC_VCT::GetRecordTransportStreamId, mstv.iatsc_vct_getrecordtransportstreamid
req.header: atscpsipparser.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IATSC_VCT::GetRecordTransportStreamId
 - atscpsipparser/IATSC_VCT::GetRecordTransportStreamId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - atscpsipparser.h
api_name:
 - IATSC_VCT.GetRecordTransportStreamId
---

# IATSC_VCT::GetRecordTransportStreamId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordTransportStreamId</b> method returns the transport stream identifier (TSID) for a specified channel.

## -parameters

### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_vct-getcountofrecords">IATSC_VCT::GetCountOfRecords</a> method to get the number of records in the VCT.

### -param pwVal [out]

Receives the channel_TSID field. This value represents the TSID associated with the transport stream that carries the MPEG-2 program for this virtual channel.

## -returns

The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_OUT_OF_BOUNDS</b></dt>
</dl>
</td>
<td width="60%">
Index out of bounds.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iatsc_vct">IATSC_VCT Interface</a>