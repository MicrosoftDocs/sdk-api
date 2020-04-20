---
UID: NF:atscpsipparser.IATSC_MGT.GetRecordType
title: IATSC_MGT::GetRecordType (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.helpviewer_keywords: ["GetRecordType","GetRecordType method [Microsoft TV Technologies]","GetRecordType method [Microsoft TV Technologies]","IATSC_MGT interface","IATSC_MGT interface [Microsoft TV Technologies]","GetRecordType method","IATSC_MGT.GetRecordType","IATSC_MGT::GetRecordType","IATSC_MGTGetRecordType","atscpsipparser/IATSC_MGT::GetRecordType","mstv.iatsc_mgt_getrecordtype"]
old-location: mstv\iatsc_mgt_getrecordtype.htm
tech.root: mstv
ms.assetid: f3a1ef39-7de4-4979-acb9-805893f41937
ms.date: 12/05/2018
ms.keywords: GetRecordType, GetRecordType method [Microsoft TV Technologies], GetRecordType method [Microsoft TV Technologies],IATSC_MGT interface, IATSC_MGT interface [Microsoft TV Technologies],GetRecordType method, IATSC_MGT.GetRecordType, IATSC_MGT::GetRecordType, IATSC_MGTGetRecordType, atscpsipparser/IATSC_MGT::GetRecordType, mstv.iatsc_mgt_getrecordtype
f1_keywords:
- atscpsipparser/IATSC_MGT.GetRecordType
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- atscpsipparser.h
api_name:
- IATSC_MGT.GetRecordType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IATSC_MGT::GetRecordType


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordType</b> method returns the table type for a record in the MGT.


## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_mgt-getcountofrecords">IATSC_MGT::GetCountOfRecords</a> method to get the number of records in the MGT.


### -param pwVal [out]

Receives the table_type field.


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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iatsc_mgt">IATSC_MGT Interface</a>
 

 

