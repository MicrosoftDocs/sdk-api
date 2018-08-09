---
UID: NF:mpeg2psiparser.IPMT.GetCountOfRecords
title: IPMT::GetCountOfRecords
author: windows-sdk-content
description: The GetCountOfRecords method returns the number of records in the PMT. Each record corresponds to a stream in the program.
old-location: mstv\ipmt_getcountofrecords.htm
old-project: mstv
ms.assetid: f4e5009b-4c0d-4d0c-b480-4030cedbdb97
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetCountOfRecords, GetCountOfRecords method [Microsoft TV Technologies], GetCountOfRecords method [Microsoft TV Technologies],IPMT interface, IPMT interface [Microsoft TV Technologies],GetCountOfRecords method, IPMT.GetCountOfRecords, IPMT::GetCountOfRecords, IPMTGetCountOfRecords, mpeg2psiparser/IPMT::GetCountOfRecords, mstv.ipmt_getcountofrecords
ms.prod: windows
ms.technology: windows-sdk
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
 - IPMT.GetCountOfRecords
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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




<a href="https://msdn.microsoft.com/0dbd4cc3-5ef3-4c71-ba3f-149d5050ba24">IPMT Interface</a>
 

 

