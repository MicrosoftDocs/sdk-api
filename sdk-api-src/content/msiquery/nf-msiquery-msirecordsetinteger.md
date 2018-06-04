---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# MsiRecordSetInteger function


## -description


The 
<b>MsiRecordSetInteger</b> function sets a record field to an integer field.


## -parameters




### -param hRecord [in]

Handle to the record.


### -param iField [in]

Specifies the field of the record to set.


### -param iValue [in]

Specifies the value to which to set the field.


## -returns



This function returns UINT.




## -remarks



In the 
<b>MsiRecordSetInteger</b> function, attempting to store a value in a nonexistent field causes an error. Note that the following code returns <b>ERROR_INVALID_PARAMETER</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>MSIHANDLE hRecord;
UINT lReturn;  

//create an msirecord with no fields
hRecord = MsiCreateRecord(0); 

//attempting to set the first field's value gives you ERROR_INVALID_PARAMETER 
lReturn = MsiRecordSetInteger(hRecord, 1, 0);  
</pre>
</td>
</tr>
</table></span></div>
To set a record integer field to <b>NULL_INTEGER</b>, set <i>iValue</i> to <b>MSI_NULL_INTEGER</b>.




## -see-also




<a href="database_functions.htm">Record Processing Functions</a>
 

 

