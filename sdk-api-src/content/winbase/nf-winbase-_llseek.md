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

# _llseek function


## -description


<p class="CCE_Message">[This function is provided for compatibility with 16-bit versions of Windows. New applications should use the <b>SetFilePointer</b> function.]

Repositions the file pointer for the specified file.


## -parameters




### -param hFile

A handle to an open file. This handle is created by <a href="https://msdn.microsoft.com/89e19823-c720-4bfc-95d5-18942573dd94">_lcreat</a>.


### -param lOffset

TBD


### -param iOrigin

TBD




#### - LONG

The number of bytes that the file pointer is to be moved.


#### - nOrigin

The starting point and the direction that the pointer will be moved.


This parameter must be set to one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Moves the pointer from the beginning of the file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Moves the file from its current location.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Moves the pointer from the end of the file.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value specifies the new offset. Otherwise, the return value is HFILE_ERROR. To get extended error information, use the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



When a file is initially opened, the file pointer is set to the beginning of the file. The <b>_llseek</b> function moves the pointer without reading data, which allows random access to the content of the file.




## -see-also




<a href="https://msdn.microsoft.com/a0a0081b-9132-4dea-967b-1ee1d1fdfa13">SetFilePointer</a>
 

 

