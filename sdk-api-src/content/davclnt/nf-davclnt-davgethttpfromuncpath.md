---
UID: NF:davclnt.DavGetHTTPFromUNCPath
title: DavGetHTTPFromUNCPath function (davclnt.h)
description: Converts the specified UNC path to an equivalent HTTP path.
helpviewer_keywords: ["DavGetHTTPFromUNCPath","DavGetHTTPFromUNCPath function [WebDAV]","davclnt/DavGetHTTPFromUNCPath","webdav.davgethttpfromuncpath"]
old-location: webdav\davgethttpfromuncpath.htm
tech.root: WebDAV
ms.assetid: caa83e54-a029-45aa-9681-26b2be54fea3
ms.date: 12/05/2018
ms.keywords: DavGetHTTPFromUNCPath, DavGetHTTPFromUNCPath function [WebDAV], davclnt/DavGetHTTPFromUNCPath, webdav.davgethttpfromuncpath
req.header: davclnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DavGetHTTPFromUNCPath
 - davclnt/DavGetHTTPFromUNCPath
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - netapi32.dll
 - DavHlpr.dll
 - Ext-MS-Win-Rdr-DavHlpr-L1-1-0.dll
api_name:
 - DavGetHTTPFromUNCPath
---

# DavGetHTTPFromUNCPath function


## -description

Converts the specified UNC path to an equivalent HTTP path.

## -parameters

### -param UncPath [in]

A pointer to a <b>null</b>-terminated Unicode string that contains the UNC path. This path must be in the following format:

&#92;&#92;<i>server</i>[@SSL][@<i>port</i>][&#92;<i>path</i>]

where<ul>
<li><i>server</i> is the server name.</li>
<li>@SSL is optional and indicates a request for an SSL connection.</li>
<li><i>port</i> is an optional port number. The standard ports are 80 for http and 443 for https (SSL).</li>
<li><i>path</i> is optional and specifies a path to a remote file or directory on the server.</li>
</ul>

### -param Url [out]

A pointer to a caller-allocated buffer  that receives the HTTP path as a <b>null</b>-terminated Unicode string.

### -param lpSize [in, out]

A pointer to a variable that on input specifies the maximum size, in Unicode characters, of the buffer that the <i>HttpPath</i> parameter points to. If the function succeeds, on output the variable receives the number of characters that were copied into the buffer. If the function fails with ERROR_INSUFFICIENT_BUFFER, on output the variable receives the number of characters needed to store the HTTP path, including the "http://" or "https://" prefix and the terminating <b>NULL</b> character.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>, such as the following value.

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