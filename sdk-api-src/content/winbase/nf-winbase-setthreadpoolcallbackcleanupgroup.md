---
UID: NF:winbase.SetThreadpoolCallbackCleanupGroup
title: SetThreadpoolCallbackCleanupGroup function (winbase.h)
description: Associates the specified cleanup group with the specified callback environment. (SetThreadpoolCallbackCleanupGroup)
helpviewer_keywords: ["SetThreadpoolCallbackCleanupGroup","SetThreadpoolCallbackCleanupGroup function","base.setthreadpoolcallbackcleanupgroup","winbase/SetThreadpoolCallbackCleanupGroup"]
old-location: base\setthreadpoolcallbackcleanupgroup.htm
tech.root: backup
ms.assetid: 395db7ba-ff39-46ee-917b-2896a0e99d43
ms.date: 12/05/2018
ms.keywords: SetThreadpoolCallbackCleanupGroup, SetThreadpoolCallbackCleanupGroup function, base.setthreadpoolcallbackcleanupgroup, winbase/SetThreadpoolCallbackCleanupGroup
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetThreadpoolCallbackCleanupGroup
 - winbase/SetThreadpoolCallbackCleanupGroup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - SetThreadpoolCallbackCleanupGroup
---

# SetThreadpoolCallbackCleanupGroup function


## -description

Associates the specified cleanup group with the specified callback environment.

## -parameters

### -param pcbe [in, out]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines the callback environment. The <a href="/windows/desktop/api/winbase/nf-winbase-initializethreadpoolenvironment">InitializeThreadpoolEnvironment</a> function returns this structure.

### -param ptpcg [in]

A <b>TP_CLEANUP_GROUP</b> structure that defines the cleanup group. The <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolcleanupgroup">CreateThreadpoolCleanupGroup</a> function returns this structure.

### -param pfng [in, optional]

The cleanup callback to be called if the cleanup group is canceled before the associated object is released. The function is called when you call <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolcleanupgroupmembers">CloseThreadpoolCleanupGroupMembers</a>.

## -remarks

This function is implemented as an inline function.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="/windows/desktop/ProcThread/using-the-thread-pool-functions">Using the Thread Pool Functions</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-destroythreadpoolenvironment">DestroyThreadpoolEnvironment</a>



<a href="/windows/desktop/api/winbase/nf-winbase-initializethreadpoolenvironment">InitializeThreadpoolEnvironment</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbacklibrary">SetThreadpoolCallbackLibrary</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbackpool">SetThreadpoolCallbackPool</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbackpriority">SetThreadpoolCallbackPriority</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbackrunslong">SetThreadpoolCallbackRunsLong</a>



<a href="/windows/desktop/ProcThread/thread-pools">Thread Pools</a>
