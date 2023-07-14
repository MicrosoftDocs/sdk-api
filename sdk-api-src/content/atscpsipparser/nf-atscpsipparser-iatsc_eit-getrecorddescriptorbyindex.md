---
UID: NF:atscpsipparser.IATSC_EIT.GetRecordDescriptorByIndex
title: IATSC_EIT::GetRecordDescriptorByIndex (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetRecordDescriptorByIndex","GetRecordDescriptorByIndex method [Microsoft TV Technologies]","GetRecordDescriptorByIndex method [Microsoft TV Technologies]","IATSC_EIT interface","IATSC_EIT interface [Microsoft TV Technologies]","GetRecordDescriptorByIndex method","IATSC_EIT.GetRecordDescriptorByIndex","IATSC_EIT::GetRecordDescriptorByIndex","IATSC_EITGetRecordDescriptorByIndex","atscpsipparser/IATSC_EIT::GetRecordDescriptorByIndex","mstv.iatsc_eit_getrecorddescriptorbyindex"]
old-location: mstv\iatsc_eit_getrecorddescriptorbyindex.htm
tech.root: mstv
ms.assetid: 06144d3d-b789-4ba3-b313-958de366764f
ms.date: 12/05/2018
ms.keywords: GetRecordDescriptorByIndex, GetRecordDescriptorByIndex method [Microsoft TV Technologies], GetRecordDescriptorByIndex method [Microsoft TV Technologies],IATSC_EIT interface, IATSC_EIT interface [Microsoft TV Technologies],GetRecordDescriptorByIndex method, IATSC_EIT.GetRecordDescriptorByIndex, IATSC_EIT::GetRecordDescriptorByIndex, IATSC_EITGetRecordDescriptorByIndex, atscpsipparser/IATSC_EIT::GetRecordDescriptorByIndex, mstv.iatsc_eit_getrecorddescriptorbyindex
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
 - IATSC_EIT::GetRecordDescriptorByIndex
 - atscpsipparser/IATSC_EIT::GetRecordDescriptorByIndex
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
 - IATSC_EIT.GetRecordDescriptorByIndex
---

# IATSC_EIT::GetRecordDescriptorByIndex


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordDescriptorByIndex</b> method returns a descriptor for a specified record in the EIT.

## -parameters

### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_eit-getcountofrecords">IATSC_EIT::GetCountOfRecords</a> method to get the number of records in the EIT.

### -param dwIndex [in]

Specifies which descriptor to retrieve, indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_eit-getrecordcountofdescriptors">IATSC_EIT::GetRecordCountOfDescriptors</a> method to get the number of descriptors for a particular record.

### -param ppDescriptor [out]

Receives a pointer to the <a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-igenericdescriptor">IGenericDescriptor</a> interface. Use this interface to retrieve the information in the descriptor. The caller must release the interface.

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