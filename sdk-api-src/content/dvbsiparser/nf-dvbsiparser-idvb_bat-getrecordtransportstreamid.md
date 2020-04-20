---
UID: NF:dvbsiparser.IDVB_BAT.GetRecordTransportStreamId
title: IDVB_BAT::GetRecordTransportStreamId (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.helpviewer_keywords: ["GetRecordTransportStreamId","GetRecordTransportStreamId method [Microsoft TV Technologies]","GetRecordTransportStreamId method [Microsoft TV Technologies]","IDVB_BAT interface","IDVB_BAT interface [Microsoft TV Technologies]","GetRecordTransportStreamId method","IDVB_BAT.GetRecordTransportStreamId","IDVB_BAT::GetRecordTransportStreamId","IDVB_BATGetRecordTransportStreamId","dvbsiparser/IDVB_BAT::GetRecordTransportStreamId","mstv.idvb_bat_getrecordtransportstreamid"]
old-location: mstv\idvb_bat_getrecordtransportstreamid.htm
tech.root: mstv
ms.assetid: fdb406d1-5242-4f3e-a1c9-b10296d98d67
ms.date: 12/05/2018
ms.keywords: GetRecordTransportStreamId, GetRecordTransportStreamId method [Microsoft TV Technologies], GetRecordTransportStreamId method [Microsoft TV Technologies],IDVB_BAT interface, IDVB_BAT interface [Microsoft TV Technologies],GetRecordTransportStreamId method, IDVB_BAT.GetRecordTransportStreamId, IDVB_BAT::GetRecordTransportStreamId, IDVB_BATGetRecordTransportStreamId, dvbsiparser/IDVB_BAT::GetRecordTransportStreamId, mstv.idvb_bat_getrecordtransportstreamid
f1_keywords:
- dvbsiparser/IDVB_BAT.GetRecordTransportStreamId
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dvbsiparser.h
api_name:
- IDVB_BAT.GetRecordTransportStreamId
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDVB_BAT::GetRecordTransportStreamId


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordTransportStreamId</b> method returns the transport stream identifier (TSID) for a record in the BAT.


## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_bat-getcountofrecords">IDVB_BAT::GetCountOfRecords</a> method to get the number of records in the BAT.


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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_bat">IDVB_BAT Interface</a>
 

 

