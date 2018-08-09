---
UID: NF:ntmsapi.GetVolumesFromDriveW
title: GetVolumesFromDriveW function
author: windows-sdk-content
description: The GetVolumesFromDrive function retrieves the volume and drive letter for a given removable storage media drive.
old-location: fs\getvolumesfromdrive.htm
old-project: Rsm
ms.assetid: 2509aed9-193e-402c-b0b7-fe94a8a6e0d6
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: GetVolumesFromDrive, GetVolumesFromDrive function [Files], GetVolumesFromDriveA, GetVolumesFromDriveW, base.getvolumesfromdrive, fs.getvolumesfromdrive, ntmsapi/GetVolumesFromDrive, ntmsapi/GetVolumesFromDriveA, ntmsapi/GetVolumesFromDriveW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ntmsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetVolumesFromDriveW (Unicode) and GetVolumesFromDriveA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntmsapi.dll
api_name:
 - GetVolumesFromDrive
 - GetVolumesFromDriveA
 - GetVolumesFromDriveW
product: Windows
targetos: Windows
req.lib: Ntmsapi.lib
req.dll: Ntmsapi.dll
req.irql: 
req.product: ADAM
---

# GetVolumesFromDriveW function


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
 

 

