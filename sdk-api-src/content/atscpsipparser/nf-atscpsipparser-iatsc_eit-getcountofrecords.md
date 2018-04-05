---
UID: NF:atscpsipparser.IATSC_EIT.GetCountOfRecords
title: IATSC_EIT::GetCountOfRecords method
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iatsc_eit_getcountofrecords.htm
old-project: mstv
ms.assetid: edf16862-5bc4-4022-9727-11c1a291417d
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetCountOfRecords method [Microsoft TV Technologies], GetCountOfRecords method [Microsoft TV Technologies], IATSC_EIT interface, GetCountOfRecords,IATSC_EIT.GetCountOfRecords, IATSC_EIT, IATSC_EIT interface [Microsoft TV Technologies], GetCountOfRecords method, IATSC_EIT::GetCountOfRecords, IATSC_EITGetCountOfRecords, atscpsipparser/IATSC_EIT::GetCountOfRecords, mstv.iatsc_eit_getcountofrecords
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
req.typenames: APPX_PACKAGE_WRITER_PAYLOAD_STREAM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	atscpsipparser.h
api_name:
-	IATSC_EIT.GetCountOfRecords
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IATSC_EIT::GetCountOfRecords method


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetCountOfRecords</b> method returns the number of records in the EIT.


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




<a href="https://msdn.microsoft.com/ab3fd79f-4ca6-418e-8e7c-a5fa196c09e6">IATSC_EIT Interface</a>
 

 

