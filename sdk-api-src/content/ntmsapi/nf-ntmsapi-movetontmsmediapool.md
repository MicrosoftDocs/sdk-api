---
UID: NF:ntmsapi.MoveToNtmsMediaPool
title: MoveToNtmsMediaPool function (ntmsapi.h)
description: The MoveToNtmsMediaPool function moves the specified medium from its current media pool to the specified media pool.
helpviewer_keywords: ["MoveToNtmsMediaPool","MoveToNtmsMediaPool function [Files]","_zaw_movetontmsmediapool","base.movetontmsmediapool","fs.movetontmsmediapool","ntmsapi/MoveToNtmsMediaPool"]
old-location: fs\movetontmsmediapool.htm
tech.root: fs
ms.assetid: 6bc11877-6657-4e8b-8239-bb2720cfb256
ms.date: 12/05/2018
ms.keywords: MoveToNtmsMediaPool, MoveToNtmsMediaPool function [Files], _zaw_movetontmsmediapool, base.movetontmsmediapool, fs.movetontmsmediapool, ntmsapi/MoveToNtmsMediaPool
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
 - MoveToNtmsMediaPool
 - ntmsapi/MoveToNtmsMediaPool
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
 - MoveToNtmsMediaPool
---

# MoveToNtmsMediaPool function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>MoveToNtmsMediaPool</b> function moves the specified medium from its current media pool to the specified media pool.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpMediaId [in]

Unique identifier of a piece of physical media.

### -param lpPoolId [in]

Unique identifier of the destination media pool.

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

<b>Windows XP:  </b>NTMS_MODIFY_ACCESS to the source media's media pool or the destination media pool is denied. Other security errors are also possible, but they would indicate a security subsystem error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUSY</b></dt>
</dl>
</td>
<td width="60%">
At least one side of the media is in use or currently unavailable.

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
<dt><b>ERROR_INVALID_MEDIA_POOL</b></dt>
</dl>
</td>
<td width="60%">
The destination media pool is not valid; the media pool is nonexistent; or the media in the unrecognized or import pool may only be moved to the free pool.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_MEDIA</b></dt>
</dl>
</td>
<td width="60%">
The source media or implied source media pool is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The media ID or media pool ID is missing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MEDIA_INCOMPATIBLE</b></dt>
</dl>
</td>
<td width="60%">
The media type of the source differs from the media type of the destination media pool.

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

The destination pool specified in the 
<b>MoveToNtmsMediaPool</b> function must be of the same media type and have compatible security.

RSM writes an on-media identifier to media before moving the media into the free media pool.

A medium having a partition in the Completed, Allocated, or Reserved state may not be moved to the Free media pool. A medium may be moved to an Import pool only if all the partitions of the medium are in the Import state.

<b>Windows Server 2003:  </b>If the free pool is the source pool, NTMS_USE_ACCESS to the free pool and NTMS_CONTROL_ACCESS to the destination pool is required. Otherwise, NTMS_CONTROL_ACCESS is required on both source and destination pool. If the free pool is the destination pool, NTMS_CONTROL_ACCESS to the source pool and NTMS_USER_ACCESS to the free pool is required. Otherwise, NTMS_CONTROL_ACCESS is required on both source and destination pools.

## -see-also

<a href="/previous-versions/windows/desktop/rsm/media">AllocateNtmsMedia</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-createntmsmediapool">CreateNtmsMediaPool</a>



<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Media Services Functions</a>