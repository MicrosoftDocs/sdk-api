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

# GetVolumesFromDriveA function


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>GetVolumesFromDrive</b> function retrieves the volume and drive letter for a given removable storage media drive.


## -parameters




### -param pszDriveName [in]

The name of the removable storage media drive.


### -param VolumeNameBufferPtr [out]

The volume that represents the removable storage media drive.


### -param DriveLetterBufferPtr [out]

The drive letter that represents the removable storage media drive.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is one of the <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>.




## -remarks



This function assumes there will be only zero or one partitions on a 
    removable disk, so there is at most one drive letter and one volume name.




## -see-also




<a href="https://msdn.microsoft.com/e5c1b165-2c55-40c3-94d8-c996c5db4250">GetNtmsObjectInformation</a>



<a href="removable_storage_manager_functions.htm">Library Control Functions</a>
 

 

