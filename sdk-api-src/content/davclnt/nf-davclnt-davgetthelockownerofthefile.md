---
UID: NF:davclnt.DavGetTheLockOwnerOfTheFile
title: DavGetTheLockOwnerOfTheFile function (davclnt.h)
description: Returns the file lock owner for a file that is locked on a WebDAV server.
helpviewer_keywords: ["DavGetTheLockOwnerOfTheFile","DavGetTheLockOwnerOfTheFile function [WebDAV]","davclnt/DavGetTheLockOwnerOfTheFile","webdav.davgetthelockownerofthefile"]
old-location: webdav\davgetthelockownerofthefile.htm
tech.root: WebDAV
ms.assetid: 94a4607c-2770-4656-8710-987d6b951e0e
ms.date: 12/05/2018
ms.keywords: DavGetTheLockOwnerOfTheFile, DavGetTheLockOwnerOfTheFile function [WebDAV], davclnt/DavGetTheLockOwnerOfTheFile, webdav.davgetthelockownerofthefile
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
 - DavGetTheLockOwnerOfTheFile
 - davclnt/DavGetTheLockOwnerOfTheFile
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
 - DavGetTheLockOwnerOfTheFile
---

# DavGetTheLockOwnerOfTheFile function


## -description

Returns the file lock owner for a file that is locked on a WebDAV server.

## -parameters

### -param FileName [in]

A pointer to a <b>null</b>-terminated Unicode string that contains the name of a locked file on the WebDAV server. This string must be in one of the following formats:

<ul>
<li>&#92;&#92;<i>server</i>&#92;<i>path</i>&#92;<i>filename</i></li>
<li><i>drive</i>:&#92;<i>filename</i></li>
</ul>
where <i>server</i> is the name of a server, <i>path</i> is the path to a remote file on the server, <i>filename</i> is a valid file name, and <i>drive</i> is the drive letter that a remote share is mapped to on the local computer. (A <i>share</i> is a directory on a server that is made available to users over the network.)

### -param LockOwnerName [out, optional]

A pointer to a caller-allocated buffer  that receives the name of the owner of the file lock. This parameter is optional and can be <b>NULL</b>. If it is <b>NULL</b>, the <i>LockOwnerNameLengthInBytes</i> parameter must point to zero on input.

### -param LockOwnerNameLengthInBytes [in, out]

A pointer to a variable that on input specifies the maximum size, in Unicode characters, of the buffer that the <i>LockOwnerName</i> parameter points to. If the function succeeds, on output the variable receives the number of characters that were copied into the buffer. If the function fails with ERROR_INSUFFICIENT_BUFFER, on output the variable receives the number of characters needed to store the lock owner name, including the terminating <b>NULL</b> character.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>, such as one of the following values.

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
The buffer that the <i>LockOwnerName</i> parameter points to was not large enough to store the lock owner name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more parameter values were not valid. For example, this error code is returned if the <i>FileName</i> parameter is a <b>null</b> pointer.

</td>
</tr>
</table>

## -remarks

If a call to a function such as <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> for a file on a WebDAV server fails with ERROR_LOCK_VIOLATION, you can use the <b>DavGetTheLockOwnerOfTheFile</b> function to determine the owner of the file lock.

To obtain the required buffer length for the <i>LockOwnerName</i> buffer, call <b>DavGetTheLockOwnerOfTheFile</b> with <i>LockOwnerName</i> set to <b>NULL</b> and <i>LockOwnerNameLengthInBytes</i> set to zero. The return value is ERROR_INSUFFICIENT_BUFFER, and on output the <i>LockOwnerNameLengthInBytes</i> parameter receives the required buffer length.