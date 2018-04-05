---
UID: NF:mpeg2psiparser.IPAT.GetRecordProgramNumber
title: IPAT::GetRecordProgramNumber method
author: windows-driver-content
description: The GetRecordProgramNumber method retrieves a program number from the PAT.
old-location: mstv\ipat_getrecordprogramnumber.htm
old-project: mstv
ms.assetid: 24a79c42-aebb-4c31-af86-508c5de3b7a3
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetRecordProgramNumber method [Microsoft TV Technologies], GetRecordProgramNumber method [Microsoft TV Technologies], IPAT interface, GetRecordProgramNumber,IPAT.GetRecordProgramNumber, IPAT, IPAT interface [Microsoft TV Technologies], GetRecordProgramNumber method, IPAT::GetRecordProgramNumber, IPATGetRecordProgramNumber, mpeg2psiparser/IPAT::GetRecordProgramNumber, mstv.ipat_getrecordprogramnumber
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
-	IPAT.GetRecordProgramNumber
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IPAT::GetRecordProgramNumber method


## -description



The <b>GetRecordProgramNumber</b> method retrieves a program number from the PAT.




## -parameters




### -param dwIndex [in]

Specifies the record to retrieve, indexed from zero. Call the <a href="https://msdn.microsoft.com/6b73a02e-d6dd-402b-baca-8728cd0fa900">IPAT::GetCountOfRecords</a> method to get the number of records in the PAT.


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




<a href="https://msdn.microsoft.com/31b0e558-0f22-4761-a964-1908c2835478">IPAT Interface</a>
 

 

