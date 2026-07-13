---
UID: NF:winbase.SetThreadpoolCallbackRunsLong
title: SetThreadpoolCallbackRunsLong function (winbase.h)
description: Indicates that callbacks associated with this callback environment may not return quickly. (SetThreadpoolCallbackRunsLong)
helpviewer_keywords: ["SetThreadpoolCallbackRunsLong","SetThreadpoolCallbackRunsLong function","base.setthreadpoolcallbackrunslong","winbase/SetThreadpoolCallbackRunsLong"]
old-location: base\setthreadpoolcallbackrunslong.htm
tech.root: backup
ms.assetid: 19ca0501-02d8-4851-8015-65e53d6f8074
ms.date: 12/05/2018
ms.keywords: SetThreadpoolCallbackRunsLong, SetThreadpoolCallbackRunsLong function, base.setthreadpoolcallbackrunslong, winbase/SetThreadpoolCallbackRunsLong
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
 - SetThreadpoolCallbackRunsLong
 - winbase/SetThreadpoolCallbackRunsLong
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
 - SetThreadpoolCallbackRunsLong
---

# SetThreadpoolCallbackRunsLong function


## -description

Indicates that callbacks associated with this callback environment may not return quickly.

## -parameters

### -param pcbe [in, out]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines the callback environment. The <a href="/windows/desktop/api/winbase/nf-winbase-initializethreadpoolenvironment">InitializeThreadpoolEnvironment</a> function returns this structure.

## -remarks

The thread pool may use this information to better determine when a new thread should be created.

This function is implemented as an inline function.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.

## -see-also

<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-callbackmayrunlong">CallbackMayRunLong</a>



<a href="/windows/desktop/api/winbase/nf-winbase-destroythreadpoolenvironment">DestroyThreadpoolEnvironment</a>



<a href="/windows/desktop/api/winbase/nf-winbase-initializethreadpoolenvironment">InitializeThreadpoolEnvironment</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbackcleanupgroup">SetThreadpoolCallbackCleanupGroup</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbacklibrary">SetThreadpoolCallbackLibrary</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbackpool">SetThreadpoolCallbackPool</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbackpriority">SetThreadpoolCallbackPriority</a>



<a href="/windows/desktop/ProcThread/thread-pools">Thread Pools</a>
