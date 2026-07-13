---
UID: NF:ntmsapi.GetVolumesFromDriveW
title: GetVolumesFromDriveW function (ntmsapi.h)
description: The GetVolumesFromDrive function retrieves the volume and drive letter for a given removable storage media drive. (Unicode)
helpviewer_keywords: ["GetVolumesFromDrive", "GetVolumesFromDrive function [Files]", "GetVolumesFromDriveW", "base.getvolumesfromdrive", "fs.getvolumesfromdrive", "ntmsapi/GetVolumesFromDrive", "ntmsapi/GetVolumesFromDriveW"]
old-location: fs\getvolumesfromdrive.htm
tech.root: fs
ms.assetid: 2509aed9-193e-402c-b0b7-fe94a8a6e0d6
ms.date: 12/05/2018
ms.keywords: GetVolumesFromDrive, GetVolumesFromDrive function [Files], GetVolumesFromDriveA, GetVolumesFromDriveW, base.getvolumesfromdrive, fs.getvolumesfromdrive, ntmsapi/GetVolumesFromDrive, ntmsapi/GetVolumesFromDriveA, ntmsapi/GetVolumesFromDriveW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetVolumesFromDriveW
 - ntmsapi/GetVolumesFromDriveW
dev_langs:
 - c++
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
---

# GetVolumesFromDriveW function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

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

If the function fails, the return value is one of the <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>.

## -remarks

This function assumes there will be only zero or one partitions on a 
    removable disk, so there is at most one drive letter and one volume name.





> [!NOTE]
> The ntmsapi.h header defines GetVolumesFromDrive as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-getntmsobjectinformation">GetNtmsObjectInformation</a>



<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Library Control Functions</a>
