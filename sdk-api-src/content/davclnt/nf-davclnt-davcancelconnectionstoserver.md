---
UID: NF:davclnt.DavCancelConnectionsToServer
title: DavCancelConnectionsToServer function (davclnt.h)
author: windows-sdk-content
description: Closes all connections to a WebDAV server or a remote file or directory on a WebDAV server.
old-location: webdav\davcancelconnectionstoserver.htm
tech.root: WebDAV
ms.assetid: 6eb3b011-4cd3-45ec-a07e-c8743d35a176
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DavCancelConnectionsToServer, DavCancelConnectionsToServer function [WebDAV], davclnt/DavCancelConnectionsToServer, webdav.davcancelconnectionstoserver
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
req.lib: Davclnt.lib
req.dll: Davclnt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - davclnt.dll
api_name:
 - DavCancelConnectionsToServer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DavCancelConnectionsToServer function


## -description


Closes all connections to a WebDAV server or a remote file or directory on a WebDAV server.


## -parameters




### -param lpName [in]

Pointer to a null-terminated Unicode string that contains the name of the remote file or server. This string must be in one of the following formats:

<ul>
<li>http://<i>server</i>/<i>path</i></li>
<li>\\<i>server</i>\<i>path</i></li>
<li><i>server</i></li>
</ul>
where <i>server</i> is the name of a WebDAV server, and <i>path</i> is the path to a remote file or directory on the server.


### -param fForce

A Boolean value that specifies whether the connection should be closed if there are open files. Set this parameter to <b>FALSE</b> if the connection should be closed only if there are no open files. Set this parameter to <b>TRUE</b> if the connection should be closed even if there are open files.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> or network error code such as one of the following values.

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
The <i>lpName</i> parameter contained a value that was not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_BAD_NETNAME</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpName</i> parameter contained a value that was not a valid remote file  name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
No connections to the remote file or server were found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_OPEN_FILES</b></dt>
</dl>
</td>
<td width="60%">
There are open files on the connection, and <i>fForce</i> parameter was set to <b>FALSE</b>.

</td>
</tr>
</table>
 



