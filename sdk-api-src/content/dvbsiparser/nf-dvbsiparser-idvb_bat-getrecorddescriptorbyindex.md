---
UID: NF:dvbsiparser.IDVB_BAT.GetRecordDescriptorByIndex
title: IDVB_BAT::GetRecordDescriptorByIndex (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetRecordDescriptorByIndex","GetRecordDescriptorByIndex method [Microsoft TV Technologies]","GetRecordDescriptorByIndex method [Microsoft TV Technologies]","IDVB_BAT interface","IDVB_BAT interface [Microsoft TV Technologies]","GetRecordDescriptorByIndex method","IDVB_BAT.GetRecordDescriptorByIndex","IDVB_BAT::GetRecordDescriptorByIndex","IDVB_BATGetRecordDescriptorByIndex","dvbsiparser/IDVB_BAT::GetRecordDescriptorByIndex","mstv.idvb_bat_getrecorddescriptorbyindex"]
old-location: mstv\idvb_bat_getrecorddescriptorbyindex.htm
tech.root: mstv
ms.assetid: ea1ace90-4378-4dec-9326-70e6f9814dde
ms.date: 12/05/2018
ms.keywords: GetRecordDescriptorByIndex, GetRecordDescriptorByIndex method [Microsoft TV Technologies], GetRecordDescriptorByIndex method [Microsoft TV Technologies],IDVB_BAT interface, IDVB_BAT interface [Microsoft TV Technologies],GetRecordDescriptorByIndex method, IDVB_BAT.GetRecordDescriptorByIndex, IDVB_BAT::GetRecordDescriptorByIndex, IDVB_BATGetRecordDescriptorByIndex, dvbsiparser/IDVB_BAT::GetRecordDescriptorByIndex, mstv.idvb_bat_getrecorddescriptorbyindex
req.header: dvbsiparser.h
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
 - IDVB_BAT::GetRecordDescriptorByIndex
 - dvbsiparser/IDVB_BAT::GetRecordDescriptorByIndex
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IDVB_BAT.GetRecordDescriptorByIndex
---

# IDVB_BAT::GetRecordDescriptorByIndex


## -description

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordDescriptorByIndex</b> method retrieves a descriptor for a specified record in the BAT.

## -parameters

### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_bat-getcountofrecords">IDVB_BAT::GetCountOfRecords</a> method to get the number of records in the BAT.

### -param dwIndex [in]

Specifies which descriptor to retrieve, indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_bat-getrecordcountofdescriptors">IDVB_BAT::GetRecordCountOfDescriptors</a> method to get the number of descriptors for a particular record.

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

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_bat">IDVB_BAT Interface</a>