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

# DavGetExtendedError function


## -description


Retrieves the extended error code information that the WebDAV server returned for the previous failed I/O operation.


## -parameters




### -param hFile [in]

A handle to an open file for which the previous I/O operation has failed. If the previous operation is a failed create operation, in which case there is no open file handle, specify INVALID_HANDLE_VALUE for this parameter.


### -param ExtError [out]

Pointer to a variable that receives the extended error code.


### -param ExtErrorString [out]

Pointer to a buffer  that receives the extended error information as a null-terminated Unicode string.


### -param cChSize [in, out]

A pointer to a variable that on input specifies the size, in Unicode characters, of the buffer that the <i>ExtErrorString</i> parameter points to. This value must be at least 1024 characters.

 If the function succeeds, on output the variable receives the number of characters that are actually copied into the buffer. If the function fails with ERROR_INSUFFICIENT_BUFFER, the variable receives 1024, but no characters are copied into the <i>ExtErrorString</i> buffer.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>, such as one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more parameter values were not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The value that the <i>cChSize</i> parameter points to was less than 1024.

</td>
</tr>
</table>
 




## -remarks



If you call  this function for a file handle whose previous I/O  operation was successful, it returns ERROR_INVALID_PARAMETER.




## -see-also




<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/800f4d40-252a-44fe-b10d-348c22d69355">OpenFile</a>



<a href="https://msdn.microsoft.com/9d6fa723-fe3e-4052-b0b3-2686eee076a7">WriteFile</a>
 

 

