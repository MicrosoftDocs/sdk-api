---
UID: NF:atscpsipparser.IATSC_EIT.GetRecordCountOfDescriptors
title: IATSC_EIT::GetRecordCountOfDescriptors (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetRecordCountOfDescriptors","GetRecordCountOfDescriptors method [Microsoft TV Technologies]","GetRecordCountOfDescriptors method [Microsoft TV Technologies]","IATSC_EIT interface","IATSC_EIT interface [Microsoft TV Technologies]","GetRecordCountOfDescriptors method","IATSC_EIT.GetRecordCountOfDescriptors","IATSC_EIT::GetRecordCountOfDescriptors","IATSC_EITGetRecordCountOfDescriptors","atscpsipparser/IATSC_EIT::GetRecordCountOfDescriptors","mstv.iatsc_eit_getrecordcountofdescriptors"]
old-location: mstv\iatsc_eit_getrecordcountofdescriptors.htm
tech.root: mstv
ms.assetid: fd568711-c82c-4ffe-9333-2b729502fe79
ms.date: 12/05/2018
ms.keywords: GetRecordCountOfDescriptors, GetRecordCountOfDescriptors method [Microsoft TV Technologies], GetRecordCountOfDescriptors method [Microsoft TV Technologies],IATSC_EIT interface, IATSC_EIT interface [Microsoft TV Technologies],GetRecordCountOfDescriptors method, IATSC_EIT.GetRecordCountOfDescriptors, IATSC_EIT::GetRecordCountOfDescriptors, IATSC_EITGetRecordCountOfDescriptors, atscpsipparser/IATSC_EIT::GetRecordCountOfDescriptors, mstv.iatsc_eit_getrecordcountofdescriptors
req.header: atscpsipparser.h
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
 - IATSC_EIT::GetRecordCountOfDescriptors
 - atscpsipparser/IATSC_EIT::GetRecordCountOfDescriptors
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - atscpsipparser.h
api_name:
 - IATSC_EIT.GetRecordCountOfDescriptors
---

# IATSC_EIT::GetRecordCountOfDescriptors


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordCountOfDescriptors</b> method returns the number of descriptors for a record in the EIT.

## -parameters

### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_eit-getcountofrecords">IATSC_EIT::GetCountOfRecords</a> method to get the number of records in the EIT.

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

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iatsc_eit">IATSC_EIT Interface</a>