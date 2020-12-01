---
UID: NF:ntmsapi.DismountNtmsDrive
title: DismountNtmsDrive function (ntmsapi.h)
description: The DismountNtmsDrive function queues a command to move the media in the specified drive to its storage slot. This function should be paired with the MountNtmsMedia function.
helpviewer_keywords: ["DismountNtmsDrive","DismountNtmsDrive function [Files]","_zaw_dismountntmsdrive","base.dismountntmsdrive","fs.dismountntmsdrive","ntmsapi/DismountNtmsDrive"]
old-location: fs\dismountntmsdrive.htm
tech.root: fs
ms.assetid: dbec501c-a7bc-4679-afe1-df833dcb932d
ms.date: 12/05/2018
ms.keywords: DismountNtmsDrive, DismountNtmsDrive function [Files], _zaw_dismountntmsdrive, base.dismountntmsdrive, fs.dismountntmsdrive, ntmsapi/DismountNtmsDrive
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
 - DismountNtmsDrive
 - ntmsapi/DismountNtmsDrive
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
 - DismountNtmsDrive
---

# DismountNtmsDrive function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>DismountNtmsDrive</b> function queues a command to move the media in the specified drive to its storage slot. This function should be paired with the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-mountntmsmedia">MountNtmsMedia</a> function.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpDriveId [in]

Unique identifier of a drive object.

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

<b>Windows XP:  </b>NTMS_CONTROL_ACCESS to the library is denied. Other security errors are also possible, but they would indicate a security subsystem error.

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
The drive or library is not enabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DRIVE</b></dt>
</dl>
</td>
<td width="60%">
The drive ID is not valid.

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
The library for the drive is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The drive ID is missing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The drive does not contain media.

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

If the drive specified by the 
<b>DismountNtmsDrive</b> function is empty or if the media is opened, an error is returned. Otherwise, the media is returned to its slot.

Dismount requests to stand alone drives place the drive in the dismountable state and return success.

## -see-also

<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Library Control Functions</a>