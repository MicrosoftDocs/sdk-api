---
UID: NF:ntmsapi.DecommissionNtmsMedia
title: DecommissionNtmsMedia function (ntmsapi.h)
description: The DecommissionNtmsMedia function moves a side from the Available state to the Decommissioned state.
helpviewer_keywords: ["DecommissionNtmsMedia","DecommissionNtmsMedia function [Files]","_zaw_decommissionntmsmedia","base.decommissionntmsmedia","fs.decommissionntmsmedia","ntmsapi/DecommissionNtmsMedia"]
old-location: fs\decommissionntmsmedia.htm
tech.root: fs
ms.assetid: 2bb1a54b-6308-4ccd-9fc6-1b11f4432a3f
ms.date: 12/05/2018
ms.keywords: DecommissionNtmsMedia, DecommissionNtmsMedia function [Files], _zaw_decommissionntmsmedia, base.decommissionntmsmedia, fs.decommissionntmsmedia, ntmsapi/DecommissionNtmsMedia
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
 - DecommissionNtmsMedia
 - ntmsapi/DecommissionNtmsMedia
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
 - DecommissionNtmsMedia
---

# DecommissionNtmsMedia function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>DecommissionNtmsMedia</b> function moves a side from the Available state to the Decommissioned state.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpMediaId [in]

Unique identifier of a side of a piece of physical media.

## -returns

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
The media pool for media is not valid.

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
The media is not in the Available state.

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

Media decommissioned by the 
<b>DecommissionNtmsMedia</b> function is recognized by RSM but the decommissioned media does not contain any data and is never again used.

Only media that is in the Available state can be decommissioned. For more information, see 
<a href="/previous-versions/windows/desktop/rsm/media-life-cycle">Media Life Cycle</a>.

## -see-also

<a href="/previous-versions/windows/desktop/rsm/media">AllocateNtmsMedia</a>



<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Media Services Functions</a>