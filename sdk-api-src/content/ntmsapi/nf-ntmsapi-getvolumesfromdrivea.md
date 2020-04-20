---
UID: NF:ntmsapi.GetVolumesFromDriveA
title: GetVolumesFromDriveA function (ntmsapi.h)
description: The GetVolumesFromDrive function retrieves the volume and drive letter for a given removable storage media drive.helpviewer_keywords: ["GetVolumesFromDrive","GetVolumesFromDrive function [Files]","GetVolumesFromDriveA","GetVolumesFromDriveW","base.getvolumesfromdrive","fs.getvolumesfromdrive","ntmsapi/GetVolumesFromDrive","ntmsapi/GetVolumesFromDriveA","ntmsapi/GetVolumesFromDriveW"]
old-location: fs\getvolumesfromdrive.htm
tech.root: Rsm
ms.assetid: 2509aed9-193e-402c-b0b7-fe94a8a6e0d6
ms.date: 12/05/2018
ms.keywords: GetVolumesFromDrive, GetVolumesFromDrive function [Files], GetVolumesFromDriveA, GetVolumesFromDriveW, base.getvolumesfromdrive, fs.getvolumesfromdrive, ntmsapi/GetVolumesFromDrive, ntmsapi/GetVolumesFromDriveA, ntmsapi/GetVolumesFromDriveW
f1_keywords:
- ntmsapi/GetVolumesFromDrive
dev_langs:
- c++
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
req.lib: Ntmsapi.lib
req.dll: Ntmsapi.dll
req.irql: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetVolumesFromDriveA function


## -description


<p class="CCE_Message">[<a href="https://docs.microsoft.com/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

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

If the function fails, the return value is one of the <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>.




## -remarks



This function assumes there will be only zero or one partitions on a 
    removable disk, so there is at most one drive letter and one volume name.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntmsapi/nf-ntmsapi-getntmsobjectinformation">GetNtmsObjectInformation</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Library Control Functions</a>
 

 

