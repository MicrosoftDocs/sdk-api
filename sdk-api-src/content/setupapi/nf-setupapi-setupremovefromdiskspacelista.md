---
UID: NF:setupapi.SetupRemoveFromDiskSpaceListA
title: SetupRemoveFromDiskSpaceListA function (setupapi.h)
description: The SetupRemoveFromDiskSpaceList function removes a file delete or copy operation from a disk-space list. (ANSI)
helpviewer_keywords: ["FILEOP_COPY", "FILEOP_DELETE", "SetupRemoveFromDiskSpaceListA", "setupapi/SetupRemoveFromDiskSpaceListA"]
old-location: setup\setupremovefromdiskspacelist.htm
tech.root: setup
ms.assetid: 0d23c8ce-ada6-4640-b9ad-8989f9a122a2
ms.date: 12/05/2018
ms.keywords: FILEOP_COPY, FILEOP_DELETE, SetupRemoveFromDiskSpaceList, SetupRemoveFromDiskSpaceList function [Setup API], SetupRemoveFromDiskSpaceListA, SetupRemoveFromDiskSpaceListW, _setupapi_setupremovefromdiskspacelist, setup.setupremovefromdiskspacelist, setupapi/SetupRemoveFromDiskSpaceList, setupapi/SetupRemoveFromDiskSpaceListA, setupapi/SetupRemoveFromDiskSpaceListW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupRemoveFromDiskSpaceListW (Unicode) and SetupRemoveFromDiskSpaceListA (ANSI)
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
 - SetupRemoveFromDiskSpaceListA
 - setupapi/SetupRemoveFromDiskSpaceListA
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
 - SetupRemoveFromDiskSpaceList
 - SetupRemoveFromDiskSpaceListA
 - SetupRemoveFromDiskSpaceListW
---

# SetupRemoveFromDiskSpaceListA function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupRemoveFromDiskSpaceList</b> function removes a file delete or copy operation from a disk-space list.

## -parameters

### -param DiskSpace [in]

Handle to a disk-space list.

### -param TargetFilespec [in]

Pointer to a null-terminated string that specifies the file name of the file to remove from the disk-space list. This is typically a fully qualified  path. Otherwise, the path must be relative to the current directory.

### -param Operation [in]

File operation to be removed from the list. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILEOP_DELETE"></a><a id="fileop_delete"></a><dl>
<dt><b>FILEOP_DELETE</b></dt>
</dl>
</td>
<td width="60%">
A file delete operation.

</td>
</tr>
<tr>
<td width="40%"><a id="FILEOP_COPY"></a><a id="fileop_copy"></a><dl>
<dt><b>FILEOP_COPY</b></dt>
</dl>
</td>
<td width="60%">
A file copy operation.

</td>
</tr>
</table>

### -param Reserved1 [in]

Must be zero.

### -param Reserved2 [in]

Must be zero.

## -returns

If the file was not in the list, the 
<b>SetupRemoveFromDiskSpaceList</b> function returns a nonzero value and 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_INVALID_DRIVE or ERROR_INVALID_NAME. If the file was in the list then upon success the routine returns a nonzero value and 
<b>GetLastError</b> returns NO_ERROR.

If the routine fails for some other reason, it returns zero and 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns extended error information.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupaddtodiskspacelista">SetupAddToDiskSpaceList</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupremoveinstallsectionfromdiskspacelista">SetupRemoveInstallSectionFromDiskSpaceList</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupremovesectionfromdiskspacelista">SetupRemoveSectionFromDiskSpaceList</a>

## -remarks

> [!NOTE]
> The setupapi.h header defines SetupRemoveFromDiskSpaceList as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
