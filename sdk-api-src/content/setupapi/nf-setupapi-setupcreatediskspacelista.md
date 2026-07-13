---
UID: NF:setupapi.SetupCreateDiskSpaceListA
title: SetupCreateDiskSpaceListA function (setupapi.h)
description: The SetupCreateDiskSpaceList function creates a disk-space list. (ANSI)
helpviewer_keywords: ["SetupCreateDiskSpaceListA", "setupapi/SetupCreateDiskSpaceListA"]
old-location: setup\setupcreatediskspacelist.htm
tech.root: setup
ms.assetid: a578ed9d-12b2-43f4-ab0a-183269de0d40
ms.date: 12/05/2018
ms.keywords: SetupCreateDiskSpaceList, SetupCreateDiskSpaceList function [Setup API], SetupCreateDiskSpaceListA, SetupCreateDiskSpaceListW, _setupapi_setupcreatediskspacelist, setup.setupcreatediskspacelist, setupapi/SetupCreateDiskSpaceList, setupapi/SetupCreateDiskSpaceListA, setupapi/SetupCreateDiskSpaceListW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupCreateDiskSpaceListW (Unicode) and SetupCreateDiskSpaceListA (ANSI)
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
 - SetupCreateDiskSpaceListA
 - setupapi/SetupCreateDiskSpaceListA
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
 - SetupCreateDiskSpaceList
 - SetupCreateDiskSpaceListA
 - SetupCreateDiskSpaceListW
---

# SetupCreateDiskSpaceListA function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupCreateDiskSpaceList</b> function creates a disk-space list.

## -parameters

### -param Reserved1 [in]

Unused, must be zero.

### -param Reserved2 [in]

Unused, must be zero.

### -param Flags [in]

This parameter can be the following value. 







#### SPDSL_IGNORE_DISK

File operations added to the list will ignore files that already exist on the disk. For example, if the disk contains a 5000-byte file, C:\MyDir\MyFile, and you add a Copy operation to the disk-space list for a new version, C:\MyDir\MyFile, that is 6500 bytes, the space required will be 6500 bytes (instead of 1500 bytes, which is the value returned if you do not set SPDSL_IGNORE_DISK).

## -returns

If the function succeeds, it returns a handle to the disk-space list.

If the function fails, it returns null. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdestroydiskspacelist">SetupDestroyDiskSpaceList</a>

## -remarks

> [!NOTE]
> The setupapi.h header defines SetupCreateDiskSpaceList as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
