---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# DriveType function


## -description


<p class="CCE_Message">[<b>DriveType</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Determines the drive type based on the drive number.


## -parameters




### -param iDrive [in]

Type: <b>int</b>

The number of the drive that you want to test. "A:" corresponds to 0, "B:" to 1, and so on.


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
 




## -remarks



<b>DriveType</b> is equivalent to calling <a href="https://msdn.microsoft.com/c4e55b50-637a-446f-aa9c-7d8c71d8071c">RealDriveType</a>. <b>RealDriveType</b> is the preferred function.




## -see-also




<a href="https://msdn.microsoft.com/b3989a3f-fc90-4ea0-8d3e-8e57068a08bc">GetDriveType</a>



<a href="https://msdn.microsoft.com/c4e55b50-637a-446f-aa9c-7d8c71d8071c">RealDriveType</a>
 

 

