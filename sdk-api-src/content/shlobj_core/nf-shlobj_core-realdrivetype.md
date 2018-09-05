---
UID: NF:shlobj_core.RealDriveType
title: RealDriveType function
author: windows-sdk-content
description: RealDriveType may be altered or unavailable.
old-location: shell\RealDriveType.htm
old-project: shell
ms.assetid: c4e55b50-637a-446f-aa9c-7d8c71d8071c
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: RealDriveType, RealDriveType function [Windows Shell], _win32_RealDriveType, shell.RealDriveType, shlobj_core/RealDriveType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.redist: 
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
tech.root: 
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - RealDriveType
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
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




<a href="https://msdn.microsoft.com/3089656d-2e64-4d65-aa18-0a451d82fa95">DriveType</a>



<a href="https://msdn.microsoft.com/b3989a3f-fc90-4ea0-8d3e-8e57068a08bc">GetDriveType</a>
 

 

