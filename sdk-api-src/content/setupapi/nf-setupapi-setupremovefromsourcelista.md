---
UID: NF:setupapi.SetupRemoveFromSourceListA
title: SetupRemoveFromSourceListA function (setupapi.h)
description: The SetupRemoveFromSourceList function removes a value from the list of installation sources for either the current user or the system. The system and user lists are merged at run time. (ANSI)
helpviewer_keywords: ["SetupRemoveFromSourceListA", "setupapi/SetupRemoveFromSourceListA"]
old-location: setup\setupremovefromsourcelist.htm
tech.root: setup
ms.assetid: 9e87f481-7d6a-4d8e-8f71-d104de3533f8
ms.date: 12/05/2018
ms.keywords: SetupRemoveFromSourceList, SetupRemoveFromSourceList function [Setup API], SetupRemoveFromSourceListA, SetupRemoveFromSourceListW, _setupapi_setupremovefromsourcelist, setup.setupremovefromsourcelist, setupapi/SetupRemoveFromSourceList, setupapi/SetupRemoveFromSourceListA, setupapi/SetupRemoveFromSourceListW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupRemoveFromSourceListW (Unicode) and SetupRemoveFromSourceListA (ANSI)
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
 - SetupRemoveFromSourceListA
 - setupapi/SetupRemoveFromSourceListA
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
 - SetupRemoveFromSourceList
 - SetupRemoveFromSourceListA
 - SetupRemoveFromSourceListW
---

# SetupRemoveFromSourceListA function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupRemoveFromSourceList</b> function removes a value from the list of installation sources for either the current user or the system. The system and user lists are merged at run time.

A caller of this function is required have administrative privileges, otherwise the function fails.

## -parameters

### -param Flags [in]

Specifies which source to remove from the list. This parameter can be any combination of the following values. 







#### SRCLIST_SYSTEM

Remove the source to the per-system list. The caller must be an administrator.



#### SRCLIST_USER

Remove the source to the per-user list.



#### SRCLIST_SYSIFADMIN

If the caller is an administrator, the source is removed from the per-system list; if the caller is not an administrator, the source is removed from the per-user list for the current user.

<div class="alert"><b>Note</b>  If a temporary list is currently in use (see 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupsetsourcelista">SetupSetSourceList</a>), the preceding flags are ignored and the source is removed from the temporary list.</div>
<div> </div>




#### SRCLIST_SUBDIRS

Remove all subdirectories of the source.

### -param Source [in]

Pointer to a null-terminated string that specifies the source to remove from the list.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupaddtosourcelista">SetupAddToSourceList</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupsetsourcelista">SetupSetSourceList</a>

## -remarks

> [!NOTE]
> The setupapi.h header defines SetupRemoveFromSourceList as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
