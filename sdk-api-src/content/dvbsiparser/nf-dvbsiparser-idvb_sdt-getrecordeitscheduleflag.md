---
UID: NF:dvbsiparser.IDVB_SDT.GetRecordEITScheduleFlag
title: IDVB_SDT::GetRecordEITScheduleFlag (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetRecordEITScheduleFlag","GetRecordEITScheduleFlag method [Microsoft TV Technologies]","GetRecordEITScheduleFlag method [Microsoft TV Technologies]","IDVB_SDT interface","IDVB_SDT interface [Microsoft TV Technologies]","GetRecordEITScheduleFlag method","IDVB_SDT.GetRecordEITScheduleFlag","IDVB_SDT::GetRecordEITScheduleFlag","IDVB_SDTGetRecordEITScheduleFlag","dvbsiparser/IDVB_SDT::GetRecordEITScheduleFlag","mstv.idvb_sdt_getrecordeitscheduleflag"]
old-location: mstv\idvb_sdt_getrecordeitscheduleflag.htm
tech.root: mstv
ms.assetid: 6f78ebf4-d882-4fdd-90a0-52ad3cd9ca1e
ms.date: 12/05/2018
ms.keywords: GetRecordEITScheduleFlag, GetRecordEITScheduleFlag method [Microsoft TV Technologies], GetRecordEITScheduleFlag method [Microsoft TV Technologies],IDVB_SDT interface, IDVB_SDT interface [Microsoft TV Technologies],GetRecordEITScheduleFlag method, IDVB_SDT.GetRecordEITScheduleFlag, IDVB_SDT::GetRecordEITScheduleFlag, IDVB_SDTGetRecordEITScheduleFlag, dvbsiparser/IDVB_SDT::GetRecordEITScheduleFlag, mstv.idvb_sdt_getrecordeitscheduleflag
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
 - IDVB_SDT::GetRecordEITScheduleFlag
 - dvbsiparser/IDVB_SDT::GetRecordEITScheduleFlag
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
 - IDVB_SDT.GetRecordEITScheduleFlag
---

# IDVB_SDT::GetRecordEITScheduleFlag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordEITScheduleFlag</b> method queries whether the current transport stream contains schedule EIT information for a particular service.

## -parameters

### -param dwRecordIndex [in]

Specifies the record number for the service, indexed from zero. Call <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_sdt-getcountofrecords">IDVB_SDT::GetCountOfRecords</a> to get the number of records in the SDT.

### -param pfVal [out]

Pointer to a variable that receives a Boolean value. The value is <b>TRUE</b> if the EIT_schedule_flag bit is set, or <b>FALSE</b> otherwise. The value <b>TRUE</b> indicates that the current transport stream contains schedule EIT information for the service.

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
<b>NULL</b> pointer argument.

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