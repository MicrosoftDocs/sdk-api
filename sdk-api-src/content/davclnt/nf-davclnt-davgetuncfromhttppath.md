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

# DavGetUNCFromHTTPPath function


## -description


Converts the specified HTTP path to an equivalent UNC path.


## -parameters




### -param Url

TBD


### -param UncPath [out]

A pointer to a caller-allocated buffer  that receives the UNC path as a <b>null</b>-terminated Unicode string.


### -param lpSize [in, out]

A pointer to a variable that on input specifies the maximum size, in Unicode characters, of the buffer that the <i>UncPath</i> parameter points to. If the function succeeds, on output the variable receives the number of characters that were copied into the buffer, including the terminating <b>NULL</b> character. If the function fails with ERROR_INSUFFICIENT_BUFFER, on output the variable receives the number of characters needed to store the UNC path, including the terminating <b>NULL</b> character.


#### - HttpPath [in]

A pointer to a <b>null</b>-terminated Unicode string that contains the HTTP path. This string can be in any of the following formats, where <i>server</i> is the server name and <i>path</i> is the path to a remote file or directory on the server:

<ul>
<li>http://<i>server</i>/<i>path</i></li>
<li>http://<i>server</i></li>
<li>\\http://<i>server</i>/<i>path</i></li>
<li>\\http://<i>server</i></li>
<li>https://<i>server</i>/<i>path</i></li>
<li>https://<i>server</i></li>
<li>\\https://<i>server</i>/<i>path</i></li>
<li>\\https://<i>server</i></li>
<li>\\<i>server</i>\<i>path</i></li>
<li>\\<i>server</i></li>
</ul>

## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>, such as the following value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer that the <i>UncPath</i> parameter points to was not large enough to store the UNC path.

</td>
</tr>
</table>
 



