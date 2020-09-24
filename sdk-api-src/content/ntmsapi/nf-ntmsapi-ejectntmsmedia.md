---
UID: NF:ntmsapi.EjectNtmsMedia
title: EjectNtmsMedia function (ntmsapi.h)
description: The EjectNtmsMedia function ejects the specified medium from the port of the current library. If the library is busy, RSM queues EjectNtmsMedia and returns success.
helpviewer_keywords: ["EjectNtmsMedia","EjectNtmsMedia function [Files]","NTMS_EJECT_QUEUE","NTMS_EJECT_START","NTMS_EJECT_STOP","_zaw_ejectntmsmedia","base.ejectntmsmedia","fs.ejectntmsmedia","ntmsapi/EjectNtmsMedia"]
old-location: fs\ejectntmsmedia.htm
tech.root: fs
ms.assetid: ecb7374c-d1fa-4e7c-87ad-045122cb466e
ms.date: 12/05/2018
ms.keywords: EjectNtmsMedia, EjectNtmsMedia function [Files], NTMS_EJECT_QUEUE, NTMS_EJECT_START, NTMS_EJECT_STOP, _zaw_ejectntmsmedia, base.ejectntmsmedia, fs.ejectntmsmedia, ntmsapi/EjectNtmsMedia
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
 - EjectNtmsMedia
 - ntmsapi/EjectNtmsMedia
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
 - EjectNtmsMedia
---

# EjectNtmsMedia function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>EjectNtmsMedia</b> function ejects the specified medium from the port of the current library. If the library is busy, RSM queues 
<b>EjectNtmsMedia</b> and returns success.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpMediaId [in]

Unique identifier of a piece of physical media (PMID).

### -param lpEjectOperation [in, out]

GUID of the eject process library request. If <i>dwAction</i> is NTMS_EJECT_START, this parameter receives the GUID for the operation. If <i>dwAction</i> is NTMS_EJECT_STOP, this parameter must be set to the GUID for the operation to be stopped. This parameter is not used with NTMS_EJECT_QUEUE.

### -param dwAction [in]

Action to perform. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_EJECT_START"></a><a id="ntms_eject_start"></a><dl>
<dt><b>NTMS_EJECT_START</b></dt>
</dl>
</td>
<td width="60%">
Start the eject operation with a port. The specified medium is ejected until the time-out event occurs or the function is called again with NTMS_EJECT_STOP. The time-out value is specified in the library object and is applied to all ejections in the library.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_EJECT_STOP"></a><a id="ntms_eject_stop"></a><dl>
<dt><b>NTMS_EJECT_STOP</b></dt>
</dl>
</td>
<td width="60%">
Terminate the ejection process specified by <i>lpEjectOperation</i> before the time-out event lapses.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_EJECT_QUEUE"></a><a id="ntms_eject_queue"></a><dl>
<dt><b>NTMS_EJECT_QUEUE</b></dt>
</dl>
</td>
<td width="60%">
Queue the specified media for ejection. Used to group media for multi-slot NTMS_IEPORT objects.

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
NTMS_CONTROL_ACCESS to the library is denied. Other security errors are also possible, but they would indicate a security subsystem error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUSY</b></dt>
</dl>
</td>
<td width="60%">
More media was queued than slots available in the NTMS_IEPORT object.

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
The library is disabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The session ID is missing or is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
A stop was performed on an operation ID that was not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A library ID or operation ID pointer is missing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_LIBRARY_OFFLINE</b></dt>
</dl>
</td>
<td width="60%">
The library ID refers to an offline library that cannot eject media.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MEDIA_NOT_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The media is disabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was an allocation failure during processing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The eject is queued.

</td>
</tr>
</table>

## -remarks

The 
<b>EjectNtmsMedia</b> function returns to the application as soon as the eject request is queued.

Media ejected using the 
<b>EjectNtmsMedia</b> function is moved to the offline library or deleted from the database. Cleaner cartridges, import media, unrecognized media, and incompatible media are deleted when ejected.

The NTMS_EJECT_QUEUE flag is used to bundle or batch media marked for ejection into a multi-slot library. You can queue media for ejection using the queue action when the application has queued all the necessary media. The application uses the start command to begin the physical eject operation. If more media is queued than slots in the NTMS_IEPORT object, 
<b>EjectNtmsMedia</b> returns ERROR_BUSY. To begin the physical eject operation, the application can use NTMS_EJECT_START with the last media ID or <b>NULL</b>.

If the media is currently in use (mounted or opened), this function returns an error.

If the library does not have a port, use the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-accessntmslibrarydoor">AccessNtmsLibraryDoor</a> function to insert and eject media.

The 
<b>EjectNtmsMedia</b> function does not work with the offline library.

## -see-also

<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-injectntmsmedia">InjectNtmsMedia</a>



<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Library Control Functions</a>