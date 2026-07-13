---
UID: NF:setupapi.SetupAddToDiskSpaceListW
title: SetupAddToDiskSpaceListW function (setupapi.h)
description: The SetupAddToDiskSpaceList function adds a single delete or copy operation to a disk-space list. To add all the file operations in a section of an INF file, use either SetupAddSectionToDiskSpaceList, or SetupAddInstallSectionToDiskSpaceList. (Unicode)
helpviewer_keywords: ["FILEOP_COPY.", "FILEOP_DELETE", "SetupAddToDiskSpaceList", "SetupAddToDiskSpaceList function [Setup API]", "SetupAddToDiskSpaceListW", "_setupapi_setupaddtodiskspacelist", "setup.setupaddtodiskspacelist", "setupapi/SetupAddToDiskSpaceList", "setupapi/SetupAddToDiskSpaceListW"]
old-location: setup\setupaddtodiskspacelist.htm
tech.root: setup
ms.assetid: f1bb7096-b4a6-450b-9552-9a3dc4c71f24
ms.date: 12/05/2018
ms.keywords: FILEOP_COPY., FILEOP_DELETE, SetupAddToDiskSpaceList, SetupAddToDiskSpaceList function [Setup API], SetupAddToDiskSpaceListA, SetupAddToDiskSpaceListW, _setupapi_setupaddtodiskspacelist, setup.setupaddtodiskspacelist, setupapi/SetupAddToDiskSpaceList, setupapi/SetupAddToDiskSpaceListA, setupapi/SetupAddToDiskSpaceListW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupAddToDiskSpaceListW (Unicode) and SetupAddToDiskSpaceListA (ANSI)
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
 - SetupAddToDiskSpaceListW
 - setupapi/SetupAddToDiskSpaceListW
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
 - SetupAddToDiskSpaceList
 - SetupAddToDiskSpaceListA
 - SetupAddToDiskSpaceListW
---

# SetupAddToDiskSpaceListW function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupAddToDiskSpaceList</b> function adds a single delete or copy operation to a disk-space list. To add all the file operations in a section of an INF file, use either 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupaddsectiontodiskspacelista">SetupAddSectionToDiskSpaceList</a>, or 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista">SetupAddInstallSectionToDiskSpaceList</a>.

Target disk compression is ignored by this function. Files are assumed to occupy their full size on the target disk.

## -parameters

### -param DiskSpace [in]

Handle to the disk-space list.

### -param TargetFilespec [in]

File name of the file to be added to the disk-space list. You should use a null-terminated string that specifies  a fully qualified path. Otherwise, the path must be relative to the current directory.

### -param FileSize [in]

Uncompressed size of the file as it will exist in the target directory, in bytes. You can use 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetsourcefilesizea">SetupGetSourceFileSize</a> to retrieve this information from an INF file. This parameter is ignored for FILEOP_DELETE operations.

### -param Operation [in]

File operation to be added to the list. This parameter can be one of the following values. 



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
<td width="40%"><a id="FILEOP_COPY."></a><a id="fileop_copy."></a><dl>
<dt><b>FILEOP_COPY.</b></dt>
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

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>

## -remarks

> [!NOTE]
> The setupapi.h header defines SetupAddToDiskSpaceList as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
