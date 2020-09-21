---
UID: NC:winnt.PTP_CLEANUP_GROUP_CANCEL_CALLBACK
title: PTP_CLEANUP_GROUP_CANCEL_CALLBACK (winnt.h)
description: Applications implement this callback if they call the SetThreadpoolCallbackCleanupGroup function to specify the callback to use when CloseThreadpoolCleanupGroup is called.
helpviewer_keywords: ["PTP_CLEANUP_GROUP_CANCEL_CALLBACK","PTP_CLEANUP_GROUP_CANCEL_CALLBACK callback","PTP_CLEANUP_GROUP_CANCEL_CALLBACK callback function","base.cleanupgroupcancelcallback","winnt/PTP_CLEANUP_GROUP_CANCEL_CALLBACK"]
old-location: base\cleanupgroupcancelcallback.htm
tech.root: backup
ms.assetid: 5704b0df-a868-40f0-9bcf-41274facb0b5
ms.date: 12/05/2018
ms.keywords: PTP_CLEANUP_GROUP_CANCEL_CALLBACK, PTP_CLEANUP_GROUP_CANCEL_CALLBACK callback, PTP_CLEANUP_GROUP_CANCEL_CALLBACK callback function, base.cleanupgroupcancelcallback, winnt/PTP_CLEANUP_GROUP_CANCEL_CALLBACK
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PTP_CLEANUP_GROUP_CANCEL_CALLBACK
 - winnt/PTP_CLEANUP_GROUP_CANCEL_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WinNT.h
api_name:
 - PTP_CLEANUP_GROUP_CANCEL_CALLBACK
---

# PTP_CLEANUP_GROUP_CANCEL_CALLBACK callback function


## -description

Applications implement this callback if they call the <a href="/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbackcleanupgroup">SetThreadpoolCallbackCleanupGroup</a> function to specify the callback to use when <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolcleanupgroup">CloseThreadpoolCleanupGroup</a> is called.

The <b>PTP_CLEANUP_GROUP_CANCEL_CALLBACK</b> type defines a pointer to this callback function. <i>CleanupGroupCancelCallback</i> is a placeholder for the application-defined function name.

## -parameters

### -param ObjectContext [in, out, optional]

Optional application-defined data specified during creation of the object.

### -param CleanupContext [in, out, optional]

Optional application-defined data specified using <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolcleanupgroupmembers">CloseThreadpoolCleanupGroupMembers</a>.

## -see-also

<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolcleanupgroup">CloseThreadpoolCleanupGroup</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolcleanupgroupmembers">CloseThreadpoolCleanupGroupMembers</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbackcleanupgroup">SetThreadpoolCallbackCleanupGroup</a>



<a href="/windows/desktop/ProcThread/thread-pools">Thread Pools</a>