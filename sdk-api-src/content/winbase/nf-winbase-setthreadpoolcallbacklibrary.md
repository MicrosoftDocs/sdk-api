---
UID: NF:winbase.SetThreadpoolCallbackLibrary
title: SetThreadpoolCallbackLibrary function (winbase.h)
description: Ensures that the specified DLL remains loaded as long as there are outstanding callbacks. (SetThreadpoolCallbackLibrary)
helpviewer_keywords: ["SetThreadpoolCallbackLibrary","SetThreadpoolCallbackLibrary function","base.setthreadpoolcallbacklibrary","winbase/SetThreadpoolCallbackLibrary"]
old-location: base\setthreadpoolcallbacklibrary.htm
tech.root: backup
ms.assetid: 41d5d8c5-4938-4274-bcfa-b122bbc70530
ms.date: 12/05/2018
ms.keywords: SetThreadpoolCallbackLibrary, SetThreadpoolCallbackLibrary function, base.setthreadpoolcallbacklibrary, winbase/SetThreadpoolCallbackLibrary
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
 - SetThreadpoolCallbackLibrary
 - winbase/SetThreadpoolCallbackLibrary
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
 - SetThreadpoolCallbackLibrary
---

# SetThreadpoolCallbackLibrary function


## -description

Ensures that the specified DLL remains loaded as long as there are outstanding callbacks.

## -parameters

### -param pcbe [in, out]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines the callback environment. The <a href="/windows/desktop/api/winbase/nf-winbase-initializethreadpoolenvironment">InitializeThreadpoolEnvironment</a> function returns this structure.

### -param mod [in]

A handle to the DLL.

## -remarks

You should call this function if a callback might acquire the loader lock. This prevents a deadlock from occurring when one thread in DllMain is waiting for the callback to end, and another thread that is executing the callback attempts to acquire the loader lock.

If the DLL containing the callback might be unloaded, the cleanup code in DllMain must cancel outstanding callbacks before releasing the object.

Managing callbacks created with a TP_CALLBACK_ENVIRON that specifies a callback library is somewhat processing-intensive.  You should consider other options for ensuring that the library is not unloaded while callbacks are executing, or to guarantee that callbacks which may be executing do not acquire the loader lock.

The thread pool assumes ownership of the library reference supplied to this function.  The caller should not call <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary">FreeLibrary</a> on a module handle after passing it to this function.

This function is implemented as an inline function.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-destroythreadpoolenvironment">DestroyThreadpoolEnvironment</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-freelibrarywhencallbackreturns">FreeLibraryWhenCallbackReturns</a>



<a href="/windows/desktop/api/winbase/nf-winbase-initializethreadpoolenvironment">InitializeThreadpoolEnvironment</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbackcleanupgroup">SetThreadpoolCallbackCleanupGroup</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbackpool">SetThreadpoolCallbackPool</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbackpriority">SetThreadpoolCallbackPriority</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbackrunslong">SetThreadpoolCallbackRunsLong</a>



<a href="/windows/desktop/ProcThread/thread-pools">Thread Pools</a>
