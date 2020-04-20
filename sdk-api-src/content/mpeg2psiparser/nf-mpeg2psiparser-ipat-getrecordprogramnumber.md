---
UID: NF:mpeg2psiparser.IPAT.GetRecordProgramNumber
title: IPAT::GetRecordProgramNumber (mpeg2psiparser.h)
description: The GetRecordProgramNumber method retrieves a program number from the PAT.helpviewer_keywords: ["GetRecordProgramNumber","GetRecordProgramNumber method [Microsoft TV Technologies]","GetRecordProgramNumber method [Microsoft TV Technologies]","IPAT interface","IPAT interface [Microsoft TV Technologies]","GetRecordProgramNumber method","IPAT.GetRecordProgramNumber","IPAT::GetRecordProgramNumber","IPATGetRecordProgramNumber","mpeg2psiparser/IPAT::GetRecordProgramNumber","mstv.ipat_getrecordprogramnumber"]
old-location: mstv\ipat_getrecordprogramnumber.htm
tech.root: mstv
ms.assetid: 24a79c42-aebb-4c31-af86-508c5de3b7a3
ms.date: 12/05/2018
ms.keywords: GetRecordProgramNumber, GetRecordProgramNumber method [Microsoft TV Technologies], GetRecordProgramNumber method [Microsoft TV Technologies],IPAT interface, IPAT interface [Microsoft TV Technologies],GetRecordProgramNumber method, IPAT.GetRecordProgramNumber, IPAT::GetRecordProgramNumber, IPATGetRecordProgramNumber, mpeg2psiparser/IPAT::GetRecordProgramNumber, mstv.ipat_getrecordprogramnumber
f1_keywords:
- mpeg2psiparser/IPAT.GetRecordProgramNumber
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Mpeg2PsiParser.h
api_name:
- IPAT.GetRecordProgramNumber
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPAT::GetRecordProgramNumber


## -description



The <b>GetRecordProgramNumber</b> method retrieves a program number from the PAT.




## -parameters




### -param dwIndex [in]

Specifies the record to retrieve, indexed from zero. Call the <a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipat-getcountofrecords">IPAT::GetCountOfRecords</a> method to get the number of records in the PAT.


### -param pwVal [out]

Receives the program number.


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




<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-ipat">IPAT Interface</a>
 

 

