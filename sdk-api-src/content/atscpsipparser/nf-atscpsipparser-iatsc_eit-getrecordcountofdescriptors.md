---
UID: NF:atscpsipparser.IATSC_EIT.GetRecordCountOfDescriptors
title: IATSC_EIT::GetRecordCountOfDescriptors
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iatsc_eit_getrecordcountofdescriptors.htm
old-project: mstv
ms.assetid: fd568711-c82c-4ffe-9333-2b729502fe79
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetRecordCountOfDescriptors, GetRecordCountOfDescriptors method [Microsoft TV Technologies], GetRecordCountOfDescriptors method [Microsoft TV Technologies],IATSC_EIT interface, IATSC_EIT interface [Microsoft TV Technologies],GetRecordCountOfDescriptors method, IATSC_EIT.GetRecordCountOfDescriptors, IATSC_EIT::GetRecordCountOfDescriptors, IATSC_EITGetRecordCountOfDescriptors, atscpsipparser/IATSC_EIT::GetRecordCountOfDescriptors, mstv.iatsc_eit_getrecordcountofdescriptors
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AsyncStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	atscpsipparser.h
api_name:
-	IATSC_EIT.GetRecordCountOfDescriptors
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IATSC_EIT::GetRecordCountOfDescriptors


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordCountOfDescriptors</b> method returns the number of descriptors for a record in the EIT.


## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="https://msdn.microsoft.com/edf16862-5bc4-4022-9727-11c1a291417d">IATSC_EIT::GetCountOfRecords</a> method to get the number of records in the EIT.


### -param pdwVal [out]

Receives the number of descriptors.


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




<a href="https://msdn.microsoft.com/ab3fd79f-4ca6-418e-8e7c-a5fa196c09e6">IATSC_EIT Interface</a>
 

 

