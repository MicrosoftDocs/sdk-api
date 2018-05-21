---
UID: NF:fileapi.GetDriveTypeW
title: GetDriveTypeW function
author: windows-driver-content
description: Determines whether a disk drive is a removable, fixed, CD-ROM, RAM disk, or network drive.
old-location: fs\getdrivetype.htm
old-project: FileIO
ms.assetid: b3989a3f-fc90-4ea0-8d3e-8e57068a08bc
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: GetDriveType, GetDriveType function [Files], GetDriveTypeA, GetDriveTypeW, _win32_getdrivetype, base.getdrivetype, fileapi/GetDriveType, fileapi/GetDriveTypeA, fileapi/GetDriveTypeW, fs.getdrivetype, winbase/GetDriveType, winbase/GetDriveTypeA, winbase/GetDriveTypeW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetDriveTypeW (Unicode) and GetDriveTypeA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: STREAM_INFO_LEVELS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-File-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-Core-File-l1-2-0.dll
-	API-MS-Win-Core-File-l1-2-1.dll
-	API-MS-Win-Core-File-l1-2-2.dll
-	API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
-	MinKernelBase.dll
api_name:
-	GetDriveType
-	GetDriveTypeA
-	GetDriveTypeW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Internet Explorer 5
---

# GetDriveTypeW function


## -description


Determines whether a disk drive is a removable, fixed, CD-ROM, RAM disk, or network 
    drive.

To determine whether a drive is a USB-type drive, call 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff551967">SetupDiGetDeviceRegistryProperty</a> 
    and specify the <b>SPDRP_REMOVAL_POLICY</b> property.


## -parameters




### -param lpRootPathName [in, optional]

The root directory for the drive.
      

A trailing backslash is required. If this parameter is <b>NULL</b>, the function uses the 
       root of the current directory.


## -returns



The return value specifies the type of drive, which can be one of the following values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRIVE_UNKNOWN</b></dt>
<dt>0</dt>
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
<dt>1</dt>
</dl>
</td>
<td width="60%">
The root path is invalid; for example, there is no volume mounted at the specified path.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRIVE_REMOVABLE</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The drive has removable media; for example, a floppy drive, thumb drive, or flash card reader.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRIVE_FIXED</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The drive has fixed media; for example, a hard disk drive or flash drive.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRIVE_REMOTE</b></dt>
<dt>4</dt>
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
<dt>5</dt>
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
<dt>6</dt>
</dl>
</td>
<td width="60%">
The drive is a RAM disk.

</td>
</tr>
</table>
 




## -remarks



In Windows 8 and Windows Server 2012, this function is supported by the following technologies.

<table>
<tr>
<th>Technology</th>
<th>Supported</th>
</tr>
<tr>
<td>
Server Message Block (SMB) 3.0 protocol

</td>
<td>
No

</td>
</tr>
<tr>
<td>
SMB 3.0 Transparent Failover (TFO)

</td>
<td>
No

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
No

</td>
</tr>
<tr>
<td>
Cluster Shared Volume File System (CsvFS)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
Resilient File System (ReFS)

</td>
<td>
Yes

</td>
</tr>
</table>
 

SMB does not support volume management functions.




## -see-also




<a href="https://msdn.microsoft.com/4fe14c49-3fd6-48b7-92de-a0c867b2e042">GetDiskFreeSpace</a>



<a href="https://msdn.microsoft.com/dc985126-970c-49f2-877f-3759125e43b6">Volume Management Functions</a>
 

 

