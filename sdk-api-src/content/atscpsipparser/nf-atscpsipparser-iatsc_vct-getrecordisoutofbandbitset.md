---
UID: NF:atscpsipparser.IATSC_VCT.GetRecordIsOutOfBandBitSet
title: IATSC_VCT::GetRecordIsOutOfBandBitSet (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetRecordIsOutOfBandBitSet","GetRecordIsOutOfBandBitSet method [Microsoft TV Technologies]","GetRecordIsOutOfBandBitSet method [Microsoft TV Technologies]","IATSC_VCT interface","IATSC_VCT interface [Microsoft TV Technologies]","GetRecordIsOutOfBandBitSet method","IATSC_VCT.GetRecordIsOutOfBandBitSet","IATSC_VCT::GetRecordIsOutOfBandBitSet","IATSC_VCTGetRecordIsOutOfBandBitSet","atscpsipparser/IATSC_VCT::GetRecordIsOutOfBandBitSet","mstv.iatsc_vct_getrecordisoutofbandbitset"]
old-location: mstv\iatsc_vct_getrecordisoutofbandbitset.htm
tech.root: mstv
ms.assetid: cb4dc4f0-2bbb-44f6-b45e-347cce890b75
ms.date: 12/05/2018
ms.keywords: GetRecordIsOutOfBandBitSet, GetRecordIsOutOfBandBitSet method [Microsoft TV Technologies], GetRecordIsOutOfBandBitSet method [Microsoft TV Technologies],IATSC_VCT interface, IATSC_VCT interface [Microsoft TV Technologies],GetRecordIsOutOfBandBitSet method, IATSC_VCT.GetRecordIsOutOfBandBitSet, IATSC_VCT::GetRecordIsOutOfBandBitSet, IATSC_VCTGetRecordIsOutOfBandBitSet, atscpsipparser/IATSC_VCT::GetRecordIsOutOfBandBitSet, mstv.iatsc_vct_getrecordisoutofbandbitset
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
 - IATSC_VCT::GetRecordIsOutOfBandBitSet
 - atscpsipparser/IATSC_VCT::GetRecordIsOutOfBandBitSet
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
 - IATSC_VCT.GetRecordIsOutOfBandBitSet
---

# IATSC_VCT::GetRecordIsOutOfBandBitSet


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordIsOutOfBandBitSet</b> method queries whether the out_of_band bit is set for a particular record in the VCT.

## -parameters

### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_vct-getcountofrecords">IATSC_VCT::GetCountOfRecords</a> method to get the number of records in the VCT.

### -param pfVal [out]

Receives a Boolean value. The value is <b>TRUE</b> if the out_of_band bit is set, indicating that this channel is carried on an out-of-band physical transmission channel. Otherwise, the value is <b>FALSE</b>.

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