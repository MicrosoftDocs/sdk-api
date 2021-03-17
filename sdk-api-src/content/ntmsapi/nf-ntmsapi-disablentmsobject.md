---
UID: NF:ntmsapi.DisableNtmsObject
title: DisableNtmsObject function (ntmsapi.h)
description: The DisableNtmsObject function disables the specified RSM object.
helpviewer_keywords: ["DisableNtmsObject","DisableNtmsObject function [Files]","NTMS_DRIVE","NTMS_LIBRARY","NTMS_PHYSICAL_MEDIA","_zaw_disablentmsobject","base.disablentmsobject","fs.disablentmsobject","ntmsapi/DisableNtmsObject"]
old-location: fs\disablentmsobject.htm
tech.root: fs
ms.assetid: 409d1ab6-c611-4118-aa10-095d585c099a
ms.date: 12/05/2018
ms.keywords: DisableNtmsObject, DisableNtmsObject function [Files], NTMS_DRIVE, NTMS_LIBRARY, NTMS_PHYSICAL_MEDIA, _zaw_disablentmsobject, base.disablentmsobject, fs.disablentmsobject, ntmsapi/DisableNtmsObject
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
 - DisableNtmsObject
 - ntmsapi/DisableNtmsObject
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
 - DisableNtmsObject
---

# DisableNtmsObject function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>DisableNtmsObject</b> function disables the specified RSM object.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param dwType [in]

RSM object type. This parameter can be one of the following values from the 
<a href="/windows/desktop/api/ntmsapi/ne-ntmsapi-ntmsobjectstypes">NtmsObjectsTypes</a> enumeration type. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_DRIVE"></a><a id="ntms_drive"></a><dl>
<dt><b>NTMS_DRIVE</b></dt>
</dl>
</td>
<td width="60%">
Drive

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LIBRARY"></a><a id="ntms_library"></a><dl>
<dt><b>NTMS_LIBRARY</b></dt>
</dl>
</td>
<td width="60%">
Library

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_PHYSICAL_MEDIA"></a><a id="ntms_physical_media"></a><dl>
<dt><b>NTMS_PHYSICAL_MEDIA</b></dt>
</dl>
</td>
<td width="60%">
Physical media (tape, optical disk, CD, or magnetic cartridge)

</td>
</tr>
</table>

### -param lpObjectId [in]

Unique identifier of the RSM object.

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
NTMS_MODIFY_ACCESS to the library containing the object is denied. Other security errors are possible, but indicate a security subsystem error.

<b>Windows XP:  </b>NTMS_CONTROL_ACCESS to the library containing the object is denied. Other security errors are possible, but indicate a security subsystem error.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An object ID is missing or the object type is not valid. (The object type is not valid if it is not NTMS_LIBRARY, NTMS_DRIVE, or NTMS_PHYSICAL_MEDIA.)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The object is already disabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_LIBRARY_OFFLINE</b></dt>
</dl>
</td>
<td width="60%">
The library ID refers to an off-line library that cannot be enabled or disabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The object is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The disable is queued.

</td>
</tr>
</table>

## -remarks

The 
<b>DisableNtmsObject</b> function queues a disable command for the specified object. The function returns successfully when the command is queued. If RSM is busy, the command can take some time to complete. When the medium is disabled, RSM renders all of the media's sides and associated logical media unavailable. All requests to disabled media return errors.

To remove a drive or media changer from service the drive or media changer must first be disabled.

All objects contained by a disabled object are also disabled. For example, disabling a piece of physical media disables all sides. Whenever possible, when a drive is disabled, the medium in the drive is removed and placed in its slot.

## -see-also

<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-enablentmsobject">EnableNtmsObject</a>



<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Object Management Functions</a>