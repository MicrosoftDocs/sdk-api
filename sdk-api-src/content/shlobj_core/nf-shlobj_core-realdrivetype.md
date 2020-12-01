---
UID: NF:shlobj_core.RealDriveType
title: RealDriveType function (shlobj_core.h)
description: RealDriveType may be altered or unavailable.
helpviewer_keywords: ["RealDriveType","RealDriveType function [Windows Shell]","_win32_RealDriveType","shell.RealDriveType","shlobj_core/RealDriveType"]
old-location: shell\RealDriveType.htm
tech.root: shell
ms.assetid: c4e55b50-637a-446f-aa9c-7d8c71d8071c
ms.date: 12/05/2018
ms.keywords: RealDriveType, RealDriveType function [Windows Shell], _win32_RealDriveType, shell.RealDriveType, shlobj_core/RealDriveType
req.header: shlobj_core.h
req.include-header: Shlobj.h
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RealDriveType
 - shlobj_core/RealDriveType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - RealDriveType
---

# RealDriveType function


## -description

<p class="CCE_Message">[<b>RealDriveType</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Determines the drive type based on the drive number.

## -parameters

### -param iDrive [in]

Type: <b>int</b>

The number of the drive that you want to test. "A:" corresponds to 0, "B:" to 1, and so on.

### -param fOKToHitNet [in]

Type: <b>BOOL</b>

Reserved. Must be set to 0.

## -returns

Type: <b>int</b>

Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRIVE_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
The drive type cannot be determined.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRIVE_NO_ROOT_DIR</b></dt>
</dl>
</td>
<td width="60%">
The root path is invalid. For example, no volume is mounted at the path.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRIVE_REMOVABLE</b></dt>
</dl>
</td>
<td width="60%">
The disk can be removed from the drive.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRIVE_FIXED</b></dt>
</dl>
</td>
<td width="60%">
The disk cannot be removed from the drive.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRIVE_REMOTE</b></dt>
</dl>
</td>
<td width="60%">
The drive is a remote (network) drive.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRIVE_CDROM</b></dt>
</dl>
</td>
<td width="60%">
The drive is a CD-ROM drive.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRIVE_RAMDISK</b></dt>
</dl>
</td>
<td width="60%">
The drive is a RAM disk.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/shlobj/nf-shlobj-drivetype">DriveType</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getdrivetypea">GetDriveType</a>