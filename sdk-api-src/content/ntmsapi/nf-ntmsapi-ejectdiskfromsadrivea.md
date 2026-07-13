---
UID: NF:ntmsapi.EjectDiskFromSADriveA
title: EjectDiskFromSADriveA function (ntmsapi.h)
description: The EjectDiskFromSADrive function ejects the media that is in a standalone removable drive. (ANSI)
helpviewer_keywords: ["EjectDiskFromSADriveA", "NTMS_EJECT_ASK_USER", "NTMS_EJECT_FORCE", "NTMS_EJECT_IMMEDIATE", "NTMS_EJECT_QUEUE", "NTMS_EJECT_START", "NTMS_EJECT_STOP", "ntmsapi/EjectDiskFromSADriveA"]
old-location: fs\ejectdiskfromsadrive.htm
tech.root: fs
ms.assetid: eb1e79b5-f059-4e18-836f-3ba4de97eea2
ms.date: 12/05/2018
ms.keywords: EjectDiskFromSADrive, EjectDiskFromSADrive function [Files], EjectDiskFromSADriveA, EjectDiskFromSADriveW, NTMS_EJECT_ASK_USER, NTMS_EJECT_FORCE, NTMS_EJECT_IMMEDIATE, NTMS_EJECT_QUEUE, NTMS_EJECT_START, NTMS_EJECT_STOP, base.ejectdiskfromsadrive, fs.ejectdiskfromsadrive, ntmsapi/EjectDiskFromSADrive, ntmsapi/EjectDiskFromSADriveA, ntmsapi/EjectDiskFromSADriveW
req.header: ntmsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EjectDiskFromSADriveW (Unicode) and EjectDiskFromSADriveA (ANSI)
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
 - EjectDiskFromSADriveA
 - ntmsapi/EjectDiskFromSADriveA
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
 - EjectDiskFromSADrive
 - EjectDiskFromSADriveA
 - EjectDiskFromSADriveW
---

# EjectDiskFromSADriveA function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>EjectDiskFromSADrive</b> function ejects the  media that is in a standalone removable 
  drive.

## -parameters

### -param lpComputerName [in]

Removable Storage Manager (RSM) server name. If this parameter is <b>NULL</b>, the current computer name is used.

### -param lpAppName [in]

Unique character string that identifies the application. This name identifies resources and operator requests. This parameter is optional and may be <b>NULL</b>.

### -param lpDeviceName [in]

Name of the device to eject.  For example, \\.\Cdrom0 or \\.\PhysicalDriveX (where X is the number of the drive being accessed).

### -param hWnd [in]

 

Handle to a dialog box window for  user confirmation.

### -param lpTitle [in]

Title displayed in a dialog box to get user input.

### -param lpMessage [in]

Message displayed in a dialog box to get user input.

### -param dwOptions [in]

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
Start the eject operation with a port. The specified medium is ejected until the time-out event occurs or the function is called again with <b>NTMS_EJECT_STOP</b>. The time-out value is specified in the library object and is applied to all ejections in the library.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_EJECT_STOP"></a><a id="ntms_eject_stop"></a><dl>
<dt><b>NTMS_EJECT_STOP</b></dt>
</dl>
</td>
<td width="60%">
Terminate the ejection process before the time-out event lapses.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_EJECT_QUEUE"></a><a id="ntms_eject_queue"></a><dl>
<dt><b>NTMS_EJECT_QUEUE</b></dt>
</dl>
</td>
<td width="60%">
Allow the eject to be asynchronous.  The function queues the specified media for ejection and then returns.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_EJECT_FORCE"></a><a id="ntms_eject_force"></a><dl>
<dt><b>NTMS_EJECT_FORCE</b></dt>
</dl>
</td>
<td width="60%">
Force the media to be ejected.  For example, NTFS can hold locks on media, and this option will cause the media to be ejected despite that lock.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_EJECT_IMMEDIATE"></a><a id="ntms_eject_immediate"></a><dl>
<dt><b>NTMS_EJECT_IMMEDIATE</b></dt>
</dl>
</td>
<td width="60%">
Eject the media immediately and synchronously. The function will not return until the eject is complete.  Does not queue the specified media for ejection.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_EJECT_ASK_USER"></a><a id="ntms_eject_ask_user"></a><dl>
<dt><b>NTMS_EJECT_ASK_USER</b></dt>
</dl>
</td>
<td width="60%">
Eject the media immediately and synchronously. The function will not return until the eject is complete.  Does not queue the specified media for ejection.  If the eject operation fails, prompt the user to either cancel or force the operation.

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
The eject operation was successful.

</td>
</tr>
</table>

## -remarks

Although <a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-ejectntmsmedia">EjectNtmsMedia</a> can, in some cases, be used to accomplish the same functionality, <b>EjectDiskFromSADrive</b> provides a convenient way to eject media from a standalone device, by specifying its drive name instead of its RSM name. In some cases it is the only way to overcome file system locks on the media in order to eject that media.

The 
<b>EjectDiskFromSADrive</b> function returns to the application as soon as the eject request is queued, unless <b>NTMS_EJECT_IMMEDIATE</b> option is specified.

Media ejected using the 
<b>EjectDiskFromSADrive</b> function is moved to the offline library or deleted from the database. Import media, unrecognized media, and incompatible media are deleted when ejected.

The 
<b>EjectDiskFromSADrive</b> function does not work with the offline library.





> [!NOTE]
> The ntmsapi.h header defines EjectDiskFromSADrive as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-ejectntmsmedia">EjectNtmsMedia</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-injectntmsmedia">InjectNtmsMedia</a>



<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Library Control Functions</a>
