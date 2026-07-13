---
UID: NF:setupapi.SetupQuerySpaceRequiredOnDriveW
title: SetupQuerySpaceRequiredOnDriveW function (setupapi.h)
description: The SetupQuerySpaceRequiredOnDrive function examines a disk space list to determine the space that is required to perform all the file operations listed for a specific drive. (Unicode)
helpviewer_keywords: ["SetupQuerySpaceRequiredOnDrive", "SetupQuerySpaceRequiredOnDrive function [Setup API]", "SetupQuerySpaceRequiredOnDriveW", "_setupapi_setupqueryspacerequiredondrive", "setup.setupqueryspacerequiredondrive", "setupapi/SetupQuerySpaceRequiredOnDrive", "setupapi/SetupQuerySpaceRequiredOnDriveW"]
old-location: setup\setupqueryspacerequiredondrive.htm
tech.root: setup
ms.assetid: 529e04e2-671a-4aad-bb1c-2b24cf2e5cd1
ms.date: 12/05/2018
ms.keywords: SetupQuerySpaceRequiredOnDrive, SetupQuerySpaceRequiredOnDrive function [Setup API], SetupQuerySpaceRequiredOnDriveA, SetupQuerySpaceRequiredOnDriveW, _setupapi_setupqueryspacerequiredondrive, setup.setupqueryspacerequiredondrive, setupapi/SetupQuerySpaceRequiredOnDrive, setupapi/SetupQuerySpaceRequiredOnDriveA, setupapi/SetupQuerySpaceRequiredOnDriveW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupQuerySpaceRequiredOnDriveW (Unicode) and SetupQuerySpaceRequiredOnDriveA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupQuerySpaceRequiredOnDriveW
 - setupapi/SetupQuerySpaceRequiredOnDriveW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
api_name:
 - SetupQuerySpaceRequiredOnDrive
 - SetupQuerySpaceRequiredOnDriveA
 - SetupQuerySpaceRequiredOnDriveW
---

# SetupQuerySpaceRequiredOnDriveW function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupQuerySpaceRequiredOnDrive</b> function examines a disk space list to determine the space that is required to perform all the file operations listed for a specific drive.

## -parameters

### -param DiskSpace [in]

The handle to a disk space list.

### -param DriveSpec [in]

A pointer to a null-terminated string that specifies the drive where space information is to be returned. 

This should be in the form "x:" or "\\server\share".

### -param SpaceRequired [out]

If the function succeeds, this parameter receives the amount of additional space that is required to process all the file operations listed in the disk space list for the drive that <i>DriveSpec</i> specifies. 




The 
<b>SetupQuerySpaceRequiredOnDrive</b> function calculates the additional space required on the target drive by checking for preexisting versions of the files on the target drive.

For example, if a file operation copies a 2000-byte file, FIRST.EXE, to the directory, C:\MYPROG\, the 
<b>SetupQuerySpaceRequiredOnDrive</b> function automatically checks for a preexisting version of that file in that directory. If a preexisting version of C:\MYPROG\FIRST.EXE has a file size of 500 bytes, the additional space required on the drive C for that operation is 1500 bytes.

The value received can be 0 (zero) or a negative number, if additional space is not required, or if space is freed on the target drive.

If FIRST.EXE in the preceding example is being deleted from the drive C, the amount of space required is 2000 bytes, or the space freed on drive C.

If the preexisting version has a file size of 5000 bytes, then the disk space required to replace it with the 2000-byte FIRST.EXE is 3000 bytes.

File sizes are rounded to disk cluster boundaries.

### -param Reserved1 [in]

Reserved; must be 0 (zero).

### -param Reserved2 [in]

Reserved; must be 0 (zero).

## -returns

If the function succeeds, the return value is a nonzero value and <i>SpaceRequired</i> receives the amount of space required by the file operations listed in the current disk space list.

If the function fails, the return value is 0 (zero). To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DRIVE</b></dt>
</dl>
</td>
<td width="60%">
The specified drive is not on the disk-space list.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The specified <i>DiskSpace</i> handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The specified <i>DriveSpec</i> string is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupquerydrivesindiskspacelista">SetupQueryDrivesInDiskSpaceList</a>

## -remarks

> [!NOTE]
> The setupapi.h header defines SetupQuerySpaceRequiredOnDrive as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
