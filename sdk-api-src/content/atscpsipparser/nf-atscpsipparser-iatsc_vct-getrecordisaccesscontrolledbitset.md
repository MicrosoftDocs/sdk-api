---
UID: NF:atscpsipparser.IATSC_VCT.GetRecordIsAccessControlledBitSet
title: IATSC_VCT::GetRecordIsAccessControlledBitSet (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetRecordIsAccessControlledBitSet","GetRecordIsAccessControlledBitSet method [Microsoft TV Technologies]","GetRecordIsAccessControlledBitSet method [Microsoft TV Technologies]","IATSC_VCT interface","IATSC_VCT interface [Microsoft TV Technologies]","GetRecordIsAccessControlledBitSet method","IATSC_VCT.GetRecordIsAccessControlledBitSet","IATSC_VCT::GetRecordIsAccessControlledBitSet","IATSC_VCTGetRecordIsAccessControlledBitSet","atscpsipparser/IATSC_VCT::GetRecordIsAccessControlledBitSet","mstv.iatsc_vct_getrecordisaccesscontrolledbitset"]
old-location: mstv\iatsc_vct_getrecordisaccesscontrolledbitset.htm
tech.root: mstv
ms.assetid: c94dc694-dc3f-4639-997e-fb6d534c9e4c
ms.date: 12/05/2018
ms.keywords: GetRecordIsAccessControlledBitSet, GetRecordIsAccessControlledBitSet method [Microsoft TV Technologies], GetRecordIsAccessControlledBitSet method [Microsoft TV Technologies],IATSC_VCT interface, IATSC_VCT interface [Microsoft TV Technologies],GetRecordIsAccessControlledBitSet method, IATSC_VCT.GetRecordIsAccessControlledBitSet, IATSC_VCT::GetRecordIsAccessControlledBitSet, IATSC_VCTGetRecordIsAccessControlledBitSet, atscpsipparser/IATSC_VCT::GetRecordIsAccessControlledBitSet, mstv.iatsc_vct_getrecordisaccesscontrolledbitset
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
 - IATSC_VCT::GetRecordIsAccessControlledBitSet
 - atscpsipparser/IATSC_VCT::GetRecordIsAccessControlledBitSet
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
 - IATSC_VCT.GetRecordIsAccessControlledBitSet
---

# IATSC_VCT::GetRecordIsAccessControlledBitSet


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordIsAccessControlledBitSet</b> method queries whether the access_controlled bit is set for a particular record in the VCT.

## -parameters

### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_vct-getcountofrecords">IATSC_VCT::GetCountOfRecords</a> method to get the number of records in the VCT.

### -param pfVal [out]

Receives a Boolean value. The value is <b>TRUE</b> if the access_controlled bit is set, indicating that this virtual channel might be access controlled. Otherwise, the value is <b>FALSE</b>, indicating that access is not restricted.

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

## -see-also

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iatsc_vct">IATSC_VCT Interface</a>