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

# GetDiskFreeSpaceA function


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
 

 

