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

# RtlUnicodeToMultiByteSize function


## -description


Determines how many bytes are needed to represent a Unicode string as an ANSI string.


## -parameters




### -param BytesInMultiByteString [out]

Returns the number of bytes for the ANSI equivalent of the Unicode string pointed to by <i>UnicodeString</i>. This number does not include the terminating <b>NULL</b> character. 


### -param UnicodeString [in]

The Unicode source string for which the ANSI length is calculated.


### -param BytesInUnicodeString [in]

The number of bytes in the string pointed to by
        <i>UnicodeString</i>.


## -returns



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The count was successful. The various NTSTATUS values are defined in NTSTATUS.H, which is distributed with the Windows DDK.

</td>
</tr>
</table>
 




## -remarks



It is recommended that you use <a href="https://msdn.microsoft.com/b8c13444-86ab-479c-ac04-9b184d9eebf6">WideCharToMultiByte</a> instead of <b>RtlUnicodeToMultiByteSize</b>. When its <i>cbMultiByte</i> parameter is set to zero, the <b>WideCharToMultiByte</b> function returns the number of bytes required for the buffer. 



