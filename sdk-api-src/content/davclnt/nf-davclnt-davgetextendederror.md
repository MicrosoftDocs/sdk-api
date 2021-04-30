---
UID: NF:davclnt.DavGetExtendedError
title: DavGetExtendedError function (davclnt.h)
description: Retrieves the extended error code information that the WebDAV server returned for the previous failed I/O operation.
helpviewer_keywords: ["DavGetExtendedError","DavGetExtendedError function [WebDAV]","davclnt/DavGetExtendedError","webdav.davgetextendederror"]
old-location: webdav\davgetextendederror.htm
tech.root: WebDAV
ms.assetid: 939b6163-b7ae-4ab7-9bcc-a02cbf34ca63
ms.date: 12/05/2018
ms.keywords: DavGetExtendedError, DavGetExtendedError function [WebDAV], davclnt/DavGetExtendedError, webdav.davgetextendederror
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
 - DavGetExtendedError
 - davclnt/DavGetExtendedError
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
 - DavGetExtendedError
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

If the function fails, the return value is a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>, such as one of the following values.

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

<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/winbase/nf-winbase-openfile">OpenFile</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a>