---
UID: NF:atscpsipparser.IATSC_MGT.GetRecordTypePid
title: IATSC_MGT::GetRecordTypePid (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetRecordTypePid","GetRecordTypePid method [Microsoft TV Technologies]","GetRecordTypePid method [Microsoft TV Technologies]","IATSC_MGT interface","IATSC_MGT interface [Microsoft TV Technologies]","GetRecordTypePid method","IATSC_MGT.GetRecordTypePid","IATSC_MGT::GetRecordTypePid","IATSC_MGTGetRecordTypePid","atscpsipparser/IATSC_MGT::GetRecordTypePid","mstv.iatsc_mgt_getrecordtypepid"]
old-location: mstv\iatsc_mgt_getrecordtypepid.htm
tech.root: mstv
ms.assetid: c8c4cfba-b03c-478e-a49e-c01d663535a0
ms.date: 12/05/2018
ms.keywords: GetRecordTypePid, GetRecordTypePid method [Microsoft TV Technologies], GetRecordTypePid method [Microsoft TV Technologies],IATSC_MGT interface, IATSC_MGT interface [Microsoft TV Technologies],GetRecordTypePid method, IATSC_MGT.GetRecordTypePid, IATSC_MGT::GetRecordTypePid, IATSC_MGTGetRecordTypePid, atscpsipparser/IATSC_MGT::GetRecordTypePid, mstv.iatsc_mgt_getrecordtypepid
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
 - IATSC_MGT::GetRecordTypePid
 - atscpsipparser/IATSC_MGT::GetRecordTypePid
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
 - IATSC_MGT.GetRecordTypePid
---

# IATSC_MGT::GetRecordTypePid


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordTypePid</b> method returns the packet identifier (PID) for the table type described by a record in the MGT.

## -parameters

### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_mgt-getcountofrecords">IATSC_MGT::GetCountOfRecords</a> method to get the number of records in the MGT.

### -param ppidVal [out]

Receives the table_type_PID field.

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

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iatsc_mgt">IATSC_MGT Interface</a>