---
UID: NF:dvbsiparser.IDVB_SDT.GetRecordServiceId
title: IDVB_SDT::GetRecordServiceId (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetRecordServiceId","GetRecordServiceId method [Microsoft TV Technologies]","GetRecordServiceId method [Microsoft TV Technologies]","IDVB_SDT interface","IDVB_SDT interface [Microsoft TV Technologies]","GetRecordServiceId method","IDVB_SDT.GetRecordServiceId","IDVB_SDT::GetRecordServiceId","IDVB_SDTGetRecordServiceId","dvbsiparser/IDVB_SDT::GetRecordServiceId","mstv.idvb_sdt_getrecordserviceid"]
old-location: mstv\idvb_sdt_getrecordserviceid.htm
tech.root: mstv
ms.assetid: a5d93d66-f9a6-439c-b0a5-9310d4fa6d88
ms.date: 12/05/2018
ms.keywords: GetRecordServiceId, GetRecordServiceId method [Microsoft TV Technologies], GetRecordServiceId method [Microsoft TV Technologies],IDVB_SDT interface, IDVB_SDT interface [Microsoft TV Technologies],GetRecordServiceId method, IDVB_SDT.GetRecordServiceId, IDVB_SDT::GetRecordServiceId, IDVB_SDTGetRecordServiceId, dvbsiparser/IDVB_SDT::GetRecordServiceId, mstv.idvb_sdt_getrecordserviceid
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
 - IDVB_SDT::GetRecordServiceId
 - dvbsiparser/IDVB_SDT::GetRecordServiceId
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
 - IDVB_SDT.GetRecordServiceId
---

# IDVB_SDT::GetRecordServiceId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordServiceId</b> method returns the service identifier for a record in the SDT.

## -parameters

### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_sdt-getcountofrecords">IDVB_SDT::GetCountOfRecords</a> to get the number of records in the SDT.

### -param pwVal [out]

Pointer to a variable that receives the service_id field.

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

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_sdt">IDVB_SDT Interface</a>