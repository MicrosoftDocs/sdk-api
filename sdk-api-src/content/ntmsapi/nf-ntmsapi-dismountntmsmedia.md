---
UID: NF:ntmsapi.DismountNtmsMedia
title: DismountNtmsMedia function (ntmsapi.h)
description: The DismountNtmsMedia function queues a command to move the specified media in a drive to its storage. This function should be paired with the MountNtmsMedia function.
helpviewer_keywords: ["DismountNtmsMedia","DismountNtmsMedia function [Files]","NTMS_DISMOUNT_DEFERRED","NTMS_DISMOUNT_IMMEDIATE","_zaw_dismountntmsmedia","base.dismountntmsmedia","fs.dismountntmsmedia","ntmsapi/DismountNtmsMedia"]
old-location: fs\dismountntmsmedia.htm
tech.root: fs
ms.assetid: 95336487-ca50-4003-a155-eb70173f8604
ms.date: 12/05/2018
ms.keywords: DismountNtmsMedia, DismountNtmsMedia function [Files], NTMS_DISMOUNT_DEFERRED, NTMS_DISMOUNT_IMMEDIATE, _zaw_dismountntmsmedia, base.dismountntmsmedia, fs.dismountntmsmedia, ntmsapi/DismountNtmsMedia
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
 - DismountNtmsMedia
 - ntmsapi/DismountNtmsMedia
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
 - DismountNtmsMedia
---

# DismountNtmsMedia function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>DismountNtmsMedia</b> function queues a command to move the specified media in a drive to its storage. This function should be paired with the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-mountntmsmedia">MountNtmsMedia</a> function.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpMediaId [in]

Array of at least one logical medium or side.

### -param dwCount [in]

Number of media identifiers in the <i>lpMediaId</i> parameter.

### -param dwOptions [in]

Options. This parameter can be the following value. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_DISMOUNT_DEFERRED"></a><a id="ntms_dismount_deferred"></a><dl>
<dt><b>NTMS_DISMOUNT_DEFERRED</b></dt>
</dl>
</td>
<td width="60%">
Marks media state as Dismountable, and keeps the medium in the drive. Subsequent mount requests are satisfied using dismounted or dismountable drives. The default is to dismount immediately.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_DISMOUNT_IMMEDIATE"></a><a id="ntms_dismount_immediate"></a><dl>
<dt><b>NTMS_DISMOUNT_IMMEDIATE</b></dt>
</dl>
</td>
<td width="60%">
Dismount the drive immediately.

</td>
</tr>
</table>

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
NTMS_USE_ACCESS to the media pool or library that contains the media is denied. Other security errors are also possible, but they would indicate a security subsystem error.

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
<dt><b>ERROR_DEVICE_NOT_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
One or more resources required to perform the dismount are not currently available (probably disabled).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_LIBRARY</b></dt>
</dl>
</td>
<td width="60%">
The library that contains the media is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_MEDIA</b></dt>
</dl>
</td>
<td width="60%">
At least one of the specified media is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
An unexpected media or device state occurred during dismount.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MEDIA_OFFLINE</b></dt>
</dl>
</td>
<td width="60%">
The specified media is offline.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MEDIA_NOT_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
One or more media resources required to perform the mount are not currently available (probably disabled).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred during processing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The media dismount has been queued.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The time-out event expired while the application attempted to acquire one or more resources.

</td>
</tr>
</table>

## -remarks

An application must use the 
<b>DismountNtmsMedia</b> function to release the drive resource after the application has used the specified medium. Unreleased media cannot be used by other RSM sessions.

The 
<b>DismountNtmsMedia</b> function returns as soon as the operation is queued with RSM. The application can wait for the side state to become idle.

## -see-also

<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Media Services Functions</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-mountntmsmedia">MountNtmsMedia</a>