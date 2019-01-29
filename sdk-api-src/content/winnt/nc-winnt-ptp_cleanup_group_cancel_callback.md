---
UID: NC:winnt.PTP_CLEANUP_GROUP_CANCEL_CALLBACK
title: PTP_CLEANUP_GROUP_CANCEL_CALLBACK
author: windows-sdk-content
description: Applications implement this callback if they call the SetThreadpoolCallbackCleanupGroup function to specify the callback to use when CloseThreadpoolCleanupGroup is called.
old-location: base\cleanupgroupcancelcallback.htm
tech.root: ProcThread
ms.assetid: 5704b0df-a868-40f0-9bcf-41274facb0b5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PTP_CLEANUP_GROUP_CANCEL_CALLBACK, PTP_CLEANUP_GROUP_CANCEL_CALLBACK callback, PTP_CLEANUP_GROUP_CANCEL_CALLBACK callback function, base.cleanupgroupcancelcallback, winnt/PTP_CLEANUP_GROUP_CANCEL_CALLBACK
ms.topic: callback
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - UserDefined
api_location:
 - WinNT.h
api_name:
 - PTP_CLEANUP_GROUP_CANCEL_CALLBACK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PTP_CLEANUP_GROUP_CANCEL_CALLBACK callback function


## -description


Applications implement this callback if they call the <a href="https://msdn.microsoft.com/395db7ba-ff39-46ee-917b-2896a0e99d43">SetThreadpoolCallbackCleanupGroup</a> function to specify the callback to use when <a href="https://msdn.microsoft.com/e38e4d99-63f2-4bac-8675-cf0f3aa149a7">CloseThreadpoolCleanupGroup</a> is called.

The <b>PTP_CLEANUP_GROUP_CANCEL_CALLBACK</b> type defines a pointer to this callback function. <i>CleanupGroupCancelCallback</i> is a placeholder for the application-defined function name.


## -parameters




### -param ObjectContext [in, out, optional]

Optional application-defined data specified during creation of the object.


### -param CleanupContext [in, out, optional]

Optional application-defined data specified using <a href="https://msdn.microsoft.com/9c78db13-d8dd-4eda-83d9-c9dbbfc6e822">CloseThreadpoolCleanupGroupMembers</a>.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/e38e4d99-63f2-4bac-8675-cf0f3aa149a7">CloseThreadpoolCleanupGroup</a>



<a href="https://msdn.microsoft.com/9c78db13-d8dd-4eda-83d9-c9dbbfc6e822">CloseThreadpoolCleanupGroupMembers</a>



<a href="https://msdn.microsoft.com/395db7ba-ff39-46ee-917b-2896a0e99d43">SetThreadpoolCallbackCleanupGroup</a>



<a href="https://msdn.microsoft.com/abe0798a-0b60-4bdb-a61e-45393f1e958d">Thread Pools</a>
 

 

