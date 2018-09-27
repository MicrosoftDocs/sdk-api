---
UID: NF:fileapi.GetDiskFreeSpaceW
title: GetDiskFreeSpaceW function
author: windows-sdk-content
description: Retrieves information about the specified disk, including the amount of free space on the disk.
old-location: fs\getdiskfreespace.htm
tech.root: fileio
ms.assetid: 4fe14c49-3fd6-48b7-92de-a0c867b2e042
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetDiskFreeSpace, GetDiskFreeSpace function [Files], GetDiskFreeSpaceA, GetDiskFreeSpaceW, _win32_getdiskfreespace, base.getdiskfreespace, fileapi/GetDiskFreeSpace, fileapi/GetDiskFreeSpaceA, fileapi/GetDiskFreeSpaceW, fs.getdiskfreespace, winbase/GetDiskFreeSpace, winbase/GetDiskFreeSpaceA, winbase/GetDiskFreeSpaceW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetDiskFreeSpaceW function


## -description


Retrieves information about the specified disk, including the amount of free space on the 
    disk.


## -parameters




### -param lpRootPathName [in]

The root directory of the disk for which information is to be returned. If this parameter is 
      <b>NULL</b>, the function uses the root of the current disk. If this parameter is a UNC name, 
      it must include a trailing backslash (for example, "\\MyServer\MyShare\"). Furthermore, a drive 
      specification must have a trailing backslash (for example, "C:\"). The calling application must 
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
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <a href="https://msdn.microsoft.com/a52f2dbd-bda6-4217-9e72-f100f8bbe334">GetDiskFreeSpaceEx</a> function lets 
    you avoid some of the arithmetic that is required by the 
    <b>GetDiskFreeSpace</b> function.

Symbolic link behavior—If the path points to a symbolic link, the operation is performed 
    on the target.




## -see-also




<a href="https://msdn.microsoft.com/301d3062-29a1-4b44-bbcd-e9d5b7d7823b">Disk Management Functions</a>



<a href="https://msdn.microsoft.com/a52f2dbd-bda6-4217-9e72-f100f8bbe334">GetDiskFreeSpaceEx</a>



<a href="https://msdn.microsoft.com/b3989a3f-fc90-4ea0-8d3e-8e57068a08bc">GetDriveType</a>
 

 

