---
UID: NF:mpeg2psiparser.IPAT.GetRecordProgramMapPid
title: IPAT::GetRecordProgramMapPid
author: windows-sdk-content
description: The GetRecordProgramMapPid method returns the packet identifier (PID) for a given record in the PAT.
old-location: mstv\ipat_getrecordprogrammappid.htm
old-project: mstv
ms.assetid: 0b1ca2c0-52c4-447a-8191-8f9b69aecd25
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetRecordProgramMapPid, GetRecordProgramMapPid method [Microsoft TV Technologies], GetRecordProgramMapPid method [Microsoft TV Technologies],IPAT interface, IPAT interface [Microsoft TV Technologies],GetRecordProgramMapPid method, IPAT.GetRecordProgramMapPid, IPAT::GetRecordProgramMapPid, IPATGetRecordProgramMapPid, mpeg2psiparser/IPAT::GetRecordProgramMapPid, mstv.ipat_getrecordprogrammappid
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mpeg2PsiParser.h
api_name:
-	IPAT.GetRecordProgramMapPid
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IPAT::GetRecordProgramMapPid


## -description



The <b>GetRecordProgramMapPid</b> method returns the packet identifier (PID) for a given record in the PAT.




## -parameters




### -param dwIndex [in]

Specifies the record to retrieve, indexed from zero. Call the <a href="https://msdn.microsoft.com/6b73a02e-d6dd-402b-baca-8728cd0fa900">IPAT::GetCountOfRecords</a> method to get the number of records in the PAT.


### -param pwVal [out]

Receives the PID. This value identifies the PID for the packets that contain the program map table (PMT) of the associated program.


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
 

 

