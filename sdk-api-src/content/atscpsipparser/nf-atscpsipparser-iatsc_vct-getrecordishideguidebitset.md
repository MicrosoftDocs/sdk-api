---
UID: NF:atscpsipparser.IATSC_VCT.GetRecordIsHideGuideBitSet
title: IATSC_VCT::GetRecordIsHideGuideBitSet (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetRecordIsHideGuideBitSet","GetRecordIsHideGuideBitSet method [Microsoft TV Technologies]","GetRecordIsHideGuideBitSet method [Microsoft TV Technologies]","IATSC_VCT interface","IATSC_VCT interface [Microsoft TV Technologies]","GetRecordIsHideGuideBitSet method","IATSC_VCT.GetRecordIsHideGuideBitSet","IATSC_VCT::GetRecordIsHideGuideBitSet","IATSC_VCTGetRecordIsHideGuideBitSet","atscpsipparser/IATSC_VCT::GetRecordIsHideGuideBitSet","mstv.iatsc_vct_getrecordishideguidebitset"]
old-location: mstv\iatsc_vct_getrecordishideguidebitset.htm
tech.root: mstv
ms.assetid: 74b2ec97-f225-4085-910e-9093995c46f8
ms.date: 12/05/2018
ms.keywords: GetRecordIsHideGuideBitSet, GetRecordIsHideGuideBitSet method [Microsoft TV Technologies], GetRecordIsHideGuideBitSet method [Microsoft TV Technologies],IATSC_VCT interface, IATSC_VCT interface [Microsoft TV Technologies],GetRecordIsHideGuideBitSet method, IATSC_VCT.GetRecordIsHideGuideBitSet, IATSC_VCT::GetRecordIsHideGuideBitSet, IATSC_VCTGetRecordIsHideGuideBitSet, atscpsipparser/IATSC_VCT::GetRecordIsHideGuideBitSet, mstv.iatsc_vct_getrecordishideguidebitset
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
 - IATSC_VCT::GetRecordIsHideGuideBitSet
 - atscpsipparser/IATSC_VCT::GetRecordIsHideGuideBitSet
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
 - IATSC_VCT.GetRecordIsHideGuideBitSet
---

# IATSC_VCT::GetRecordIsHideGuideBitSet


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordIsHideGuideBitSet</b> method queries whether the hide_guide bit is set for a particular record in the VCT.

## -parameters

### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_vct-getcountofrecords">IATSC_VCT::GetCountOfRecords</a> method to get the number of records in the VCT.

### -param pfVal [out]

Receives a Boolean value. The value is <b>TRUE</b> if the hide_guide bit is set, or <b>FALSE</b> otherwise.

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

## -remarks

If the hidden bit is set, the hide_guide bit may be set to 0, indicating that this virtual channel should appear in electronic program guide (EPG) displays. If the hidden bit is 0, the hide_guide bit is ignored.

## -see-also

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iatsc_vct">IATSC_VCT Interface</a>



<a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_vct-getrecordishiddenbitset">IATSC_VCT::GetRecordIsHiddenBitSet</a>