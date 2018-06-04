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

# DavGetHTTPFromUNCPath function


## -description


Converts the specified UNC path to an equivalent HTTP path.


## -parameters




### -param UncPath [in]

A pointer to a <b>null</b>-terminated Unicode string that contains the UNC path. This path must be in the following format:

\\<i>server</i>[@SSL][@<i>port</i>][\<i>path</i>]

where<ul>
<li><i>server</i> is the server name.</li>
<li>@SSL is optional and indicates a request for an SSL connection.</li>
<li><i>port</i> is an optional port number. The standard ports are 80 for http and 443 for https (SSL).</li>
<li><i>path</i> is optional and specifies a path to a remote file or directory on the server.</li>
</ul>



### -param Url

TBD


### -param lpSize [in, out]

A pointer to a variable that on input specifies the maximum size, in Unicode characters, of the buffer that the <i>HttpPath</i> parameter points to. If the function succeeds, on output the variable receives the number of characters that were copied into the buffer. If the function fails with ERROR_INSUFFICIENT_BUFFER, on output the variable receives the number of characters needed to store the HTTP path, including the "http://" or "https://" prefix and the terminating <b>NULL</b> character.


#### - HttpPath [out]

A pointer to a caller-allocated buffer  that receives the HTTP path as a <b>null</b>-terminated Unicode string.


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
The buffer that the <i>HttpPath</i> parameter points to was not large enough to store the HTTP path.

</td>
</tr>
</table>
 



