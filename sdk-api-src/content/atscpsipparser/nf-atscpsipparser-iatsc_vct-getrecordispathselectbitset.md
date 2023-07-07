---
UID: NF:atscpsipparser.IATSC_VCT.GetRecordIsPathSelectBitSet
title: IATSC_VCT::GetRecordIsPathSelectBitSet (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetRecordIsPathSelectBitSet","GetRecordIsPathSelectBitSet method [Microsoft TV Technologies]","GetRecordIsPathSelectBitSet method [Microsoft TV Technologies]","IATSC_VCT interface","IATSC_VCT interface [Microsoft TV Technologies]","GetRecordIsPathSelectBitSet method","IATSC_VCT.GetRecordIsPathSelectBitSet","IATSC_VCT::GetRecordIsPathSelectBitSet","IATSC_VCTGetRecordIsPathSelectBitSet","atscpsipparser/IATSC_VCT::GetRecordIsPathSelectBitSet","mstv.iatsc_vct_getrecordispathselectbitset"]
old-location: mstv\iatsc_vct_getrecordispathselectbitset.htm
tech.root: mstv
ms.assetid: 6f3e1e5c-0506-420d-981b-d30d77604e97
ms.date: 12/05/2018
ms.keywords: GetRecordIsPathSelectBitSet, GetRecordIsPathSelectBitSet method [Microsoft TV Technologies], GetRecordIsPathSelectBitSet method [Microsoft TV Technologies],IATSC_VCT interface, IATSC_VCT interface [Microsoft TV Technologies],GetRecordIsPathSelectBitSet method, IATSC_VCT.GetRecordIsPathSelectBitSet, IATSC_VCT::GetRecordIsPathSelectBitSet, IATSC_VCTGetRecordIsPathSelectBitSet, atscpsipparser/IATSC_VCT::GetRecordIsPathSelectBitSet, mstv.iatsc_vct_getrecordispathselectbitset
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
 - IATSC_VCT::GetRecordIsPathSelectBitSet
 - atscpsipparser/IATSC_VCT::GetRecordIsPathSelectBitSet
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
 - IATSC_VCT.GetRecordIsPathSelectBitSet
---

# IATSC_VCT::GetRecordIsPathSelectBitSet


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordIsPathSelectBitSet</b> method queries whether the path_select bit is set for a particular record in the VCT.

## -parameters

### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_vct-getcountofrecords">IATSC_VCT::GetCountOfRecords</a> method to get the number of records in the VCT.

### -param pfVal [out]

Receives a Boolean value. The value is <b>TRUE</b> if the path_select bit is set, or <b>FALSE</b> otherwise. The path_select bit indicates which physical input cable carries the transport stream.

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
<dt><b>MPEG2_E_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The table does not contain an out_of_band bit.

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

This bit applies only to cable VCTs. If the VCT is a terrestrial VCT, the method returns MPEG2_E_NOT_PRESENT.

## -see-also

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iatsc_vct">IATSC_VCT Interface</a>