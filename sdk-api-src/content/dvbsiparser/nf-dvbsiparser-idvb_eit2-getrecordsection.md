---
UID: NF:dvbsiparser.IDVB_EIT2.GetRecordSection
title: IDVB_EIT2::GetRecordSection (dvbsiparser.h)
description: Gets the number of a section containing an event information table (EIT) record.
helpviewer_keywords: ["GetRecordSection","GetRecordSection method [Microsoft TV Technologies]","GetRecordSection method [Microsoft TV Technologies]","IDVB_EIT2 interface","IDVB_EIT2 interface [Microsoft TV Technologies]","GetRecordSection method","IDVB_EIT2.GetRecordSection","IDVB_EIT2::GetRecordSection","dvbsiparser/IDVB_EIT2::GetRecordSection","mstv.idvb_eit2_getrecordsection"]
old-location: mstv\idvb_eit2_getrecordsection.htm
tech.root: mstv
ms.assetid: 249c93f2-53d7-4110-9db3-34f3b0296b48
ms.date: 12/05/2018
ms.keywords: GetRecordSection, GetRecordSection method [Microsoft TV Technologies], GetRecordSection method [Microsoft TV Technologies],IDVB_EIT2 interface, IDVB_EIT2 interface [Microsoft TV Technologies],GetRecordSection method, IDVB_EIT2.GetRecordSection, IDVB_EIT2::GetRecordSection, dvbsiparser/IDVB_EIT2::GetRecordSection, mstv.idvb_eit2_getrecordsection
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
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
 - IDVB_EIT2::GetRecordSection
 - dvbsiparser/IDVB_EIT2::GetRecordSection
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
 - IDVB_EIT2.GetRecordSection
---

# IDVB_EIT2::GetRecordSection


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the number of a section containing an event information table (EIT) record.

## -parameters

### -param dwRecordIndex [in]

The record number, indexed from 0. Call <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_eit-getcountofrecords">IDVB_EIT::GetCountOfRecords</a> to get the number of records in the EIT.

### -param pbVal [out]

Receives the number of the section containing the specified record. A value of 0 indicates the present section; a value of 1 indicates the following section.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
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
<dt><b>MPEG2_E_UNINITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_eit-initialize">Initialize</a> method was not called.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_eit2">IDVB_EIT2</a>