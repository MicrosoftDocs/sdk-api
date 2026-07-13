---
UID: NF:setupapi.SetupDuplicateDiskSpaceListA
title: SetupDuplicateDiskSpaceListA function (setupapi.h)
description: The SetupDuplicateDiskSpaceList function duplicates a disk-space list as a new independent disk-space list. (ANSI)
helpviewer_keywords: ["SetupDuplicateDiskSpaceListA", "setupapi/SetupDuplicateDiskSpaceListA"]
old-location: setup\setupduplicatediskspacelist.htm
tech.root: setup
ms.assetid: 92d18c15-e8e2-4e89-8d2f-7c87c948603f
ms.date: 12/05/2018
ms.keywords: SetupDuplicateDiskSpaceList, SetupDuplicateDiskSpaceList function [Setup API], SetupDuplicateDiskSpaceListA, SetupDuplicateDiskSpaceListW, setup.setupduplicatediskspacelist, setupapi/SetupDuplicateDiskSpaceList, setupapi/SetupDuplicateDiskSpaceListA, setupapi/SetupDuplicateDiskSpaceListW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupDuplicateDiskSpaceListW (Unicode) and SetupDuplicateDiskSpaceListA (ANSI)
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
 - SetupDuplicateDiskSpaceListA
 - setupapi/SetupDuplicateDiskSpaceListA
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
 - SetupDuplicateDiskSpaceList
 - SetupDuplicateDiskSpaceListA
 - SetupDuplicateDiskSpaceListW
---

# SetupDuplicateDiskSpaceListA function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The SetupDuplicateDiskSpaceList function duplicates a disk-space list as a new independent disk-space list.

## -parameters

### -param DiskSpace [in]

Handle to the disk-space list to be duplicated.

### -param Reserved1

Unused, must be  zero.

### -param Reserved2

Unused, must be  zero.

### -param Flags

Unused, must be  zero.

## -returns

If the function succeeds, it returns a handle to the new disk-space list.

If the function fails, it returns null. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>

## -remarks

> [!NOTE]
> The setupapi.h header defines SetupDuplicateDiskSpaceList as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
