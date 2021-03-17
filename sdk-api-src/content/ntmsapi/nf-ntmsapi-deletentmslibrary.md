---
UID: NF:ntmsapi.DeleteNtmsLibrary
title: DeleteNtmsLibrary function (ntmsapi.h)
description: The DeleteNtmsLibrary function deletes a library, and all the devices contained in the library, from the RSM database. All media in the library is moved to the offline library.
helpviewer_keywords: ["DeleteNtmsLibrary","DeleteNtmsLibrary function [Files]","_zaw_deletentmslibrary","base.deletentmslibrary","fs.deletentmslibrary","ntmsapi/DeleteNtmsLibrary"]
old-location: fs\deletentmslibrary.htm
tech.root: fs
ms.assetid: 2bbc1463-9fbb-49d9-84d0-7b8ea231b454
ms.date: 12/05/2018
ms.keywords: DeleteNtmsLibrary, DeleteNtmsLibrary function [Files], _zaw_deletentmslibrary, base.deletentmslibrary, fs.deletentmslibrary, ntmsapi/DeleteNtmsLibrary
req.header: ntmsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ntmsapi.lib
req.dll: Ntmsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DeleteNtmsLibrary
 - ntmsapi/DeleteNtmsLibrary
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntmsapi.dll
api_name:
 - DeleteNtmsLibrary
---

# DeleteNtmsLibrary function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>DeleteNtmsLibrary</b> function deletes a library, and all the devices contained in the library, from the RSM database. All media in the library is moved to the offline library.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpLibraryId [in]

Unique identifier of the library to be deleted.

## -returns

This function returns one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
NTMS_MODIFY_ACCESS to the library is denied. Other security errors are also possible, but they would indicate a security subsystem error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DATABASE_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The database is inaccessible or damaged.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DATABASE_FULL</b></dt>
</dl>
</td>
<td width="60%">
The database is full.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The session handle is missing or is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_LIBRARY</b></dt>
</dl>
</td>
<td width="60%">
The library identifier is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
There is a missing media identifier.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was an allocation failure during processing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
</table>

## -remarks

If the library referenced by the 
<b>DeleteNtmsLibrary</b> function contains media, the media is moved to the offline library.

You can use 
<b>DeleteNtmsLibrary</b> to remove libraries that are no longer connected to the RSM server.

## -see-also

<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Library Control Functions</a>