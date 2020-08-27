---
UID: NF:winbase.DestroyThreadpoolEnvironment
title: DestroyThreadpoolEnvironment function (winbase.h)
description: Deletes the specified callback environment. Call this function when the callback environment is no longer needed for creating new thread pool objects.
helpviewer_keywords: ["DestroyThreadpoolEnvironment","DestroyThreadpoolEnvironment function","base.destroythreadpoolenvironment","winbase/DestroyThreadpoolEnvironment"]
old-location: base\destroythreadpoolenvironment.htm
tech.root: backup
ms.assetid: b6a635f3-a603-4c2f-9aa9-1baa51922394
ms.date: 12/05/2018
ms.keywords: DestroyThreadpoolEnvironment, DestroyThreadpoolEnvironment function, base.destroythreadpoolenvironment, winbase/DestroyThreadpoolEnvironment
f1_keywords:
- winbase/DestroyThreadpoolEnvironment
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- WinBase.h
api_name:
- DestroyThreadpoolEnvironment
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DestroyThreadpoolEnvironment function


## -description


Deletes the specified callback environment. Call this function when the callback environment is no longer needed for creating new thread pool objects.


## -parameters




### -param pcbe [in, out]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines the callback environment. The <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-initializethreadpoolenvironment">InitializeThreadpoolEnvironment</a> function returns this structure.


## -remarks



This function is implemented as an inline function.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-initializethreadpoolenvironment">InitializeThreadpoolEnvironment</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbackcleanupgroup">SetThreadpoolCallbackCleanupGroup</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbacklibrary">SetThreadpoolCallbackLibrary</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbackpool">SetThreadpoolCallbackPool</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbackpriority">SetThreadpoolCallbackPriority</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbackrunslong">SetThreadpoolCallbackRunsLong</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/thread-pools">Thread Pools</a>
 

 

