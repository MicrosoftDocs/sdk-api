---
UID: NF:setupapi.SetupSetDirectoryIdA
title: SetupSetDirectoryIdA function (setupapi.h)
description: The SetupSetDirectoryId function associates a directory identifier in an INF file with a specific directory. (ANSI)
helpviewer_keywords: ["SetupSetDirectoryIdA", "setupapi/SetupSetDirectoryIdA"]
old-location: setup\setupsetdirectoryid.htm
tech.root: setup
ms.assetid: bacb7b90-a391-4f05-bedb-0c0f52fd15f9
ms.date: 12/05/2018
ms.keywords: SetupSetDirectoryId, SetupSetDirectoryId function [Setup API], SetupSetDirectoryIdA, SetupSetDirectoryIdW, _setupapi_setupsetdirectoryid, setup.setupsetdirectoryid, setupapi/SetupSetDirectoryId, setupapi/SetupSetDirectoryIdA, setupapi/SetupSetDirectoryIdW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupSetDirectoryIdW (Unicode) and SetupSetDirectoryIdA (ANSI)
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
 - SetupSetDirectoryIdA
 - setupapi/SetupSetDirectoryIdA
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
 - SetupSetDirectoryId
 - SetupSetDirectoryIdA
 - SetupSetDirectoryIdW
---

# SetupSetDirectoryIdA function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupSetDirectoryId</b> function associates a directory identifier in an INF file with a specific directory.

## -parameters

### -param InfHandle [in]

A handle for a loaded INF file.

### -param Id [in]

A directory identifier (DIRID) to use for an association. This parameter can be <b>NULL</b>. This DIRID must be greater than or equal to DIRID_USER. If an association already exists for this DIRID, it is overwritten. If <i>Id</i> is <b>NULL</b>, the <i>Directory</i> parameter is ignored, and the current set of user-defined DIRIDs is deleted.

### -param Directory [in]

A pointer to  a <b>null</b>-terminated string that specifies the directory path to associate with <i>Id</i>. This parameter can be <b>NULL</b>. If <i>Directory</i> is <b>NULL</b>, any directory associated with <i>Id</i> is unassociated. No error results if <i>Id</i> is not currently associated with a directory.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is 0 (zero). To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>SetupSetDirectoryId</b> can be used prior to queuing file copy operations to specify a target location that is only known at runtime.

After setting the directory identifier, this function traverses all appended INF files, and if any of them have unresolved string substitutions, the function attempts to re-apply string substitution to them based on the new DIRID mapping. Because of this, some INF values may change after calling 
<b>SetupSetDirectoryId</b>.

DIRID_ABSOLUTE_16BIT is not a valid value for <i>Id</i>, which ensures compatibility with 16-bit setup.





> [!NOTE]
> The setupapi.h header defines SetupSetDirectoryId as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>
