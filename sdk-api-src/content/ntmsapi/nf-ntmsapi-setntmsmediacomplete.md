---
UID: NF:ntmsapi.SetNtmsMediaComplete
title: SetNtmsMediaComplete function (ntmsapi.h)
description: The SetNtmsMediaComplete function marks a piece of logical media as complete.
helpviewer_keywords: ["SetNtmsMediaComplete","SetNtmsMediaComplete function [Files]","_zaw_setntmsmediacomplete","base.setntmsmediacomplete","fs.setntmsmediacomplete","ntmsapi/SetNtmsMediaComplete"]
old-location: fs\setntmsmediacomplete.htm
tech.root: fs
ms.assetid: 1513b487-93b6-4615-aa7b-e135f81b6ad0
ms.date: 12/05/2018
ms.keywords: SetNtmsMediaComplete, SetNtmsMediaComplete function [Files], _zaw_setntmsmediacomplete, base.setntmsmediacomplete, fs.setntmsmediacomplete, ntmsapi/SetNtmsMediaComplete
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
 - SetNtmsMediaComplete
 - ntmsapi/SetNtmsMediaComplete
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
 - SetNtmsMediaComplete
---

# SetNtmsMediaComplete function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>SetNtmsMediaComplete</b> function marks a piece of logical media as complete.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpMediaId [in]

Unique identifier of a piece of logical media.

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
 NTMS_CONTROL_ACCESS to the media's media pool is denied. Other security errors are also possible, but they would indicate a security subsystem error. 

<b>Windows XP:  </b>NTMS_MODIFY_ACCESS to the media's media pool is denied. Other security errors are also possible, but they would indicate a security subsystem error.

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
<dt><b>ERROR_INVALID_MEDIA</b></dt>
</dl>
</td>
<td width="60%">
The media identifier is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_MEDIA_POOL</b></dt>
</dl>
</td>
<td width="60%">
The media pool for the media is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The media identifier is missing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The media is not in the allocated state or is currently mounted.

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

The 
<b>SetNtmsMediaComplete</b> function marks the specified medium as Complete. An application marks the medium as Complete when the application is no longer going to write to the medium. Complete media cannot be mounted with the NTMS_MOUNT_WRITE flag.

The 
<b>SetNtmsMediaComplete</b> function is typically used when an application reaches the end of media. Media that is mounted or in use cannot be marked as complete.

## -see-also

<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Media Services Functions</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-mountntmsmedia">MountNtmsMedia</a>