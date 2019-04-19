---
UID: NF:comsvcs.ICrmFormatLogRecords.GetColumnCount
title: ICrmFormatLogRecords::GetColumnCount (comsvcs.h)
author: windows-sdk-content
description: Retrieves the number of fields (columns) in a log record of the type used by this CRM Compensator.
old-location: cos\icrmformatlogrecords_getcolumncount.htm
tech.root: cossdk
ms.assetid: d1b1bc24-6e9d-4f48-ac11-f3892a3be2b1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetColumnCount, GetColumnCount method [COM+], GetColumnCount method [COM+],ICrmFormatLogRecords interface, ICrmFormatLogRecords interface [COM+],GetColumnCount method, ICrmFormatLogRecords.GetColumnCount, ICrmFormatLogRecords::GetColumnCount, _dtc_ICrmFormatLogRecords_GetColumnCount, comsvcs/ICrmFormatLogRecords::GetColumnCount, cos.icrmformatlogrecords_getcolumncount
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ICrmFormatLogRecords.GetColumnCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICrmFormatLogRecords::GetColumnCount


## -description


Retrieves the number of fields (columns) in a log record of the type used by this CRM Compensator.


## -parameters




### -param plColumnCount [out]

The number of fields (columns) in the log record.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/aa801bd0-5253-4f9f-8859-b808d4dc081b">ICrmFormatLogRecords</a>
 

 

