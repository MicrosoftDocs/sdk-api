---
UID: NF:ntmsapi.DeallocateNtmsMedia
title: DeallocateNtmsMedia function (ntmsapi.h)
description: The DeallocateNtmsMedia function deallocates the side associated with the specified logical media.
helpviewer_keywords: ["DeallocateNtmsMedia","DeallocateNtmsMedia function [Files]","_zaw_deallocatentmsmedia","base.deallocatentmsmedia","fs.deallocatentmsmedia","ntmsapi/DeallocateNtmsMedia"]
old-location: fs\deallocatentmsmedia.htm
tech.root: fs
ms.assetid: e053c725-2da6-4eeb-b471-644847dd8db5
ms.date: 12/05/2018
ms.keywords: DeallocateNtmsMedia, DeallocateNtmsMedia function [Files], _zaw_deallocatentmsmedia, base.deallocatentmsmedia, fs.deallocatentmsmedia, ntmsapi/DeallocateNtmsMedia
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
 - DeallocateNtmsMedia
 - ntmsapi/DeallocateNtmsMedia
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
 - DeallocateNtmsMedia
---

# DeallocateNtmsMedia function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>DeallocateNtmsMedia</b> function deallocates the side associated with the specified logical media.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpMediaId [in]

Unique identifier of the logical media (LMID).

### -param dwOptions

Reserved; must be zero.

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
The session handle missing or is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_MEDIA</b></dt>
</dl>
</td>
<td width="60%">
The LMID is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The media or media pool ID is missing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARTITION</b></dt>
</dl>
</td>
<td width="60%">
The LMID side is not valid.

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

When a logical medium is deallocated with the 
<b>DeallocateNtmsMedia</b> function, RSM puts the side associated with the logical media in the Available or Decommissioned media state. The logical media is deleted from the system when the logical media is deallocated.

Sides are decommissioned upon deallocation if the side has been allocated the maximum number of times specified in the media pool. After media is in the Decommissioned state, it cannot be allocated again.

<b>Windows Server 2003:  </b>If media is being returned to the free pool, NTMS_USE_ACCESS to the free pool and NTMS_CONTROL_ACCESS to the source pool is required. If the free pool is not the destination media pool, NTMS_CONTROL_ACCESS is required on both source and destination pools.

## -see-also

<a href="/previous-versions/windows/desktop/rsm/media">AllocateNtmsMedia</a>



<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Media Services Functions</a>