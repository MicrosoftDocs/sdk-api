---
UID: NF:dvbsiparser.IDVB_RST.GetRecordRunningStatus
title: IDVB_RST::GetRecordRunningStatus (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetRecordRunningStatus","GetRecordRunningStatus method [Microsoft TV Technologies]","GetRecordRunningStatus method [Microsoft TV Technologies]","IDVB_RST interface","IDVB_RST interface [Microsoft TV Technologies]","GetRecordRunningStatus method","IDVB_RST.GetRecordRunningStatus","IDVB_RST::GetRecordRunningStatus","IDVB_RSTGetRecordRunningStatus","dvbsiparser/IDVB_RST::GetRecordRunningStatus","mstv.idvb_rst_getrecordrunningstatus"]
old-location: mstv\idvb_rst_getrecordrunningstatus.htm
tech.root: mstv
ms.assetid: ca0a0b3b-14a8-4456-85a0-51df559d04b8
ms.date: 12/05/2018
ms.keywords: GetRecordRunningStatus, GetRecordRunningStatus method [Microsoft TV Technologies], GetRecordRunningStatus method [Microsoft TV Technologies],IDVB_RST interface, IDVB_RST interface [Microsoft TV Technologies],GetRecordRunningStatus method, IDVB_RST.GetRecordRunningStatus, IDVB_RST::GetRecordRunningStatus, IDVB_RSTGetRecordRunningStatus, dvbsiparser/IDVB_RST::GetRecordRunningStatus, mstv.idvb_rst_getrecordrunningstatus
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
 - IDVB_RST::GetRecordRunningStatus
 - dvbsiparser/IDVB_RST::GetRecordRunningStatus
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
 - IDVB_RST.GetRecordRunningStatus
---

# IDVB_RST::GetRecordRunningStatus


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordRunningStatus</b> method returns the running status for a record in the RST.

## -parameters

### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_rst-getcountofrecords">IDVB_RST::GetCountOfRecords</a> method to get the number of records in the RST.

### -param pbVal [out]

Pointer to a variable that receives the running_status field.

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

## -remarks

ETSI EN 300 468 defines the following values for the running_status field.

<table>
<tr>
<th>Value
            </th>
<th>Description
            </th>
</tr>
<tr>
<td>0</td>
<td>Undefined.</td>
</tr>
<tr>
<td>1</td>
<td>Not running.</td>
</tr>
<tr>
<td>2</td>
<td>Starts in a few seconds.</td>
</tr>
<tr>
<td>3</td>
<td>Pausing.</td>
</tr>
<tr>
<td>4</td>
<td>Running.</td>
</tr>
<tr>
<td>5 to 7</td>
<td>Reserved.</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_rst">IDVB_RST Interface</a>