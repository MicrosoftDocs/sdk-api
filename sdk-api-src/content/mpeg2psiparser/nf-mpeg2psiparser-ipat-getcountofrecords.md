---
UID: NF:mpeg2psiparser.IPAT.GetCountOfRecords
title: IPAT::GetCountOfRecords
author: windows-driver-content
description: The GetCountOfRecords method returns the number of records in the PAT. Each record corresponds to one program.
old-location: mstv\ipat_getcountofrecords.htm
old-project: mstv
ms.assetid: 6b73a02e-d6dd-402b-baca-8728cd0fa900
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetCountOfRecords, GetCountOfRecords method [Microsoft TV Technologies], GetCountOfRecords method [Microsoft TV Technologies],IPAT interface, IPAT interface [Microsoft TV Technologies],GetCountOfRecords method, IPAT.GetCountOfRecords, IPAT::GetCountOfRecords, IPATGetCountOfRecords, mpeg2psiparser/IPAT::GetCountOfRecords, mstv.ipat_getcountofrecords
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MPEG_HEADER_VERSION_BITS, *PMPEG_HEADER_VERSION_BITS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mpeg2PsiParser.h
api_name:
-	IPAT.GetCountOfRecords
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IPAT::GetCountOfRecords


## -description



The <b>GetCountOfRecords</b> method returns the number of records in the PAT. Each record corresponds to one program.




## -parameters




### -param pdwVal [out]

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




<a href="https://msdn.microsoft.com/31b0e558-0f22-4761-a964-1908c2835478">IPAT Interface</a>
 

 

