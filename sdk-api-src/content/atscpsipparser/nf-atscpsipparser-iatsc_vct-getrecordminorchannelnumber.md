---
UID: NF:atscpsipparser.IATSC_VCT.GetRecordMinorChannelNumber
title: IATSC_VCT::GetRecordMinorChannelNumber (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.helpviewer_keywords: ["GetRecordMinorChannelNumber","GetRecordMinorChannelNumber method [Microsoft TV Technologies]","GetRecordMinorChannelNumber method [Microsoft TV Technologies]","IATSC_VCT interface","IATSC_VCT interface [Microsoft TV Technologies]","GetRecordMinorChannelNumber method","IATSC_VCT.GetRecordMinorChannelNumber","IATSC_VCT::GetRecordMinorChannelNumber","IATSC_VCTGetRecordMinorChannelNumber","atscpsipparser/IATSC_VCT::GetRecordMinorChannelNumber","mstv.iatsc_vct_getrecordminorchannelnumber"]
old-location: mstv\iatsc_vct_getrecordminorchannelnumber.htm
tech.root: mstv
ms.assetid: e0c6eecb-7543-4476-882c-29b1ee103359
ms.date: 12/05/2018
ms.keywords: GetRecordMinorChannelNumber, GetRecordMinorChannelNumber method [Microsoft TV Technologies], GetRecordMinorChannelNumber method [Microsoft TV Technologies],IATSC_VCT interface, IATSC_VCT interface [Microsoft TV Technologies],GetRecordMinorChannelNumber method, IATSC_VCT.GetRecordMinorChannelNumber, IATSC_VCT::GetRecordMinorChannelNumber, IATSC_VCTGetRecordMinorChannelNumber, atscpsipparser/IATSC_VCT::GetRecordMinorChannelNumber, mstv.iatsc_vct_getrecordminorchannelnumber
f1_keywords:
- atscpsipparser/IATSC_VCT.GetRecordMinorChannelNumber
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
- IATSC_VCT.GetRecordMinorChannelNumber
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IATSC_VCT::GetRecordMinorChannelNumber


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordMinorChannelNumber</b> method returns the minor channel number for a record in the VCT.


## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_vct-getcountofrecords">IATSC_VCT::GetCountOfRecords</a> method to get the number of records in the VCT.


### -param pwVal [out]

Receives the minor channel number.


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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_vct-getrecordmajorchannelnumber">GetRecordMajorChannelNumber</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iatsc_vct">IATSC_VCT Interface</a>
 

 

