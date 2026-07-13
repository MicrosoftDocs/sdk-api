---
UID: NF:fileapi.GetDiskFreeSpaceExA
title: GetDiskFreeSpaceExA function (fileapi.h)
description: Retrieves information about the amount of space that is available on a disk volume, which is the total amount of space, the total amount of free space, and the total amount of free space available to the user that is associated with the calling thread. (ANSI)
helpviewer_keywords: ["GetDiskFreeSpaceExA", "fileapi/GetDiskFreeSpaceExA"]
old-location: fs\getdiskfreespaceex.htm
tech.root: fs
ms.assetid: a52f2dbd-bda6-4217-9e72-f100f8bbe334
ms.date: 12/05/2018
ms.keywords: GetDiskFreeSpaceEx, GetDiskFreeSpaceEx function [Files], GetDiskFreeSpaceExA, GetDiskFreeSpaceExW, _win32_getdiskfreespaceex, base.getdiskfreespaceex, fileapi/GetDiskFreeSpaceEx, fileapi/GetDiskFreeSpaceExA, fileapi/GetDiskFreeSpaceExW, fs.getdiskfreespaceex, winbase/GetDiskFreeSpaceEx, winbase/GetDiskFreeSpaceExA, winbase/GetDiskFreeSpaceExW
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetDiskFreeSpaceExW (Unicode) and GetDiskFreeSpaceExA (ANSI)
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
 - GetDiskFreeSpaceExA
 - fileapi/GetDiskFreeSpaceExA
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
 - GetDiskFreeSpaceEx
 - GetDiskFreeSpaceExA
 - GetDiskFreeSpaceExW
---

# GetDiskFreeSpaceExA function


## -description

Retrieves information about the amount of space that is available on a disk volume, which is the total 
    amount of space, the total amount of free space, and the total amount of free space available to the user that is 
    associated with the calling thread.

## -parameters

### -param lpDirectoryName [in, optional]

A directory on the disk.

If this parameter is <b>NULL</b>, the function uses the root of the current disk.

If this parameter is a UNC name, it must include a trailing backslash, for example, 
       "\\\\MyServer\\MyShare\\".

This parameter does not have to specify the root directory on a disk. The function accepts any directory on a 
       disk.

The calling application must have <b>FILE_LIST_DIRECTORY</b> access rights for this  
       directory.

### -param lpFreeBytesAvailableToCaller [out, optional]

A pointer to a variable that receives the total number of free bytes on a disk that are available to the user 
       who is associated with the calling thread.

This parameter can be <b>NULL</b>.

If per-user quotas are being used, this value may be less than the total number of free bytes on a disk.

### -param lpTotalNumberOfBytes [out, optional]

A pointer to a variable that receives the total number of bytes on a disk that are available to the user who 
       is associated with the calling thread.

This parameter can be <b>NULL</b>.

If per-user quotas are being used, this value may be less than the total number of bytes on a disk.

To determine the total number of bytes on a disk or volume, use 
       <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_length_info">IOCTL_DISK_GET_LENGTH_INFO</a>.

### -param lpTotalNumberOfFreeBytes [out, optional]

A pointer to a variable that receives the total number of free bytes on a disk.

This parameter can be <b>NULL</b>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero (0). To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The values obtained by this function are of the type 
    <a href="/windows/win32/api/winnt/ns-winnt-ularge_integer~r1">ULARGE_INTEGER</a>. Do not truncate these values to 32 
     bits.

The <b>GetDiskFreeSpaceEx</b> function returns zero (0) 
    for <i>lpTotalNumberOfFreeBytes</i> and <i>lpFreeBytesAvailable</i> for all 
    CD requests unless the disk is an unwritten CD in a CD-RW drive.

Symbolic link behavior—If the path points to a symbolic link, the operation is performed 
    on the target.





> [!NOTE]
> The fileapi.h header defines GetDiskFreeSpaceEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/FileIO/disk-management-functions">Disk Management Functions</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getdiskfreespacea">GetDiskFreeSpace</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea">GetModuleHandle</a>
