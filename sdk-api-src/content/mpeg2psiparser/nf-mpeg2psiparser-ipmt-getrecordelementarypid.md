---
UID: NF:mpeg2psiparser.IPMT.GetRecordElementaryPid
title: IPMT::GetRecordElementaryPid
author: windows-sdk-content
description: The GetRecordElementaryPid method returns the packet identifier (PID) for a given elementary stream in the program.
old-location: mstv\ipmt_getrecordelementarypid.htm
old-project: mstv
ms.assetid: ed4790ee-97ce-482e-834e-4081a310f4bb
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetRecordElementaryPid, GetRecordElementaryPid method [Microsoft TV Technologies], GetRecordElementaryPid method [Microsoft TV Technologies],IPMT interface, IPMT interface [Microsoft TV Technologies],GetRecordElementaryPid method, IPMT.GetRecordElementaryPid, IPMT::GetRecordElementaryPid, IPMTGetRecordElementaryPid, mpeg2psiparser/IPMT::GetRecordElementaryPid, mstv.ipmt_getrecordelementarypid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mpeg2psiparser.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MPEG_HEADER_VERSION_BITS, *PMPEG_HEADER_VERSION_BITS
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
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IPMT::GetRecordElementaryPid


## -description



The <b>GetRecordElementaryPid</b> method returns the packet identifier (PID) for a given elementary stream in the program.




## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="https://msdn.microsoft.com/f4e5009b-4c0d-4d0c-b480-4030cedbdb97">IPMT::GetCountOfRecords</a> method to get the number of records in the PMT.


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




<a href="https://msdn.microsoft.com/0dbd4cc3-5ef3-4c71-ba3f-149d5050ba24">IPMT Interface</a>
 

 

