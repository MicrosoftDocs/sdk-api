---
UID: NF:dvbsiparser.IDVB_SDT.GetTransportStreamId
title: IDVB_SDT::GetTransportStreamId (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetTransportStreamId","GetTransportStreamId method [Microsoft TV Technologies]","GetTransportStreamId method [Microsoft TV Technologies]","IDVB_SDT interface","IDVB_SDT interface [Microsoft TV Technologies]","GetTransportStreamId method","IDVB_SDT.GetTransportStreamId","IDVB_SDT::GetTransportStreamId","IDVB_SDTGetTransportStreamId","dvbsiparser/IDVB_SDT::GetTransportStreamId","mstv.idvb_sdt_gettransportstreamid"]
old-location: mstv\idvb_sdt_gettransportstreamid.htm
tech.root: mstv
ms.assetid: a4ecaf56-bc2b-46f3-94e7-aae63ad9be06
ms.date: 12/05/2018
ms.keywords: GetTransportStreamId, GetTransportStreamId method [Microsoft TV Technologies], GetTransportStreamId method [Microsoft TV Technologies],IDVB_SDT interface, IDVB_SDT interface [Microsoft TV Technologies],GetTransportStreamId method, IDVB_SDT.GetTransportStreamId, IDVB_SDT::GetTransportStreamId, IDVB_SDTGetTransportStreamId, dvbsiparser/IDVB_SDT::GetTransportStreamId, mstv.idvb_sdt_gettransportstreamid
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
 - IDVB_SDT::GetTransportStreamId
 - dvbsiparser/IDVB_SDT::GetTransportStreamId
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
 - IDVB_SDT.GetTransportStreamId
---

# IDVB_SDT::GetTransportStreamId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetTransportStreamId</b> method returns the transport stream identifier (TSID) for the SDT.

## -parameters

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_sdt">IDVB_SDT Interface</a>