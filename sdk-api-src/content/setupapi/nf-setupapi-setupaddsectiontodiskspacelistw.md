---
UID: NF:setupapi.SetupAddSectionToDiskSpaceListW
title: SetupAddSectionToDiskSpaceListW function (setupapi.h)
description: The SetupAddSectionToDiskSpaceList function adds to a disk-space list all the file delete or copy operations listed in a Copy Files or Delete Files section of an INF file. (Unicode)
helpviewer_keywords: ["FILEOP_COPY", "FILEOP_DELETE", "SetupAddSectionToDiskSpaceList", "SetupAddSectionToDiskSpaceList function [Setup API]", "SetupAddSectionToDiskSpaceListW", "_setupapi_setupaddsectiontodiskspacelist", "setup.setupaddsectiontodiskspacelist", "setupapi/SetupAddSectionToDiskSpaceList", "setupapi/SetupAddSectionToDiskSpaceListW"]
old-location: setup\setupaddsectiontodiskspacelist.htm
tech.root: setup
ms.assetid: 8225d0b4-b750-4580-83f5-dcffdf2ee67b
ms.date: 12/05/2018
ms.keywords: FILEOP_COPY, FILEOP_DELETE, SetupAddSectionToDiskSpaceList, SetupAddSectionToDiskSpaceList function [Setup API], SetupAddSectionToDiskSpaceListA, SetupAddSectionToDiskSpaceListW, _setupapi_setupaddsectiontodiskspacelist, setup.setupaddsectiontodiskspacelist, setupapi/SetupAddSectionToDiskSpaceList, setupapi/SetupAddSectionToDiskSpaceListA, setupapi/SetupAddSectionToDiskSpaceListW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupAddSectionToDiskSpaceListW (Unicode) and SetupAddSectionToDiskSpaceListA (ANSI)
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
 - SetupAddSectionToDiskSpaceListW
 - setupapi/SetupAddSectionToDiskSpaceListW
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
 - SetupAddSectionToDiskSpaceList
 - SetupAddSectionToDiskSpaceListA
 - SetupAddSectionToDiskSpaceListW
---

# SetupAddSectionToDiskSpaceListW function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupAddSectionToDiskSpaceList</b> function adds to a disk-space list all the file delete or copy operations listed in a <b>Copy Files</b> or <b>Delete Files</b> section of an INF file.

Target disk compression is ignored by this function. Files are assumed to occupy their full size on the target disk.

## -parameters

### -param DiskSpace [in]

Handle to the disk-space list.

### -param InfHandle [in]

Handle to an open INF file that contains the <b>SourceDisksFiles</b> section. If <i>ListInfHandle</i> is not specified, this INF file must also contain the section named by <i>SectionName</i>.

### -param ListInfHandle [in]

Optional handle to an open INF file that contains the section specified by <i>SectionName</i>. Otherwise, <i>InfHandle</i> is assumed to contain this section.

### -param SectionName [in]

Name of the <b>Copy Files</b> or <b>Delete Files</b> section that contains the file operations to add to the disk-space list. Use a null-terminated string.

### -param Operation [in]

Type of file operation to be added to the list. This parameter can be one of the following values. 



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

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function requires a Windows INF file. Some older INF file  formats may not be supported. 





> [!NOTE]
> The setupapi.h header defines SetupAddSectionToDiskSpaceList as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista">SetupAddInstallSectionToDiskSpaceList</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupaddtodiskspacelista">SetupAddToDiskSpaceList</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupremovesectionfromdiskspacelista">SetupRemoveSectionFromDiskSpaceList</a>
