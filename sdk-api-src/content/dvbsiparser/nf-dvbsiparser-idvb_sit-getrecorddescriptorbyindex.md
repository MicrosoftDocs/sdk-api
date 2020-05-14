---
UID: NF:dvbsiparser.IDVB_SIT.GetRecordDescriptorByIndex
title: IDVB_SIT::GetRecordDescriptorByIndex (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetRecordDescriptorByIndex","GetRecordDescriptorByIndex method [Microsoft TV Technologies]","GetRecordDescriptorByIndex method [Microsoft TV Technologies]","IDVB_SIT interface","IDVB_SIT interface [Microsoft TV Technologies]","GetRecordDescriptorByIndex method","IDVB_SIT.GetRecordDescriptorByIndex","IDVB_SIT::GetRecordDescriptorByIndex","IDVB_SITGetRecordDescriptorByIndex","dvbsiparser/IDVB_SIT::GetRecordDescriptorByIndex","mstv.idvb_sit_getrecorddescriptorbyindex"]
old-location: mstv\idvb_sit_getrecorddescriptorbyindex.htm
tech.root: mstv
ms.assetid: c6556778-74ea-487c-a6c9-82ed20e79031
ms.date: 12/05/2018
ms.keywords: GetRecordDescriptorByIndex, GetRecordDescriptorByIndex method [Microsoft TV Technologies], GetRecordDescriptorByIndex method [Microsoft TV Technologies],IDVB_SIT interface, IDVB_SIT interface [Microsoft TV Technologies],GetRecordDescriptorByIndex method, IDVB_SIT.GetRecordDescriptorByIndex, IDVB_SIT::GetRecordDescriptorByIndex, IDVB_SITGetRecordDescriptorByIndex, dvbsiparser/IDVB_SIT::GetRecordDescriptorByIndex, mstv.idvb_sit_getrecorddescriptorbyindex
f1_keywords:
- dvbsiparser/IDVB_SIT.GetRecordDescriptorByIndex
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dvbsiparser.h
api_name:
- IDVB_SIT.GetRecordDescriptorByIndex
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDVB_SIT::GetRecordDescriptorByIndex


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordDescriptorByIndex</b> method retrieves a descriptor for a specified record in the SIT.


## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_sit-getcountofrecords">IDVB_SIT::GetCountOfRecords</a> to get the number of records in the SIT.


### -param dwIndex [in]

Specifies which descriptor to retrieve, indexed from zero. Call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_sit-getrecordcountofdescriptors">IDVB_SIT::GetRecordCountOfDescriptors</a> method to get the number of descriptors for a particular record.


### -param ppDescriptor [out]

Address of a variable that receives an <a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-igenericdescriptor">IGenericDescriptor</a> interface pointer. Use this interface to retrieve the information in the descriptor. The caller must release the interface.


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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_sit">IDVB_SIT Interface</a>
 

 

