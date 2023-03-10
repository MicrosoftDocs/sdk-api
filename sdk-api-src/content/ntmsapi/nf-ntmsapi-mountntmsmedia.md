---
UID: NF:ntmsapi.MountNtmsMedia
title: MountNtmsMedia function (ntmsapi.h)
description: The MountNtmsMedia function synchronously mounts one or more pieces of media.
helpviewer_keywords: ["MountNtmsMedia","MountNtmsMedia function [Files]","NTMS_MOUNT_ERROR_NOT_AVAILABLE","NTMS_MOUNT_ERROR_OFFLINE","NTMS_MOUNT_READ","NTMS_MOUNT_SPECIFIC_DRIVE","NTMS_MOUNT_WRITE","NTMS_PRIORITY_HIGH","NTMS_PRIORITY_HIGHEST","NTMS_PRIORITY_LOW","NTMS_PRIORITY_LOWEST","NTMS_PRIORITY_NORMAL","_zaw_mountntmsmedia","base.mountntmsmedia","fs.mountntmsmedia","ntmsapi/MountNtmsMedia"]
old-location: fs\mountntmsmedia.htm
tech.root: fs
ms.assetid: f943f36c-654a-48ed-aeb2-1fc146f2d9ff
ms.date: 12/05/2018
ms.keywords: MountNtmsMedia, MountNtmsMedia function [Files], NTMS_MOUNT_ERROR_NOT_AVAILABLE, NTMS_MOUNT_ERROR_OFFLINE, NTMS_MOUNT_READ, NTMS_MOUNT_SPECIFIC_DRIVE, NTMS_MOUNT_WRITE, NTMS_PRIORITY_HIGH, NTMS_PRIORITY_HIGHEST, NTMS_PRIORITY_LOW, NTMS_PRIORITY_LOWEST, NTMS_PRIORITY_NORMAL, _zaw_mountntmsmedia, base.mountntmsmedia, fs.mountntmsmedia, ntmsapi/MountNtmsMedia
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
 - MountNtmsMedia
 - ntmsapi/MountNtmsMedia
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
 - MountNtmsMedia
---

# MountNtmsMedia function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>MountNtmsMedia</b> function synchronously mounts one or more pieces of media.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpMediaId [in]

Array of unique identifiers of logical media or sides.

### -param lpDriveId [in, out]

Array of drive identifiers that corresponds to the list of media in the <i>lpMediaId</i> parameter. This array either specifies a list of drives to mount media into or receives the list of drives that media is mounted into on operation completion. See the NTMS_MOUNT_SPECIFIC_DRIVE value below. If the 
<b>MountNtmsMedia</b> function times out prior to the completion of the mount, RSM does not return the list of drives.

### -param dwCount [in]

Number of media identifiers and drive identifiers passed in the <i>lpMediaId</i> and <i>lpDriveId</i> parameters. Note that <i>lpMediaId</i> and <i>lpDriveId</i> must point to the first element of equal-length arrays.

### -param dwOptions [in]

Options. This parameter can be one or more of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_MOUNT_SPECIFIC_DRIVE"></a><a id="ntms_mount_specific_drive"></a><dl>
<dt><b>NTMS_MOUNT_SPECIFIC_DRIVE</b></dt>
</dl>
</td>
<td width="60%">
Mount the media into the specific drives provided in the <i>lpDriveId</i> parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_MOUNT_READ"></a><a id="ntms_mount_read"></a><dl>
<dt><b>NTMS_MOUNT_READ</b></dt>
</dl>
</td>
<td width="60%">
Mount the media for read access. Use this value to mount read-only media.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_MOUNT_WRITE"></a><a id="ntms_mount_write"></a><dl>
<dt><b>NTMS_MOUNT_WRITE</b></dt>
</dl>
</td>
<td width="60%">
Mount the media for write access. Use this flag to prevent RSM from mounting Completed media. This value can be combined with NTMS_MOUNT_READ for read/write access. 




RSM cannot mount Completed media if this flag is selected.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_MOUNT_ERROR_NOT_AVAILABLE"></a><a id="ntms_mount_error_not_available"></a><dl>
<dt><b>NTMS_MOUNT_ERROR_NOT_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
This value returns an error if the media or a drive is not available.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_MOUNT_ERROR_OFFLINE"></a><a id="ntms_mount_error_offline"></a><dl>
<dt><b>NTMS_MOUNT_ERROR_OFFLINE</b></dt>
</dl>
</td>
<td width="60%">
Do not issue an operator request to mount offline media. Return an error if the media specified is not currently in a library.

</td>
</tr>
</table>

### -param dwPriority [in]

