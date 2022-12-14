---
UID: NC:projectedfslib.PRJ_GET_FILE_DATA_CB
title: PRJ_GET_FILE_DATA_CB (projectedfslib.h)
description: Requests the contents of a file's primary data stream.
helpviewer_keywords: ["PRJ_GET_FILE_DATA_CB","PRJ_GET_FILE_DATA_CB callback","PRJ_GET_FILE_DATA_CB callback function","ProjFS.prj_get_file_data_cb","projectedfslib/PRJ_GET_FILE_DATA_CB"]
old-location: projfs\prj_get_file_data_cb.htm
tech.root: ProjFS
ms.assetid: 8F3EEC96-70C2-40ED-BDF3-B6E979EF1F7E
ms.date: 12/05/2018
ms.keywords: PRJ_GET_FILE_DATA_CB, PRJ_GET_FILE_DATA_CB callback, PRJ_GET_FILE_DATA_CB callback function, ProjFS.prj_get_file_data_cb, projectedfslib/PRJ_GET_FILE_DATA_CB
req.header: projectedfslib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: RS5, 19H1
f1_keywords:
 - PRJ_GET_FILE_DATA_CB
 - projectedfslib/PRJ_GET_FILE_DATA_CB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - projectedfslib.h
api_name:
 - PRJ_GET_FILE_DATA_CB
---

# PRJ_GET_FILE_DATA_CB callback function


## -description

Requests the contents of a file's primary data stream.

## -parameters

### -param callbackData [in]

Information about the operation. The following <i>callbackData</i> members are necessary to implement this callback:<dl>
<dd><b>FilePathName</b> Identifies the path to the file in the provider’s backing store for which data should be returned.  Note that this reflects the name the file had when its placeholder was first created.  If it has been renamed since then, <b>FilePathName</b> identifies the original (pre-rename) name, not the current (post-rename) name.

</dd>
<dd><b>DataStreamId</b>The unique value to associate with this file stream.  The provider must pass this value in the <i>dataStreamId</i> parameter of <a href="/windows/desktop/api/projectedfslib/nf-projectedfslib-prjwritefiledata">PrjWriteFileData</a> when providing file data as part of handling this callback.

</dd>
<dd><b>VersionInfo</b> Provides the <a href="/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info">PRJ_PLACEHOLDER_VERSION_INFO</a> information that the provider supplied when it created the placeholder for this file.  This may help the provider determine which version of the file contents to return.  If the file has been renamed and the provider tracks renames, this may also help the provider determine which file’s contents are being requested.

</dd>
</dl>


The provider can access this buffer only while the callback is running. If it wishes to pend the operation and it requires data from this buffer, it must make its own copy of it.

### -param byteOffset [in]

Offset of the requested data, in bytes, from the beginning of the file. The provider must return file data starting at or before this offset

### -param length [in]

Number of bytes of file data requested. The provider must return at least this many bytes of file data beginning with byteOffset.

## -returns

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The provider successfully returned all the requested data. 


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_IO_PENDING)</b></dt>
</dl>
</td>
<td width="60%">
The provider wishes to complete the operation at a later time.

</td>
</tr>
</table>
 

An appropriate HRESULT error code if the provider fails the operation.

## -remarks

When ProjFS receives the data it will write it to the file to convert it into a hydrated placeholder. 


To handle this callback, the provider issues one or more calls to <a href="/windows/desktop/api/projectedfslib/nf-projectedfslib-prjwritefiledata">PrjWriteFileData</a> to give ProjFS the requested contents of the file's primary data stream. Then the provider completes the callback.