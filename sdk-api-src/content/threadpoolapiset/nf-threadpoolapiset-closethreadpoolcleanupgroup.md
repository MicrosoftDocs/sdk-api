---
UID: NF:threadpoolapiset.CloseThreadpoolCleanupGroup
title: CloseThreadpoolCleanupGroup function
author: windows-sdk-content
description: Closes the specified cleanup group.
old-location: base\closethreadpoolcleanupgroup.htm
tech.root: ProcThread
ms.assetid: e38e4d99-63f2-4bac-8675-cf0f3aa149a7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CloseThreadpoolCleanupGroup, CloseThreadpoolCleanupGroup function, base.closethreadpoolcleanupgroup, threadpoolapiset/CloseThreadpoolCleanupGroup, winbase/CloseThreadpoolCleanupGroup
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CloseThreadpoolCleanupGroup function


## -description


Closes the specified cleanup group.


## -parameters




### -param ptpcg [in, out]

A <b>TP_CLEANUP_GROUP</b> structure that defines the cleanup group. The <a href="https://msdn.microsoft.com/668593fe-2ed1-418d-8cd5-5fac61826ea1">CreateThreadpoolCleanupGroup</a> returns this structure.


## -returns



This function does not return a value.




## -remarks



The cleanup group must have no members when you call this function. For information on removing members of the group, see <a href="https://msdn.microsoft.com/9c78db13-d8dd-4eda-83d9-c9dbbfc6e822">CloseThreadpoolCleanupGroupMembers</a>.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/3d349c83-8b1a-4a5b-9625-be905d613b92">Using the Thread Pool Functions</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9c78db13-d8dd-4eda-83d9-c9dbbfc6e822">CloseThreadpoolCleanupGroupMembers</a>



<a href="https://msdn.microsoft.com/668593fe-2ed1-418d-8cd5-5fac61826ea1">CreateThreadpoolCleanupGroup</a>



<a href="https://msdn.microsoft.com/abe0798a-0b60-4bdb-a61e-45393f1e958d">Thread Pools</a>
 

 

