---
UID: NF:mpeg2psiparser.IPMT.GetCountOfRecords
title: IPMT::GetCountOfRecords (mpeg2psiparser.h)
author: windows-sdk-content
description: The GetCountOfRecords method returns the number of records in the PMT. Each record corresponds to a stream in the program.
old-location: mstv\ipmt_getcountofrecords.htm
tech.root: mstv
ms.assetid: f4e5009b-4c0d-4d0c-b480-4030cedbdb97
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetCountOfRecords, GetCountOfRecords method [Microsoft TV Technologies], GetCountOfRecords method [Microsoft TV Technologies],IPMT interface, IPMT interface [Microsoft TV Technologies],GetCountOfRecords method, IPMT.GetCountOfRecords, IPMT::GetCountOfRecords, IPMTGetCountOfRecords, mpeg2psiparser/IPMT::GetCountOfRecords, mstv.ipmt_getcountofrecords
ms.topic: method
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
 - IPMT.GetCountOfRecords
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPMT::GetCountOfRecords


## -description



The <b>GetCountOfRecords</b> method returns the number of records in the PMT. Each record corresponds to a stream in the program.




## -parameters




### -param pwVal [out]

Receives the number of records.


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd694820(v=VS.85).aspx">IPMT Interface</a>
 

 

