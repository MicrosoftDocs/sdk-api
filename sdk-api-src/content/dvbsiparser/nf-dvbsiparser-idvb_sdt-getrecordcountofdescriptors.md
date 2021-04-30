---
UID: NF:dvbsiparser.IDVB_SDT.GetRecordCountOfDescriptors
title: IDVB_SDT::GetRecordCountOfDescriptors (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetRecordCountOfDescriptors","GetRecordCountOfDescriptors method [Microsoft TV Technologies]","GetRecordCountOfDescriptors method [Microsoft TV Technologies]","IDVB_SDT interface","IDVB_SDT interface [Microsoft TV Technologies]","GetRecordCountOfDescriptors method","IDVB_SDT.GetRecordCountOfDescriptors","IDVB_SDT::GetRecordCountOfDescriptors","IDVB_SDTGetRecordCountOfDescriptors","dvbsiparser/IDVB_SDT::GetRecordCountOfDescriptors","mstv.idvb_sdt_getrecordcountofdescriptors"]
old-location: mstv\idvb_sdt_getrecordcountofdescriptors.htm
tech.root: mstv
ms.assetid: 99b7e2ab-c829-4e42-805b-e1ea5b725f82
ms.date: 12/05/2018
ms.keywords: GetRecordCountOfDescriptors, GetRecordCountOfDescriptors method [Microsoft TV Technologies], GetRecordCountOfDescriptors method [Microsoft TV Technologies],IDVB_SDT interface, IDVB_SDT interface [Microsoft TV Technologies],GetRecordCountOfDescriptors method, IDVB_SDT.GetRecordCountOfDescriptors, IDVB_SDT::GetRecordCountOfDescriptors, IDVB_SDTGetRecordCountOfDescriptors, dvbsiparser/IDVB_SDT::GetRecordCountOfDescriptors, mstv.idvb_sdt_getrecordcountofdescriptors
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
 - IDVB_SDT::GetRecordCountOfDescriptors
 - dvbsiparser/IDVB_SDT::GetRecordCountOfDescriptors
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
 - IDVB_SDT.GetRecordCountOfDescriptors
---

# IDVB_SDT::GetRecordCountOfDescriptors


## -description

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordCountOfDescriptors</b> method returns the number of descriptors for a record in the SDT.

## -parameters

### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_sdt-getcountofrecords">IDVB_SDT::GetCountOfRecords</a> to get the number of records in the SDT.

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

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_sdt">IDVB_SDT Interface</a>