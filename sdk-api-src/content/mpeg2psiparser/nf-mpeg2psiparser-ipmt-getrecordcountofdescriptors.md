---
UID: NF:mpeg2psiparser.IPMT.GetRecordCountOfDescriptors
title: IPMT::GetRecordCountOfDescriptors (mpeg2psiparser.h)
description: The GetRecordCountOfDescriptors method returns the number of descriptors for a record in the PMT.
helpviewer_keywords: ["GetRecordCountOfDescriptors","GetRecordCountOfDescriptors method [Microsoft TV Technologies]","GetRecordCountOfDescriptors method [Microsoft TV Technologies]","IPMT interface","IPMT interface [Microsoft TV Technologies]","GetRecordCountOfDescriptors method","IPMT.GetRecordCountOfDescriptors","IPMT::GetRecordCountOfDescriptors","IPMTGetRecordCountOfDescriptors","mpeg2psiparser/IPMT::GetRecordCountOfDescriptors","mstv.ipmt_getrecordcountofdescriptors"]
old-location: mstv\ipmt_getrecordcountofdescriptors.htm
tech.root: mstv
ms.assetid: b2470267-25a6-4ed3-91a1-30fd3ac7bbea
ms.date: 12/05/2018
ms.keywords: GetRecordCountOfDescriptors, GetRecordCountOfDescriptors method [Microsoft TV Technologies], GetRecordCountOfDescriptors method [Microsoft TV Technologies],IPMT interface, IPMT interface [Microsoft TV Technologies],GetRecordCountOfDescriptors method, IPMT.GetRecordCountOfDescriptors, IPMT::GetRecordCountOfDescriptors, IPMTGetRecordCountOfDescriptors, mpeg2psiparser/IPMT::GetRecordCountOfDescriptors, mstv.ipmt_getrecordcountofdescriptors
req.header: mpeg2psiparser.h
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
 - IPMT::GetRecordCountOfDescriptors
 - mpeg2psiparser/IPMT::GetRecordCountOfDescriptors
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mpeg2PsiParser.h
api_name:
 - IPMT.GetRecordCountOfDescriptors
---

# IPMT::GetRecordCountOfDescriptors


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetRecordCountOfDescriptors</b> method returns the number of descriptors for a record in the PMT.

## -parameters

### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipmt-getcountofrecords">IPMT::GetCountOfRecords</a> method to get the number of records in the PMT.

### -param pdwVal [out]

Receives the number of descriptors.

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

<a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-ipmt">IPMT Interface</a>