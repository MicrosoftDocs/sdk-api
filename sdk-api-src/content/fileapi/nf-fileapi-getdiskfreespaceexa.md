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
       "\\MyServer\MyShare\".

This parameter does not have to specify the root directory on a disk. The function accepts any directory on a 
       disk.

The calling application must have <b>FILE_LIST_DIRECTORY</b> access rights for this  
       directory.


### -param lpFreeBytesAvailableToCaller

TBD


### -param lpTotalNumberOfBytes [out, optional]

A pointer to a variable that receives the total number of bytes on a disk that are available to the user who 
       is associated with the calling thread.

This parameter can be <b>NULL</b>.

If per-user quotas are being used, this value may be less than the total number of bytes on a disk.

To determine the total number of bytes on a disk or volume, use 
       <a href="https://msdn.microsoft.com/library/windows/hardware/ff560370">IOCTL_DISK_GET_LENGTH_INFO</a>.


### -param lpTotalNumberOfFreeBytes [out, optional]

A pointer to a variable that receives the total number of free bytes on a disk.

This parameter can be <b>NULL</b>.


#### - lpFreeBytesAvailable [out, optional]

A pointer to a variable that receives the total number of free bytes on a disk that are available to the user 
       who is associated with the calling thread.

This parameter can be <b>NULL</b>.

If per-user quotas are being used, this value may be less than the total number of free bytes on a disk.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero (0). To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The values obtained by this function are of the type 
    <a href="https://msdn.microsoft.com/83a10c12-2cd1-449a-af3f-b2138fc50ee0">ULARGE_INTEGER</a>. Do not truncate these values to 32 
     bits.

The <b>GetDiskFreeSpaceEx</b> function returns zero (0) 
    for <i>lpTotalNumberOfFreeBytes</i> and <i>lpFreeBytesAvailable</i> for all 
    CD requests unless the disk is an unwritten CD in a CD-RW drive.

Symbolic link behavior—If the path points to a symbolic link, the operation is performed 
    on the target.




## -see-also




<a href="https://msdn.microsoft.com/301d3062-29a1-4b44-bbcd-e9d5b7d7823b">Disk Management Functions</a>



<a href="https://msdn.microsoft.com/4fe14c49-3fd6-48b7-92de-a0c867b2e042">GetDiskFreeSpace</a>



<a href="https://msdn.microsoft.com/29514410-89fe-4888-8b34-0c30d5af237f">GetModuleHandle</a>
 

 

