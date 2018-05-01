---
UID: NF:atscpsipparser.IATSC_VCT.GetRecordProgramNumber
title: IATSC_VCT::GetRecordProgramNumber method
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iatsc_vct_getrecordprogramnumber.htm
old-project: mstv
ms.assetid: 11bf3b27-98da-4f4f-a6a9-6c69b20aedda
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetRecordProgramNumber method [Microsoft TV Technologies], GetRecordProgramNumber method [Microsoft TV Technologies], IATSC_VCT interface, GetRecordProgramNumber,IATSC_VCT.GetRecordProgramNumber, IATSC_VCT, IATSC_VCT interface [Microsoft TV Technologies], GetRecordProgramNumber method, IATSC_VCT::GetRecordProgramNumber, IATSC_VCTGetRecordProgramNumber, atscpsipparser/IATSC_VCT::GetRecordProgramNumber, mstv.iatsc_vct_getrecordprogramnumber
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: atscpsipparser.h
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
req.typenames: AsyncStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	atscpsipparser.h
api_name:
-	IATSC_VCT.GetRecordProgramNumber
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IATSC_VCT::GetRecordProgramNumber method


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordProgramNumber</b> method returns the program number for a record in the VCT.


## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="https://msdn.microsoft.com/a6a9f998-f8a8-4459-91f8-aa4a5206d190">IATSC_VCT::GetCountOfRecords</a> method to get the number of records in the VCT.


### -param pwVal [out]

Receives the program_number field.


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




<a href="https://msdn.microsoft.com/3ff9cd6e-0d25-462c-93a7-2399395f68b0">IATSC_VCT Interface</a>
 

 

