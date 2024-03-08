---
UID: NF:dvbsiparser.IDVB_EIT.GetRecordCountOfDescriptors
title: IDVB_EIT::GetRecordCountOfDescriptors (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetRecordCountOfDescriptors","GetRecordCountOfDescriptors method [Microsoft TV Technologies]","GetRecordCountOfDescriptors method [Microsoft TV Technologies]","IDVB_EIT interface","IDVB_EIT interface [Microsoft TV Technologies]","GetRecordCountOfDescriptors method","IDVB_EIT.GetRecordCountOfDescriptors","IDVB_EIT::GetRecordCountOfDescriptors","IDVB_EITGetRecordCountOfDescriptors","dvbsiparser/IDVB_EIT::GetRecordCountOfDescriptors","mstv.idvb_eit_getrecordcountofdescriptors"]
old-location: mstv\idvb_eit_getrecordcountofdescriptors.htm
tech.root: mstv
ms.assetid: 85cb6ca7-552d-4d50-ac7f-4a0cb9ec4ad4
ms.date: 12/05/2018
ms.keywords: GetRecordCountOfDescriptors, GetRecordCountOfDescriptors method [Microsoft TV Technologies], GetRecordCountOfDescriptors method [Microsoft TV Technologies],IDVB_EIT interface, IDVB_EIT interface [Microsoft TV Technologies],GetRecordCountOfDescriptors method, IDVB_EIT.GetRecordCountOfDescriptors, IDVB_EIT::GetRecordCountOfDescriptors, IDVB_EITGetRecordCountOfDescriptors, dvbsiparser/IDVB_EIT::GetRecordCountOfDescriptors, mstv.idvb_eit_getrecordcountofdescriptors
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
 - IDVB_EIT::GetRecordCountOfDescriptors
 - dvbsiparser/IDVB_EIT::GetRecordCountOfDescriptors
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
 - IDVB_EIT.GetRecordCountOfDescriptors
---

# IDVB_EIT::GetRecordCountOfDescriptors


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordCountOfDescriptors</b> method returns the number of descriptors for a record in the EIT.

## -parameters

### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_eit-getcountofrecords">IDVB_EIT::GetCountOfRecords</a> to get the number of records in the EIT.

### -param pdwVal [out]

Pointer to a variable that receives the number of descriptors.

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

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_eit">IDVB_EIT Interface</a>