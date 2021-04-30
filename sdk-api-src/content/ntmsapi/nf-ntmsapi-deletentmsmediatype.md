---
UID: NF:ntmsapi.DeleteNtmsMediaType
title: DeleteNtmsMediaType function (ntmsapi.h)
description: The DeleteNtmsMediaType function deletes the specified media type relation from the specified library, provided that the library does not contain any physical media objects of the specified media type.
helpviewer_keywords: ["DeleteNtmsMediaType","DeleteNtmsMediaType function [Files]","_zaw_deletentmsmediatype","base.deletentmsmediatype","fs.deletentmsmediatype","ntmsapi/DeleteNtmsMediaType"]
old-location: fs\deletentmsmediatype.htm
tech.root: fs
ms.assetid: c2a2bc8a-4230-44c4-b6bc-4b4e2a9fece1
ms.date: 12/05/2018
ms.keywords: DeleteNtmsMediaType, DeleteNtmsMediaType function [Files], _zaw_deletentmsmediatype, base.deletentmsmediatype, fs.deletentmsmediatype, ntmsapi/DeleteNtmsMediaType
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
 - DeleteNtmsMediaType
 - ntmsapi/DeleteNtmsMediaType
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
 - DeleteNtmsMediaType
---

# DeleteNtmsMediaType function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>DeleteNtmsMediaType</b> function deletes the specified media type relation from the specified library, provided that the library does not contain any physical media objects of the specified media type.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpMediaTypeId [in]

Unique identifier of a media type to delete from a library.

### -param lpLibId [in]

Unique identifier of the library from which to delete the media type.

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
NTMS_MODIFY_ACCESS to the library is denied. Other security errors are possible, but indicate a security subsystem error.

<b>Windows XP:  </b>NTMS_CONTROL_ACCESS to the library is denied. Other security errors are possible, but indicate a security subsystem error.

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
The library ID is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The media type or library ID is missing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
An allocation failure occurred during processing.

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

If there are no physical media objects of the specified media type in the RSM system and there are no library objects that contain the specified media type relation in the RSM system, the system media pools for that media type will be deleted. Inability to delete the system media pools does not cause the 
<b>DeleteNtmsMediaType</b> function to fail.

## -see-also

<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-addntmsmediatype">AddNtmsMediaType</a>



<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Media Services Functions</a>