---
UID: NF:ntmsapi.SwapNtmsMedia
title: SwapNtmsMedia function (ntmsapi.h)
description: The SwapNtmsMedia function swaps the sides associated with the two specified LMIDs. The specified LMIDs must be in the same media pool.
helpviewer_keywords: ["SwapNtmsMedia","SwapNtmsMedia function [Files]","_zaw_swapntmsmedia","base.swapntmsmedia","fs.swapntmsmedia","ntmsapi/SwapNtmsMedia"]
old-location: fs\swapntmsmedia.htm
tech.root: fs
ms.assetid: 1e931ae0-b15c-48c8-b6a0-6fa1689263a2
ms.date: 12/05/2018
ms.keywords: SwapNtmsMedia, SwapNtmsMedia function [Files], _zaw_swapntmsmedia, base.swapntmsmedia, fs.swapntmsmedia, ntmsapi/SwapNtmsMedia
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
 - SwapNtmsMedia
 - ntmsapi/SwapNtmsMedia
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
 - SwapNtmsMedia
---

# SwapNtmsMedia function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>SwapNtmsMedia</b> function swaps the sides associated with the two specified LMIDs. The specified LMIDs must be in the same media pool.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpMediaId1 [in]

Unique identifier of a piece of logical media (LMID).

### -param lpMediaId2 [in]

Unique identifier of a piece of logical media (LMID).

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
NTMS_MODIFY_ACCESS to either media's media pool is denied. Other security errors are also possible, but they would indicate a security subsystem error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
No media label library recognizes the media label.

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
At least one of the media IDs is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_MEDIA_POOL</b></dt>
</dl>
</td>
<td width="60%">
One or more media pools for the logical media are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
At least one media identifier is missing.

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
<b>SwapNtmsMedia</b> function is used to update physical media without affecting the application.

The media for both LMIDs must not be in use for this function to succeed.

## -see-also

<a href="/previous-versions/windows/desktop/rsm/media">AllocateNtmsMedia</a>



<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Media Services Functions</a>