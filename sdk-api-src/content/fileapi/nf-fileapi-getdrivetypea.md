---
UID: NF:fileapi.GetDriveTypeA
title: GetDriveTypeA function (fileapi.h)
description: Determines whether a disk drive is a removable, fixed, CD-ROM, RAM disk, or network drive. (ANSI)
helpviewer_keywords: ["GetDriveTypeA", "fileapi/GetDriveTypeA"]
old-location: fs\getdrivetype.htm
tech.root: fs
ms.assetid: b3989a3f-fc90-4ea0-8d3e-8e57068a08bc
ms.date: 12/05/2018
ms.keywords: GetDriveType, GetDriveType function [Files], GetDriveTypeA, GetDriveTypeW, _win32_getdrivetype, base.getdrivetype, fileapi/GetDriveType, fileapi/GetDriveTypeA, fileapi/GetDriveTypeW, fs.getdrivetype, winbase/GetDriveType, winbase/GetDriveTypeA, winbase/GetDriveTypeW
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetDriveTypeW (Unicode) and GetDriveTypeA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetDriveTypeA
 - fileapi/GetDriveTypeA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-file-l1-2-5.dll
 - api-ms-win-core-file-l1-2-4.dll
 - api-ms-win-core-file-l1-2-3.dll
 - Kernel32.dll
 - API-MS-Win-Core-File-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l1-2-0.dll
 - API-MS-Win-Core-File-l1-2-1.dll
 - API-MS-Win-Core-File-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - GetDriveType
 - GetDriveTypeA
 - GetDriveTypeW
---

# GetDriveTypeA function


## -description

Determines whether a disk drive is a removable, fixed, CD-ROM, RAM disk, or network 
    drive.

To determine whether a drive is a USB-type drive, call 
    <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdeviceregistrypropertya">SetupDiGetDeviceRegistryProperty</a> 
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





> [!NOTE]
> The fileapi.h header defines GetDriveType as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-getdiskfreespacea">GetDiskFreeSpace</a>



<a href="/windows/desktop/FileIO/volume-management-functions">Volume Management Functions</a>
