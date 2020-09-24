---
UID: NF:ntmsapi.ChangeNtmsMediaType
title: ChangeNtmsMediaType function (ntmsapi.h)
description: The ChangeNtmsMediaType function moves the specified PMID to the specified target media pool and sets the PMID's media type identifier to the media type of the target media pool.
helpviewer_keywords: ["ChangeNtmsMediaType","ChangeNtmsMediaType function [Files]","_zaw_changentmsmediatype","base.changentmsmediatype","fs.changentmsmediatype","ntmsapi/ChangeNtmsMediaType"]
old-location: fs\changentmsmediatype.htm
tech.root: fs
ms.assetid: 89b3eb9b-0614-47a9-825e-1335c7fc5d0d
ms.date: 12/05/2018
ms.keywords: ChangeNtmsMediaType, ChangeNtmsMediaType function [Files], _zaw_changentmsmediatype, base.changentmsmediatype, fs.changentmsmediatype, ntmsapi/ChangeNtmsMediaType
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
 - ChangeNtmsMediaType
 - ntmsapi/ChangeNtmsMediaType
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
 - ChangeNtmsMediaType
---

# ChangeNtmsMediaType function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>ChangeNtmsMediaType</b> function moves the specified PMID to the specified target media pool and sets the PMID's media type identifier to the media type of the target media pool.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpMediaId [in]

Unique identifier of the physical media to be moved.

### -param lpPoolId [in]

Unique identifier of the media pool from which the media is to be allocated.

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
NTMS_MODIFY_ACCESS to the computer or the media's media pool is denied. Other security errors are possible, but they would indicate a security subsystem error.

<b>Windows XP:  </b> NTMS_MODIFY_ACCESS to the media's media pool is denied.

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
The media pool ID is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The media pool or media ID is missing.

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
<b>ChangeNtmsMediaType</b> function uses the same policy for moving media as the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-movetontmsmediapool">MoveToNtmsMediaPool</a> function (unrecognized media can only be moved to the free pool).

## -see-also

<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-addntmsmediatype">AddNtmsMediaType</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-deletentmsmediatype">DeleteNtmsMediaType</a>



<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Media Services Functions</a>