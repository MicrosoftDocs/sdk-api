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

# SysReAllocStringLen function


## -description


Creates a new BSTR containing a specified number of characters from an old BSTR, and frees the old BSTR.


## -parameters




### -param pbstr [in, out]

The previously allocated string.


### -param psz [in, optional]

The string from which to copy <i>len</i> characters, or NULL to keep the string uninitialized.


### -param len [in]

The number of characters to copy. A null character is placed afterward, allocating a total of <i>len</i> plus one characters.


## -returns



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The string is reallocated successfully.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists.

</td>
</tr>
</table>
 




## -remarks



Allocates a new string, copies <i>len</i> characters from the passed string into it, and then appends a null character. Frees the BSTR referenced currently by <i>pbstr</i>, and resets <i>pbstr</i> to point to the new BSTR. If <i>psz</i> is null, a string of length <i>len</i> is allocated but not initialized.

The <i>psz</i> string can contain embedded null characters and does not need to end with a null.

If this function is passed a NULL pointer, there will be an access violation and the program will crash. It is your responsibility to protect this function against NULL pointers.




## -see-also




<a href="https://msdn.microsoft.com/323cefbf-836c-4c9d-bcbe-f2663a57d2b5">String Manipulation Functions</a>
 

 

