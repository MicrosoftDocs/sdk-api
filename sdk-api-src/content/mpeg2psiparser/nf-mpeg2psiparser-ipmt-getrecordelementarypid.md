---
UID: NF:mpeg2psiparser.IPMT.GetRecordElementaryPid
title: IPMT::GetRecordElementaryPid (mpeg2psiparser.h)
author: windows-sdk-content
description: The GetRecordElementaryPid method returns the packet identifier (PID) for a given elementary stream in the program.
old-location: mstv\ipmt_getrecordelementarypid.htm
tech.root: mstv
ms.assetid: ed4790ee-97ce-482e-834e-4081a310f4bb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetRecordElementaryPid, GetRecordElementaryPid method [Microsoft TV Technologies], GetRecordElementaryPid method [Microsoft TV Technologies],IPMT interface, IPMT interface [Microsoft TV Technologies],GetRecordElementaryPid method, IPMT.GetRecordElementaryPid, IPMT::GetRecordElementaryPid, IPMTGetRecordElementaryPid, mpeg2psiparser/IPMT::GetRecordElementaryPid, mstv.ipmt_getrecordelementarypid
ms.topic: method
f1_keywords: ["mpeg2psiparser/IPMT.GetRecordElementaryPid"]
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
 - IPMT.GetRecordElementaryPid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPMT::GetRecordElementaryPid


## -description



The <b>GetRecordElementaryPid</b> method returns the packet identifier (PID) for a given elementary stream in the program.




## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipmt-getcountofrecords">IPMT::GetCountOfRecords</a> method to get the number of records in the PMT.


### -param pPidVal [out]

Receives the elementary_PID field.


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




<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-ipmt">IPMT Interface</a>
 

 

