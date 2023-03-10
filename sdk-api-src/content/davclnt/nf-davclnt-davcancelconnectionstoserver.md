---
UID: NF:davclnt.DavCancelConnectionsToServer
title: DavCancelConnectionsToServer function (davclnt.h)
description: Closes all connections to a WebDAV server or a remote file or directory on a WebDAV server.
helpviewer_keywords: ["DavCancelConnectionsToServer","DavCancelConnectionsToServer function [WebDAV]","davclnt/DavCancelConnectionsToServer","webdav.davcancelconnectionstoserver"]
old-location: webdav\davcancelconnectionstoserver.htm
tech.root: WebDAV
ms.assetid: 6eb3b011-4cd3-45ec-a07e-c8743d35a176
ms.date: 12/05/2018
ms.keywords: DavCancelConnectionsToServer, DavCancelConnectionsToServer function [WebDAV], davclnt/DavCancelConnectionsToServer, webdav.davcancelconnectionstoserver
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DavCancelConnectionsToServer
 - davclnt/DavCancelConnectionsToServer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - davclnt.dll
api_name:
 - DavCancelConnectionsToServer
---

# DavCancelConnectionsToServer function


## -description

Closes all connections to a WebDAV server or a remote file or directory on a WebDAV server.

## -parameters

### -param lpName [in]

Pointer to a null-terminated Unicode string that contains the name of the remote file or server. This string must be in one of the following formats:

<ul>
<li>http://<i>server</i>/<i>path</i></li>
<li>&#92;&#92;<i>server</i>&#92;<i>path</i></li>
<li><i>server</i></li>
</ul>
where <i>server</i> is the name of a WebDAV server, and <i>path</i> is the path to a remote file or directory on the server.

### -param fForce

A Boolean value that specifies whether the connection should be closed if there are open files. Set this parameter to <b>FALSE</b> if the connection should be closed only if there are no open files. Set this parameter to <b>TRUE</b> if the connection should be closed even if there are open files.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a <a href="/windows/desktop/Debug/system-error-codes">system error code</a> or network error code such as one of the following values.

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