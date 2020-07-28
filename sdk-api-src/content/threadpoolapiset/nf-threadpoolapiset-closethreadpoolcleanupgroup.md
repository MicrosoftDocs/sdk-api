---
UID: NF:threadpoolapiset.CloseThreadpoolCleanupGroup
title: CloseThreadpoolCleanupGroup function (threadpoolapiset.h)
description: Closes the specified cleanup group.
helpviewer_keywords: ["CloseThreadpoolCleanupGroup","CloseThreadpoolCleanupGroup function","base.closethreadpoolcleanupgroup","threadpoolapiset/CloseThreadpoolCleanupGroup","winbase/CloseThreadpoolCleanupGroup"]
old-location: base\closethreadpoolcleanupgroup.htm
tech.root: backup
ms.assetid: e38e4d99-63f2-4bac-8675-cf0f3aa149a7
ms.date: 12/05/2018
ms.keywords: CloseThreadpoolCleanupGroup, CloseThreadpoolCleanupGroup function, base.closethreadpoolcleanupgroup, threadpoolapiset/CloseThreadpoolCleanupGroup, winbase/CloseThreadpoolCleanupGroup
f1_keywords:
- threadpoolapiset/CloseThreadpoolCleanupGroup
dev_langs:
- c++
req.header: threadpoolapiset.h
req.include-header: Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
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
- CloseThreadpoolCleanupGroup
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CloseThreadpoolCleanupGroup function


## -description


Closes the specified cleanup group.


## -parameters




### -param ptpcg [in, out]

A <b>TP_CLEANUP_GROUP</b> structure that defines the cleanup group. The <a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolcleanupgroup">CreateThreadpoolCleanupGroup</a> returns this structure.


## -remarks



The cleanup group must have no members when you call this function. For information on removing members of the group, see <a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolcleanupgroupmembers">CloseThreadpoolCleanupGroupMembers</a>.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="https://docs.microsoft.com/windows/desktop/ProcThread/using-the-thread-pool-functions">Using the Thread Pool Functions</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolcleanupgroupmembers">CloseThreadpoolCleanupGroupMembers</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolcleanupgroup">CreateThreadpoolCleanupGroup</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/thread-pools">Thread Pools</a>
 

 

