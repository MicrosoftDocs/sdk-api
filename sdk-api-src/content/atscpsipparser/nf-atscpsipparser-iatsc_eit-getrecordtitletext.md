---
UID: NF:atscpsipparser.IATSC_EIT.GetRecordTitleText
title: IATSC_EIT::GetRecordTitleText
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iatsc_eit_getrecordtitletext.htm
old-project: mstv
ms.assetid: 10084fd6-2a14-4abc-8163-ec1b66987343
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetRecordTitleText, GetRecordTitleText method [Microsoft TV Technologies], GetRecordTitleText method [Microsoft TV Technologies],IATSC_EIT interface, IATSC_EIT interface [Microsoft TV Technologies],GetRecordTitleText method, IATSC_EIT.GetRecordTitleText, IATSC_EIT::GetRecordTitleText, IATSC_EITGetRecordTitleText, atscpsipparser/IATSC_EIT::GetRecordTitleText, mstv.iatsc_eit_getrecordtitletext
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
-	IATSC_EIT.GetRecordTitleText
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IATSC_EIT::GetRecordTitleText


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordTitleText</b> method returns the title text for a record in the EIT.


## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="https://msdn.microsoft.com/edf16862-5bc4-4022-9727-11c1a291417d">IATSC_EIT::GetCountOfRecords</a> method to get the number of records in the EIT.


### -param pdwLength [out]

Receives the length of the title text, in bytes.


### -param ppText [out]

Receives a pointer to the text buffer. The method allocates the buffer and fills it with the title text, which is formatted as a Multiple String Structure as defined by ATSC PSIP Standard A/65. The caller must free the buffer by calling <b>CoTaskMemFree</b>.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
This record does not contain a title.

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
 

 

