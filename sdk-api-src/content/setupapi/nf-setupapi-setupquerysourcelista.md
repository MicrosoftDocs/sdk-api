---
UID: NF:setupapi.SetupQuerySourceListA
title: SetupQuerySourceListA function (setupapi.h)
author: windows-sdk-content
description: The SetupQuerySourceList function queries the current list of installation sources. The list is built from the system and user-specific lists, and potentially overridden by a temporary list (see SetupSetSourceList).
old-location: setup\setupquerysourcelist.htm
tech.root: SetupApi
ms.assetid: 8d1de1d5-5b82-45ae-b29c-4f9a93d28c6e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetupQuerySourceList, SetupQuerySourceList function [Setup API], SetupQuerySourceListA, SetupQuerySourceListW, _setupapi_setupquerysourcelist, setup.setupquerysourcelist, setupapi/SetupQuerySourceList, setupapi/SetupQuerySourceListA, setupapi/SetupQuerySourceListW
ms.topic: function
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupQuerySourceListW (Unicode) and SetupQuerySourceListA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
api_name:
 - SetupQuerySourceList
 - SetupQuerySourceListA
 - SetupQuerySourceListW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetupQuerySourceListA function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupQuerySourceList</b> function queries the current list of installation sources. The list is built from the system and user-specific lists, and potentially overridden by a temporary list (see 
<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupsetsourcelista">SetupSetSourceList</a>).


## -parameters




### -param Flags [in]

Specifies which list to query. This parameter can be any combination of the following values. 







#### SRCLIST_SYSTEM

Query the system list.



#### SRCLIST_USER

Query the per-user list.

<div class="alert"><b>Note</b>  If the system and the user lists are both retrieved, they are merged with those items in the system list that appear first.</div>
<div> </div>
<div class="alert"><b>Note</b>  If none of the preceding flags are specified, the entire current (merged) list is returned.</div>
<div> </div>




#### SRCLIST_NOSTRIPPLATFORM

Normally, all paths are stripped of a platform-specific component if it is the final component. For example, a path stored in the registry as f:\x86 is returned as f:\. If this flag is specified, the platform-specific component is not stripped.


### -param List [in, out]

Pointer to a variable in which this function returns a pointer to an array of sources. Use a null-terminated string. The caller must free this array with a call to 
<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupfreesourcelista">SetupFreeSourceList</a>.


### -param Count [in, out]

Pointer to a variable in which this function returns the number of sources in the list.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SetupApi/functions">Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/SetupApi/overview">Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupsetsourcelista">SetupSetSourceList</a>
 

 

