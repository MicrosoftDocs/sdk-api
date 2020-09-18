---
UID: NF:winbase.InitializeThreadpoolEnvironment
title: InitializeThreadpoolEnvironment function (winbase.h)
description: Initializes a callback environment.
helpviewer_keywords: ["InitializeThreadpoolEnvironment","InitializeThreadpoolEnvironment function","base.initializethreadpoolenvironment","winbase/InitializeThreadpoolEnvironment"]
old-location: base\initializethreadpoolenvironment.htm
tech.root: backup
ms.assetid: ad610b7a-9865-4feb-81d2-491f9f87ef3e
ms.date: 12/05/2018
ms.keywords: InitializeThreadpoolEnvironment, InitializeThreadpoolEnvironment function, base.initializethreadpoolenvironment, winbase/InitializeThreadpoolEnvironment
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
 - InitializeThreadpoolEnvironment
 - winbase/InitializeThreadpoolEnvironment
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
 - InitializeThreadpoolEnvironment
---

# InitializeThreadpoolEnvironment function


## -description

Initializes a callback environment.

## -parameters

### -param pcbe [out]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines a callback environment.

## -remarks

By default, a callback executes in the default thread pool for the process. No cleanup group is associated with the callback environment, the caller is responsible for keeping the callback's DLL loaded while there are outstanding callbacks, and the callback is expected to run in a reasonable amount of time for the application. 

Create a callback environment if you plan to call one of the following functions to modify the environment:

<ul>
<li>
<a href="/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbackcleanupgroup">SetThreadpoolCallbackCleanupGroup</a>
</li>
<li>
<a href="/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbacklibrary">SetThreadpoolCallbackLibrary</a>
</li>
<li>
<a href="/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbackpool">SetThreadpoolCallbackPool</a>
</li>
<li>
<a href="/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbackpriority">SetThreadpoolCallbackPriority</a>
</li>
<li>
<a href="/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbackrunslong">SetThreadpoolCallbackRunsLong</a>
</li>
</ul>
To use the default callback environment, set the optional callback environment parameter to NULL when calling one of the following functions: 

<ul>
<li>
<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolio">CreateThreadpoolIo</a>
</li>
<li>
<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpooltimer">CreateThreadpoolTimer</a>
</li>
<li>
<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwait">CreateThreadpoolWait</a>
</li>
<li>
<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwork">CreateThreadpoolWork</a>
</li>
<li>
<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-trysubmitthreadpoolcallback">TrySubmitThreadpoolCallback</a>
</li>
</ul>
The <b>InitializeThreadpoolEnvironment</b> function is implemented as an inline function.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="/windows/desktop/ProcThread/using-the-thread-pool-functions">Using the Thread Pool Functions</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-destroythreadpoolenvironment">DestroyThreadpoolEnvironment</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbackcleanupgroup">SetThreadpoolCallbackCleanupGroup</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbacklibrary">SetThreadpoolCallbackLibrary</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbackpool">SetThreadpoolCallbackPool</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbackrunslong">SetThreadpoolCallbackRunsLong</a>



<a href="/windows/desktop/ProcThread/thread-pools">Thread Pools</a>