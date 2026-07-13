---
UID: NF:threadpoolapiset.CloseThreadpoolWork
title: CloseThreadpoolWork function (threadpoolapiset.h)
description: Releases the specified work object.
helpviewer_keywords: ["CloseThreadpoolWork","CloseThreadpoolWork function","base.closethreadpoolwork","threadpoolapiset/CloseThreadpoolWork","winbase/CloseThreadpoolWork"]
old-location: base\closethreadpoolwork.htm
tech.root: backup
ms.assetid: 89d7362e-0814-4f7e-a27f-8a297e210559
ms.date: 12/05/2018
ms.keywords: CloseThreadpoolWork, CloseThreadpoolWork function, base.closethreadpoolwork, threadpoolapiset/CloseThreadpoolWork, winbase/CloseThreadpoolWork
req.header: threadpoolapiset.h
req.include-header: Windows.h on Windows 7, Windows Server 2008  Windows Server 2008 R2
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CloseThreadpoolWork
 - threadpoolapiset/CloseThreadpoolWork
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-threadpool-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-threadpool-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - CloseThreadpoolWork
---

# CloseThreadpoolWork function


## -description

Releases the specified work object.

## -parameters

### -param pwk [in, out]

A pointer to a <b>TP_WORK</b> structure that defines the work object. The <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwork">CreateThreadpoolWork</a> function returns this pointer.

## -remarks

The work object is freed immediately if there are no outstanding callbacks; otherwise, the work object is freed asynchronously after the outstanding callbacks complete.

If there is a cleanup group associated with the work object, it is not necessary to call this function; calling the <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolcleanupgroupmembers">CloseThreadpoolCleanupGroupMembers</a> function releases the  work, wait, and timer objects associated with the cleanup group.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.

## -see-also

<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwork">CreateThreadpoolWork</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-submitthreadpoolwork">SubmitThreadpoolWork</a>



<a href="/windows/desktop/ProcThread/thread-pools">Thread Pools</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpoolworkcallbacks">WaitForThreadpoolWorkCallbacks</a>