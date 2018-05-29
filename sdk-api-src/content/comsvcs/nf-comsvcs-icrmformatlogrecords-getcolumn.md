---
UID: NF:comsvcs.ICrmFormatLogRecords.GetColumn
title: ICrmFormatLogRecords::GetColumn
author: windows-sdk-content
description: Formats one unstructured log record into an array of viewable fields.
old-location: cos\icrmformatlogrecords_getcolumn.htm
old-project: cossdk
ms.assetid: 5234f582-88e2-4a9a-8650-d0d2d4b39f31
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: GetColumn, GetColumn method [COM+], GetColumn method [COM+],ICrmFormatLogRecords interface, ICrmFormatLogRecords interface [COM+],GetColumn method, ICrmFormatLogRecords.GetColumn, ICrmFormatLogRecords::GetColumn, _dtc_ICrmFormatLogRecords_GetColumn, comsvcs/ICrmFormatLogRecords::GetColumn, cos.icrmformatlogrecords_getcolumn
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	ICrmFormatLogRecords.GetColumn
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICrmFormatLogRecords::GetColumn


## -description


Formats one unstructured log record into an array of viewable fields.


## -parameters




### -param CrmLogRec [in]

The unstructured log record to be formatted, as a <a href="https://msdn.microsoft.com/0af0eba5-6e8c-4b1d-aec4-f9a1ffe7bce6">CrmLogRecordRead</a> structure.


### -param pFormattedLogRecord [out]

The formatted log record, as a <b>Variant</b> array of the fields in this log record as <b>Variant</b> strings.


## -returns



This method can return the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A <b>NULL</b> pointer was provided as an argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The log record could not be formatted.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/aa801bd0-5253-4f9f-8859-b808d4dc081b">ICrmFormatLogRecords</a>
 

 

