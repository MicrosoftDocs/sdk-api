---
UID: NF:setupapi.SetupAddToSourceListW
title: SetupAddToSourceListW function (setupapi.h)
description: The SetupAddToSourceList function appends a value to the list of installation sources for either the current user or the system. If the value already exists, it is removed first, so that duplicate entries are not created. (Unicode)
helpviewer_keywords: ["SetupAddToSourceList", "SetupAddToSourceList function [Setup API]", "SetupAddToSourceListW", "_setupapi_setupaddtosourcelist", "setup.setupaddtosourcelist", "setupapi/SetupAddToSourceList", "setupapi/SetupAddToSourceListW"]
old-location: setup\setupaddtosourcelist.htm
tech.root: setup
ms.assetid: c1da3f9b-12ea-49f3-a5ca-45a63a56becd
ms.date: 12/05/2018
ms.keywords: SetupAddToSourceList, SetupAddToSourceList function [Setup API], SetupAddToSourceListA, SetupAddToSourceListW, _setupapi_setupaddtosourcelist, setup.setupaddtosourcelist, setupapi/SetupAddToSourceList, setupapi/SetupAddToSourceListA, setupapi/SetupAddToSourceListW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupAddToSourceListW (Unicode) and SetupAddToSourceListA (ANSI)
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
 - SetupAddToSourceListW
 - setupapi/SetupAddToSourceListW
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
 - SetupAddToSourceList
 - SetupAddToSourceListA
 - SetupAddToSourceListW
---

# SetupAddToSourceListW function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupAddToSourceList</b> function appends a value to the list of installation sources for either the current user or the system. If the value already exists, it is removed first, so that duplicate entries are not created.

A caller of this function is required have administrative privileges, otherwise the function fails.

## -parameters

### -param Flags [in]

List to which the source will be appended. This parameter can be any combination of the following values. 







#### SRCLIST_SYSTEM

Add the source to the per-system list. The caller must be an administrator.



#### SRCLIST_USER

Add the source to the per-user list.



#### SRCLIST_SYSIFADMIN

If the caller is an administrator, the source is added to the per-system list; if the caller is not a member of the administrators local group, the source is added to the per-user list for the current user.

<div class="alert"><b>Note</b>  If a temporary list is currently in use (see 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupsetsourcelista">SetupSetSourceList</a>), the preceding flags are ignored and the source is added to the temporary list.</div>
<div> </div>




#### SRCLIST_APPEND

Add the source to the end of the list. If this flag is not specified, the source is added to the beginning of the list.

### -param Source [in]

Pointer to the source to be added to the list. You should use a null-terminated string. 


##### - Flags.SRCLIST_APPEND

Add the source to the end of the list. If this flag is not specified, the source is added to the beginning of the list.


##### - Flags.SRCLIST_SYSIFADMIN

If the caller is an administrator, the source is added to the per-system list; if the caller is not a member of the administrators local group, the source is added to the per-user list for the current user.


##### - Flags.SRCLIST_SYSTEM

Add the source to the per-system list. The caller must be an administrator.


##### - Flags.SRCLIST_USER

Add the source to the per-user list.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupremovefromsourcelista">SetupRemoveFromSourceList</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupsetsourcelista">SetupSetSourceList</a>

## -remarks

> [!NOTE]
> The setupapi.h header defines SetupAddToSourceList as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
