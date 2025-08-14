---
UID: NF:fileapi.GetDiskFreeSpaceW
title: GetDiskFreeSpaceW function (fileapi.h)
description: Retrieves information about the specified disk, including the amount of free space on the disk. (Unicode)
helpviewer_keywords: ["GetDiskFreeSpace", "GetDiskFreeSpace function [Files]", "GetDiskFreeSpaceW", "_win32_getdiskfreespace", "base.getdiskfreespace", "fileapi/GetDiskFreeSpace", "fileapi/GetDiskFreeSpaceW", "fs.getdiskfreespace"]
old-location: fs\getdiskfreespace.htm
tech.root: fs
ms.assetid: 4fe14c49-3fd6-48b7-92de-a0c867b2e042
ms.date: 12/05/2018
ms.keywords: GetDiskFreeSpace, GetDiskFreeSpace function [Files], GetDiskFreeSpaceA, GetDiskFreeSpaceW, _win32_getdiskfreespace, base.getdiskfreespace, fileapi/GetDiskFreeSpace, fileapi/GetDiskFreeSpaceA, fileapi/GetDiskFreeSpaceW, fs.getdiskfreespace, winbase/GetDiskFreeSpace, winbase/GetDiskFreeSpaceA, winbase/GetDiskFreeSpaceW
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetDiskFreeSpaceW (Unicode) and GetDiskFreeSpaceA (ANSI)
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
 - GetDiskFreeSpaceW
 - fileapi/GetDiskFreeSpaceW
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
 - GetDiskFreeSpace
 - GetDiskFreeSpaceA
 - GetDiskFreeSpaceW
---

# GetDiskFreeSpaceW function


## -description

Retrieves information about the specified disk, including the amount of free space on the 
    disk.

## -parameters

### -param lpRootPathName [in]

The root directory of the disk for which information is to be returned. If this parameter is 
      <b>NULL</b>, the function uses the root of the current disk. If this parameter is a UNC name, 
      it must include a trailing backslash (for example, "\\\\MyServer\\MyShare\\"). Furthermore, a drive 
      specification must have a trailing backslash (for example, "C:\\"). The calling application must 
      have <b>FILE_LIST_DIRECTORY</b> access rights for this  directory.

### -param lpSectorsPerCluster [out]

A pointer to a variable that receives the number of sectors per cluster.

### -param lpBytesPerSector [out]

A pointer to a variable that receives the number of bytes per sector.

### -param lpNumberOfFreeClusters [out]

A pointer to a variable that receives the total number of free clusters on the disk that are available to the 
       user who is associated with the calling thread.

If per-user disk quotas are in use, this value may be less than the total number of free clusters on the 
       disk.

### -param lpTotalNumberOfClusters [out]

A pointer to a variable that receives the total number of clusters on the disk that are available to the user 
       who is associated with the calling thread.

If per-user disk quotas are in use, this value may be less than the total number of clusters on the disk.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <a href="/windows/desktop/api/fileapi/nf-fileapi-getdiskfreespaceexa">GetDiskFreeSpaceEx</a> function lets 
    you avoid some of the arithmetic that is required by the 
    <b>GetDiskFreeSpace</b> function.

Symbolic link behavior—If the path points to a symbolic link, the operation is performed 
    on the target.





> [!NOTE]
> The fileapi.h header defines GetDiskFreeSpace as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/FileIO/disk-management-functions">Disk Management Functions</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getdiskfreespaceexa">GetDiskFreeSpaceEx</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getdrivetypea">GetDriveType</a>
