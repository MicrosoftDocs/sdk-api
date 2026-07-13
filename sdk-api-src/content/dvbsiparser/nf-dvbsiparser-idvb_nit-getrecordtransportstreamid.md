---
UID: NF:dvbsiparser.IDVB_NIT.GetRecordTransportStreamId
title: IDVB_NIT::GetRecordTransportStreamId (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetRecordTransportStreamId","GetRecordTransportStreamId method [Microsoft TV Technologies]","GetRecordTransportStreamId method [Microsoft TV Technologies]","IDVB_NIT interface","IDVB_NIT interface [Microsoft TV Technologies]","GetRecordTransportStreamId method","IDVB_NIT.GetRecordTransportStreamId","IDVB_NIT::GetRecordTransportStreamId","IDVB_NITGetRecordTransportStreamId","dvbsiparser/IDVB_NIT::GetRecordTransportStreamId","mstv.idvb_nit_getrecordtransportstreamid"]
old-location: mstv\idvb_nit_getrecordtransportstreamid.htm
tech.root: mstv
ms.assetid: ed2b9fcc-fd7d-4477-9ff5-cbb7912eac26
ms.date: 12/05/2018
ms.keywords: GetRecordTransportStreamId, GetRecordTransportStreamId method [Microsoft TV Technologies], GetRecordTransportStreamId method [Microsoft TV Technologies],IDVB_NIT interface, IDVB_NIT interface [Microsoft TV Technologies],GetRecordTransportStreamId method, IDVB_NIT.GetRecordTransportStreamId, IDVB_NIT::GetRecordTransportStreamId, IDVB_NITGetRecordTransportStreamId, dvbsiparser/IDVB_NIT::GetRecordTransportStreamId, mstv.idvb_nit_getrecordtransportstreamid
req.header: dvbsiparser.h
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
 - IDVB_NIT::GetRecordTransportStreamId
 - dvbsiparser/IDVB_NIT::GetRecordTransportStreamId
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
 - IDVB_NIT.GetRecordTransportStreamId
---

# IDVB_NIT::GetRecordTransportStreamId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordTransportStreamId</b> method returns the transport stream identifier (TSID) for a record in the NIT.

## -parameters

### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_nit-getcountofrecords">IDVB_NIT::GetCountOfRecords</a> method to get the number of records in the NIT.

### -param pwVal [out]

Pointer to a variable that receives the transport_stream_id field. This value identifies the transport stream from other transport streams in the multiplex.

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

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_nit">IDVB_NIT Interface</a>