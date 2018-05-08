---
UID: NF:mpeg2psiparser.IPMT.GetRecordStreamType
title: IPMT::GetRecordStreamType
author: windows-driver-content
description: The GetRecordStreamType method returns the stream type for a given elementary stream in the program.
old-location: mstv\ipmt_getrecordstreamtype.htm
old-project: mstv
ms.assetid: c3e17c0c-88ea-4143-aa9b-da2c5bf2069f
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetRecordStreamType, GetRecordStreamType method [Microsoft TV Technologies], GetRecordStreamType method [Microsoft TV Technologies],IPMT interface, IPMT interface [Microsoft TV Technologies],GetRecordStreamType method, IPMT.GetRecordStreamType, IPMT::GetRecordStreamType, IPMTGetRecordStreamType, mpeg2psiparser/IPMT::GetRecordStreamType, mstv.ipmt_getrecordstreamtype
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
-	IPMT.GetRecordStreamType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IPMT::GetRecordStreamType


## -description



The <b>GetRecordStreamType</b> method returns the stream type for a given elementary stream in the program.




## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="https://msdn.microsoft.com/f4e5009b-4c0d-4d0c-b480-4030cedbdb97">IPMT::GetCountOfRecords</a> method to get the number of records in the PMT.


### -param pbVal [out]

Receives the stream_type field.


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
 

 

