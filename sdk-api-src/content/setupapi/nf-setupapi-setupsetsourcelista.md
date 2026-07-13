---
UID: NF:setupapi.SetupSetSourceListA
title: SetupSetSourceListA function (setupapi.h)
description: The SetupSetSourceList function allows the caller to set the list of installation sources for either the current user or the system (common to all users). (ANSI)
helpviewer_keywords: ["SetupSetSourceListA", "setupapi/SetupSetSourceListA"]
old-location: setup\setupsetsourcelist.htm
tech.root: setup
ms.assetid: 6a37a56c-ae44-4a57-9307-90efcf025d1a
ms.date: 12/05/2018
ms.keywords: SetupSetSourceList, SetupSetSourceList function [Setup API], SetupSetSourceListA, SetupSetSourceListW, _setupapi_setupsetsourcelist, setup.setupsetsourcelist, setupapi/SetupSetSourceList, setupapi/SetupSetSourceListA, setupapi/SetupSetSourceListW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupSetSourceListW (Unicode) and SetupSetSourceListA (ANSI)
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
 - SetupSetSourceListA
 - setupapi/SetupSetSourceListA
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
 - SetupSetSourceList
 - SetupSetSourceListA
 - SetupSetSourceListW
---

# SetupSetSourceListA function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupSetSourceList</b> function allows the caller to set the list of installation sources for either the current user or the system (common to all users).

## -parameters

### -param Flags [in]

Specifies the type of list. This parameter can be a combination of the following values. 







#### SRCLIST_SYSTEM

The list is the per-system Most Recently Used (MRU) list stored in the registry. The caller must be a member of the administrators local group.



#### SRCLIST_USER

The list is the per-user MRU list stored in the registry.



#### SRCLIST_TEMPORARY

The specified list is temporary and will be the only list accessible to the current process until 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupcanceltemporarysourcelist">SetupCancelTemporarySourceList</a> is called or <b>SetSourceList</b> is called again.

<div class="alert"><b>Important</b>  If a temporary list is set, sources are not added to or deleted from the system or user lists, even if subsequent calls to 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupaddtosourcelista">SetupAddToSourceList</a> or 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupremovefromsourcelista">SetupRemoveFromSourceList</a> explicitly specify those lists.</div>
<div> </div>
<div class="alert"><b>Note</b>  One of the SRCLIST_SYSTEM, SRCLIST_USER, or SRCLIST_TEMPORARY flags must be specified.</div>
<div> </div>




#### SRCLIST_NOBROWSE

The user is not allowed to add or change sources when 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setuppromptfordiska">SetupPromptForDisk</a> is used. This flag is typically used in combination with the SRCLIST_TEMPORARY flag.

### -param SourceList [in]

Pointer to an array of strings to use as the source list, as specified by the <i>Flags</i> parameter.

### -param SourceCount [in]

Number of elements in the array pointed to by <i>SourceList</i>.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupaddtosourcelista">SetupAddToSourceList</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupcanceltemporarysourcelist">SetupCancelTemporarySourceList</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupremovefromsourcelista">SetupRemoveFromSourceList</a>

## -remarks

> [!NOTE]
> The setupapi.h header defines SetupSetSourceList as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
