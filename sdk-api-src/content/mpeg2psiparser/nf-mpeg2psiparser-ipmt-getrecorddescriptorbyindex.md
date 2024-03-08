---
UID: NF:mpeg2psiparser.IPMT.GetRecordDescriptorByIndex
title: IPMT::GetRecordDescriptorByIndex (mpeg2psiparser.h)
description: The GetRecordDescriptorByIndex method retrieves a descriptor for a specified record in the PMT.
helpviewer_keywords: ["GetRecordDescriptorByIndex","GetRecordDescriptorByIndex method [Microsoft TV Technologies]","GetRecordDescriptorByIndex method [Microsoft TV Technologies]","IPMT interface","IPMT interface [Microsoft TV Technologies]","GetRecordDescriptorByIndex method","IPMT.GetRecordDescriptorByIndex","IPMT::GetRecordDescriptorByIndex","IPMTGetRecordDescriptorByIndex","mpeg2psiparser/IPMT::GetRecordDescriptorByIndex","mstv.ipmt_getrecorddescriptorbyindex"]
old-location: mstv\ipmt_getrecorddescriptorbyindex.htm
tech.root: mstv
ms.assetid: 1e37db4b-1b86-4b34-8f93-642bb603789e
ms.date: 12/05/2018
ms.keywords: GetRecordDescriptorByIndex, GetRecordDescriptorByIndex method [Microsoft TV Technologies], GetRecordDescriptorByIndex method [Microsoft TV Technologies],IPMT interface, IPMT interface [Microsoft TV Technologies],GetRecordDescriptorByIndex method, IPMT.GetRecordDescriptorByIndex, IPMT::GetRecordDescriptorByIndex, IPMTGetRecordDescriptorByIndex, mpeg2psiparser/IPMT::GetRecordDescriptorByIndex, mstv.ipmt_getrecorddescriptorbyindex
req.header: mpeg2psiparser.h
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
 - IPMT::GetRecordDescriptorByIndex
 - mpeg2psiparser/IPMT::GetRecordDescriptorByIndex
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mpeg2PsiParser.h
api_name:
 - IPMT.GetRecordDescriptorByIndex
---

# IPMT::GetRecordDescriptorByIndex


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetRecordDescriptorByIndex</b> method retrieves a descriptor for a specified record in the PMT.

## -parameters

### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipmt-getcountofrecords">IPMT::GetCountOfRecords</a> method to get the number of records in the PMT.

### -param dwDescIndex [in]

Specifies which descriptor to retrieve, indexed from zero. Call the <a href="/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipmt-getrecordcountofdescriptors">IPMT::GetRecordCountOfDescriptors</a> method to get the number of descriptors for a particular record.

### -param ppDescriptor [out]

Address of a variable that receives an <a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-igenericdescriptor">IGenericDescriptor</a> interface pointer. Use this interface to retrieve the information in the descriptor. The caller must release the interface.

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

<a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-ipmt">IPMT Interface</a>