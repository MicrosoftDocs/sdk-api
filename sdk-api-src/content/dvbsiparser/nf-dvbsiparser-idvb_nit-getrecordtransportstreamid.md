---
UID: NF:dvbsiparser.IDVB_NIT.GetRecordTransportStreamId
title: IDVB_NIT::GetRecordTransportStreamId (dvbsiparser.h)
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_nit_getrecordtransportstreamid.htm
tech.root: mstv
ms.assetid: ed2b9fcc-fd7d-4477-9ff5-cbb7912eac26
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetRecordTransportStreamId, GetRecordTransportStreamId method [Microsoft TV Technologies], GetRecordTransportStreamId method [Microsoft TV Technologies],IDVB_NIT interface, IDVB_NIT interface [Microsoft TV Technologies],GetRecordTransportStreamId method, IDVB_NIT.GetRecordTransportStreamId, IDVB_NIT::GetRecordTransportStreamId, IDVB_NITGetRecordTransportStreamId, dvbsiparser/IDVB_NIT::GetRecordTransportStreamId, mstv.idvb_nit_getrecordtransportstreamid
ms.topic: method
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
 - IDVB_NIT.GetRecordTransportStreamId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDVB_NIT::GetRecordTransportStreamId


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordTransportStreamId</b> method returns the transport stream identifier (TSID) for a record in the NIT.


## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="https://msdn.microsoft.com/fb0f8071-575a-4bbd-b34b-b8d92c17c476">IDVB_NIT::GetCountOfRecords</a> method to get the number of records in the NIT.


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




<a href="https://msdn.microsoft.com/70b638ae-0152-4a44-aeb1-f3ac382c19ce">IDVB_NIT Interface</a>
 

 