Priority of the mount used by RSM to allow access to drives. Priorities range from -15 to 15, with 15 the highest priority and 0 is the default. This parameter can also take one of the following constants. An application should pass NTMS_PRIORITY_NORMAL unless a special mount priority is required. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_PRIORITY_NORMAL"></a><a id="ntms_priority_normal"></a><dl>
<dt><b>NTMS_PRIORITY_NORMAL</b></dt>
</dl>
</td>
<td width="60%">
Mounts that are not time critical.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_PRIORITY_LOW"></a><a id="ntms_priority_low"></a><dl>
<dt><b>NTMS_PRIORITY_LOW</b></dt>
</dl>
</td>
<td width="60%">
Mounts performed as a background activity.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_PRIORITY_HIGH"></a><a id="ntms_priority_high"></a><dl>
<dt><b>NTMS_PRIORITY_HIGH</b></dt>
</dl>
</td>
<td width="60%">
Mounts that are time critical.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_PRIORITY_LOWEST"></a><a id="ntms_priority_lowest"></a><dl>
<dt><b>NTMS_PRIORITY_LOWEST</b></dt>
</dl>
</td>
<td width="60%">
Lowest priority mount.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_PRIORITY_HIGHEST"></a><a id="ntms_priority_highest"></a><dl>
<dt><b>NTMS_PRIORITY_HIGHEST</b></dt>
</dl>
</td>
<td width="60%">
Highest priority mount.

</td>
</tr>
</table>

### -param dwTimeout [in]

Maximum time allowed to mount the specified media, in milliseconds. Set this parameter to INFINITE to wait until the mount is completed.

### -param lpMountInformation

This parameter is reserved and should be <b>NULL</b>.

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
NTMS_USE_ACCESS to the media pool or library that contains the media is denied; other security errors are also possible but they would indicate a security subsystem error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUSY</b></dt>
</dl>
</td>
<td width="60%">
The media or drives are busy.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The request was canceled by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-closentmssession">CloseNtmsSession</a> function.

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
<dt><b>ERROR_DRIVE_MEDIA_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The media and drive specified are not in the same library.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DRIVE</b></dt>
</dl>
</td>
<td width="60%">
At least one of the specified drives is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_LIBRARY</b></dt>
</dl>
</td>
<td width="60%">
The library that contains the drives or media is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_MEDIA</b></dt>
</dl>
</td>
<td width="60%">
One or more of the media specified is not valid, or there are duplicate media IDs in list of media.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
An unexpected media or device state occurred during mount.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MEDIA_OFFLINE</b></dt>
</dl>
</td>
<td width="60%">
The media is offline and cannot be mounted.

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
<dt><b>ERROR_REQUEST_REFUSED</b></dt>
</dl>
</td>
<td width="60%">
The user canceled the request through the user interface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_RESOURCE_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
One or more resources required to perform the mount are disabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The media has been mounted and is ready for use.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The time-out event expired while attempting to acquire one or more required resources. The mount request has been canceled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WRITE_PROTECT</b></dt>
</dl>
</td>
<td width="60%">
The media state is set to Completed and the NTMS_MOUNT_WRITE value was specified.

</td>
</tr>
</table>

## -remarks

The 
<b>MountNtmsMedia</b> function queues a request to mount the specified media, then waits for the number of milliseconds specified in the <i>dwTimeout</i> parameter for the mount to complete or for an error to be detected. If RSM cannot complete the mount operation before <i>dwTimeout</i> expires, NTMS cancels the request and returns an error. If the specified media is in an offline library, the application might be blocked for an extended period of time. You can use the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-getntmsobjectinformation">GetNtmsObjectInformation</a> function to determine the current location of the specified medium. You can also use the NTMS_MOUNT_ERROR_OFFLINE value to generate an immediate error instead of an operator request when the media is offline.

If the specified medium is in use or a drive is not available, the process blocks up to the time-out value and returns ERROR_BUSY. If the NTMS_MOUNT_ERROR_NOT_AVAILABLE value is specified, the function returns an immediate error when a resource (media or drive) is not available.

The time-out value of INFINITE can be used to make the function wait without timing out. When a non-zero time-out value is specified in the <i>dwTimeout</i> parameter, RSM waits for all the media specified in <i>lpMediaId</i> to become mounted. If the specified time elapses before all the media is mounted, the 
<b>MountNtmsMedia</b> function returns an error and cancels the request. The application can examine the status returned and resubmit the request if desired.

When multiple media to be mounted are specified with a single call, all the specified media must be in a single library. If any of the specified media are offline, none of the media will be mounted until all the media are online.

At the completion of the mount the drive state (for example, fix or variable mode) is not defined. The application must set up the drive.

The 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-closentmssession">CloseNtmsSession</a> function can be used to cancel a mount that is pending. The default behavior is:

<ul>
<li>If the specified medium is offline, RSM posts an operator request to mount the media and the 
<b>MountNtmsMedia</b> function waits for the period of time specified in the <i>dwTimeout</i> parameter.</li>
<li>If the specified medium is online, RSM requests the mount.</li>
<li>If a drive or media is not available, RSM sends the request and the 
<b>MountNtmsMedia</b> function waits for the period of time specified in the <i>dwTimeout</i> parameter.</li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Media Services Functions</a>