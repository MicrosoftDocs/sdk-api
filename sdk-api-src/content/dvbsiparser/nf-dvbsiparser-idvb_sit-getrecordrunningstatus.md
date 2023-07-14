---
UID: NF:dvbsiparser.IDVB_SIT.GetRecordRunningStatus
title: IDVB_SIT::GetRecordRunningStatus (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetRecordRunningStatus","GetRecordRunningStatus method [Microsoft TV Technologies]","GetRecordRunningStatus method [Microsoft TV Technologies]","IDVB_SIT interface","IDVB_SIT interface [Microsoft TV Technologies]","GetRecordRunningStatus method","IDVB_SIT.GetRecordRunningStatus","IDVB_SIT::GetRecordRunningStatus","IDVB_SITGetRecordRunningStatus","dvbsiparser/IDVB_SIT::GetRecordRunningStatus","mstv.idvb_sit_getrecordrunningstatus"]
old-location: mstv\idvb_sit_getrecordrunningstatus.htm
tech.root: mstv
ms.assetid: 223b7f11-b2fa-4f63-9c9d-bee02e721670
ms.date: 12/05/2018
ms.keywords: GetRecordRunningStatus, GetRecordRunningStatus method [Microsoft TV Technologies], GetRecordRunningStatus method [Microsoft TV Technologies],IDVB_SIT interface, IDVB_SIT interface [Microsoft TV Technologies],GetRecordRunningStatus method, IDVB_SIT.GetRecordRunningStatus, IDVB_SIT::GetRecordRunningStatus, IDVB_SITGetRecordRunningStatus, dvbsiparser/IDVB_SIT::GetRecordRunningStatus, mstv.idvb_sit_getrecordrunningstatus
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
 - IDVB_SIT::GetRecordRunningStatus
 - dvbsiparser/IDVB_SIT::GetRecordRunningStatus
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
 - IDVB_SIT.GetRecordRunningStatus
---

# IDVB_SIT::GetRecordRunningStatus


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordRunningStatus</b> method returns the running status of a particular event in the SIT.

## -parameters

### -param dwRecordIndex [in]

Specifies the record number for the event, indexed from zero. Call <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_sit-getcountofrecords">IDVB_SIT::GetCountOfRecords</a> to get the number of records in the SIT.

### -param pbVal [out]

Pointer to a variable that receives the running_status field. See the Remarks section in the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_rst-getrecordrunningstatus">IDVB_RST::GetRecordRunningStatus</a> method for more information.

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

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_sit">IDVB_SIT Interface</a>