---
UID: NF:ntmsapi.CleanNtmsDrive
title: CleanNtmsDrive function (ntmsapi.h)
description: The CleanNtmsDrive function queues a cleaning request for the specified drive for cleaning.
helpviewer_keywords: ["CleanNtmsDrive","CleanNtmsDrive function [Files]","_zaw_cleanntmsdrive","base.cleanntmsdrive","fs.cleanntmsdrive","ntmsapi/CleanNtmsDrive"]
old-location: fs\cleanntmsdrive.htm
tech.root: fs
ms.assetid: 55a8e7c0-85fd-40c5-b5b9-46ad321761c4
ms.date: 12/05/2018
ms.keywords: CleanNtmsDrive, CleanNtmsDrive function [Files], _zaw_cleanntmsdrive, base.cleanntmsdrive, fs.cleanntmsdrive, ntmsapi/CleanNtmsDrive
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
 - CleanNtmsDrive
 - ntmsapi/CleanNtmsDrive
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
 - CleanNtmsDrive
---

# CleanNtmsDrive function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>CleanNtmsDrive</b> function queues a cleaning request for the specified drive for cleaning.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpDriveId [in]

Unique identifier of the drive to be cleaned.

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
NTMS_CONTROL_ACCESS to the library is denied. Other security errors are also possible, but they would indicate a security subsystem error.

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
<dt><b>ERROR_RESOURCE_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
The drive or the library is not enabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The cleaning was queued successfully.

</td>
</tr>
</table>

## -remarks

If the drive you selected in the 
<b>CleanNtmsDrive</b> function is a stand-alone drive, the drive is marked as cleaned and the time is noted in the 
<a href="/previous-versions/windows/desktop/rsm/rsm-database">RSM Database</a>.

Queued cleaning requests are deleted when the service is restarted.

## -see-also

<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Cleaner Management Functions</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-ejectntmscleaner">EjectNtmsCleaner</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-injectntmscleaner">InjectNtmsCleaner</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-releasentmscleanerslot">ReleaseNtmsCleanerSlot</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-reserventmscleanerslot">ReserveNtmsCleanerSlot</a>