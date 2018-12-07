---
UID: NF:davclnt.DavGetUNCFromHTTPPath
title: DavGetUNCFromHTTPPath function
author: windows-sdk-content
description: Converts the specified HTTP path to an equivalent UNC path.
old-location: webdav\davgetuncfromhttppath.htm
tech.root: WebDAV
ms.assetid: e9613e4a-5ba1-4954-bc7a-7843249f031e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DavGetUNCFromHTTPPath, DavGetUNCFromHTTPPath function [WebDAV], davclnt/DavGetUNCFromHTTPPath, webdav.davgetuncfromhttppath
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - DavGetUNCFromHTTPPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DavGetUNCFromHTTPPath function


## -description


Converts the specified HTTP path to an equivalent UNC path.


## -parameters




### -param Url [in]

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

### -param UncPath [out]

A pointer to a caller-allocated buffer  that receives the UNC path as a <b>null</b>-terminated Unicode string.


### -param lpSize [in, out]

A pointer to a variable that on input specifies the maximum size, in Unicode characters, of the buffer that the <i>UncPath</i> parameter points to. If the function succeeds, on output the variable receives the number of characters that were copied into the buffer, including the terminating <b>NULL</b> character. If the function fails with ERROR_INSUFFICIENT_BUFFER, on output the variable receives the number of characters needed to store the UNC path, including the terminating <b>NULL</b> character.


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
 



