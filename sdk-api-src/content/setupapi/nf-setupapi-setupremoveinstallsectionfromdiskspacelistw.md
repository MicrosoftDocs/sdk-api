---
UID: NF:setupapi.SetupRemoveInstallSectionFromDiskSpaceListW
title: SetupRemoveInstallSectionFromDiskSpaceListW function (setupapi.h)
description: The SetupRemoveInstallSectionFromDiskSpaceList function searches an Install section of an INF file for CopyFiles and DelFiles lines, and removes the file operations specified in those sections from a disk-space list. (Unicode)
helpviewer_keywords: ["SetupRemoveInstallSectionFromDiskSpaceList", "SetupRemoveInstallSectionFromDiskSpaceList function [Setup API]", "SetupRemoveInstallSectionFromDiskSpaceListW", "_setupapi_setupremoveinstallsectionfromdiskspacelist", "setup.setupremoveinstallsectionfromdiskspacelist", "setupapi/SetupRemoveInstallSectionFromDiskSpaceList", "setupapi/SetupRemoveInstallSectionFromDiskSpaceListW"]
old-location: setup\setupremoveinstallsectionfromdiskspacelist.htm
tech.root: setup
ms.assetid: dd104c59-faee-4eb6-abbc-a4c13d766298
ms.date: 12/05/2018
ms.keywords: SetupRemoveInstallSectionFromDiskSpaceList, SetupRemoveInstallSectionFromDiskSpaceList function [Setup API], SetupRemoveInstallSectionFromDiskSpaceListA, SetupRemoveInstallSectionFromDiskSpaceListW, _setupapi_setupremoveinstallsectionfromdiskspacelist, setup.setupremoveinstallsectionfromdiskspacelist, setupapi/SetupRemoveInstallSectionFromDiskSpaceList, setupapi/SetupRemoveInstallSectionFromDiskSpaceListA, setupapi/SetupRemoveInstallSectionFromDiskSpaceListW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupRemoveInstallSectionFromDiskSpaceListW (Unicode) and SetupRemoveInstallSectionFromDiskSpaceListA (ANSI)
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
 - SetupRemoveInstallSectionFromDiskSpaceListW
 - setupapi/SetupRemoveInstallSectionFromDiskSpaceListW
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
 - SetupRemoveInstallSectionFromDiskSpaceList
 - SetupRemoveInstallSectionFromDiskSpaceListA
 - SetupRemoveInstallSectionFromDiskSpaceListW
---

# SetupRemoveInstallSectionFromDiskSpaceListW function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupRemoveInstallSectionFromDiskSpaceList</b> function searches an <b>Install</b> section of an INF file for <b>CopyFiles</b> and <b>DelFiles</b> lines, and removes the file operations specified in those sections from a disk-space list.

## -parameters

### -param DiskSpace [in]

Handle to a disk-space list.

### -param InfHandle [in]

Handle to an open INF file that contains the <b>Install</b> section. If <i>LayoutInfHandle</i> is not specified, the INF file must also contain the section specified by <i>SectionName</i>.

### -param LayoutInfHandle [in]

Optional handle to the INF file that contains the <b>SourceDisksFiles</b> sections. Otherwise, that section is assumed to exist in the INF file specified by <i>InfHandle</i>.

### -param SectionName [in]

Pointer to a null-terminated string that specifies the name of the section to be added to the disk-space list.

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
> The setupapi.h header defines SetupRemoveInstallSectionFromDiskSpaceList as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista">SetupAddInstallSectionToDiskSpaceList</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupremovefromdiskspacelista">SetupRemoveFromDiskSpaceList</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupremovesectionfromdiskspacelista">SetupRemoveSectionFromDiskSpaceList</a>
