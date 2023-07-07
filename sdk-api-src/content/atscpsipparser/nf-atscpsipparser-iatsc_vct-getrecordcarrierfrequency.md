---
UID: NF:atscpsipparser.IATSC_VCT.GetRecordCarrierFrequency
title: IATSC_VCT::GetRecordCarrierFrequency (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetRecordCarrierFrequency","GetRecordCarrierFrequency method [Microsoft TV Technologies]","GetRecordCarrierFrequency method [Microsoft TV Technologies]","IATSC_VCT interface","IATSC_VCT interface [Microsoft TV Technologies]","GetRecordCarrierFrequency method","IATSC_VCT.GetRecordCarrierFrequency","IATSC_VCT::GetRecordCarrierFrequency","IATSC_VCTGetRecordCarrierFrequency","atscpsipparser/IATSC_VCT::GetRecordCarrierFrequency","mstv.iatsc_vct_getrecordcarrierfrequency"]
old-location: mstv\iatsc_vct_getrecordcarrierfrequency.htm
tech.root: mstv
ms.assetid: ff875184-1d91-489d-9941-5d1cd3e9e872
ms.date: 12/05/2018
ms.keywords: GetRecordCarrierFrequency, GetRecordCarrierFrequency method [Microsoft TV Technologies], GetRecordCarrierFrequency method [Microsoft TV Technologies],IATSC_VCT interface, IATSC_VCT interface [Microsoft TV Technologies],GetRecordCarrierFrequency method, IATSC_VCT.GetRecordCarrierFrequency, IATSC_VCT::GetRecordCarrierFrequency, IATSC_VCTGetRecordCarrierFrequency, atscpsipparser/IATSC_VCT::GetRecordCarrierFrequency, mstv.iatsc_vct_getrecordcarrierfrequency
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
 - IATSC_VCT::GetRecordCarrierFrequency
 - atscpsipparser/IATSC_VCT::GetRecordCarrierFrequency
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
 - IATSC_VCT.GetRecordCarrierFrequency
---

# IATSC_VCT::GetRecordCarrierFrequency


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordCarrierFrequency</b> method returns the carrier frequency for a channel in this VCT.

## -parameters

### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_vct-getcountofrecords">IATSC_VCT::GetCountOfRecords</a> method to get the number of records in the VCT.

### -param pdwVal [out]

Receives the carrier frequency, in Hz.

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

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iatsc_vct">IATSC_VCT Interface</a>