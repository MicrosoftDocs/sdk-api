---
UID: NF:ntmsapi.DeleteNtmsMediaPool
title: DeleteNtmsMediaPool function (ntmsapi.h)
description: The DeleteNtmsMediaPool function deletes the specified application media pool.
helpviewer_keywords: ["DeleteNtmsMediaPool","DeleteNtmsMediaPool function [Files]","_zaw_deletentmsmediapool","base.deletentmsmediapool","fs.deletentmsmediapool","ntmsapi/DeleteNtmsMediaPool"]
old-location: fs\deletentmsmediapool.htm
tech.root: fs
ms.assetid: 79885083-beb6-4c66-8271-23082994a258
ms.date: 12/05/2018
ms.keywords: DeleteNtmsMediaPool, DeleteNtmsMediaPool function [Files], _zaw_deletentmsmediapool, base.deletentmsmediapool, fs.deletentmsmediapool, ntmsapi/DeleteNtmsMediaPool
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
 - DeleteNtmsMediaPool
 - ntmsapi/DeleteNtmsMediaPool
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
 - DeleteNtmsMediaPool
---

# DeleteNtmsMediaPool function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>DeleteNtmsMediaPool</b> function deletes the specified application media pool.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpPoolId [in]

Unique identifier of the media pool.

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
NTMS_MODIFY_ACCESS to the media pool is denied. Other security errors are also possible, but they indicate a security subsystem error.

<b>Windows XP:  </b>NTMS_CONTROL_ACCESS to the media pool is denied. Other security errors are also possible, but they indicate a security subsystem error.

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
<dt><b>ERROR_INVALID_MEDIA_POOL</b></dt>
</dl>
</td>
<td width="60%">
Unable to open existing media pool, or attempting to delete free, import, or unrecognized media pools.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The media pool ID is missing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_EMPTY</b></dt>
</dl>
</td>
<td width="60%">
The media pool must be empty to be deleted.

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

Only empty media pools can be deleted with the 
<b>DeleteNtmsMediaPool</b> function.

Free, unrecognized, and import media pools are managed by RSM and cannot be deleted with 
<b>DeleteNtmsMediaPool</b>.

## -see-also

<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-createntmsmediapool">CreateNtmsMediaPool</a>



<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Media Services Functions</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-movetontmsmediapool">MoveToNtmsMediaPool</a>