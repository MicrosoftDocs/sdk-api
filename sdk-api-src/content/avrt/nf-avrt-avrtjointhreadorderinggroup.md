---
UID: NF:avrt.AvRtJoinThreadOrderingGroup
title: AvRtJoinThreadOrderingGroup function (avrt.h)
description: Joins client threads to a thread ordering group.
helpviewer_keywords: ["AvRtJoinThreadOrderingGroup","AvRtJoinThreadOrderingGroup function","avrt/AvRtJoinThreadOrderingGroup","base.avrtjointhreadorderinggroup"]
old-location: base\avrtjointhreadorderinggroup.htm
tech.root: backup
ms.assetid: 76e70f91-750e-49c8-8ddf-e8eddd150aa4
ms.date: 12/05/2018
ms.keywords: AvRtJoinThreadOrderingGroup, AvRtJoinThreadOrderingGroup function, avrt/AvRtJoinThreadOrderingGroup, base.avrtjointhreadorderinggroup
req.header: avrt.h
req.include-header: 
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
req.lib: Avrt.lib
req.dll: Avrt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AvRtJoinThreadOrderingGroup
 - avrt/AvRtJoinThreadOrderingGroup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Avrt.dll
api_name:
 - AvRtJoinThreadOrderingGroup
---

# AvRtJoinThreadOrderingGroup function


## -description

Joins client threads to a thread ordering group.

## -parameters

### -param Context [out]

A pointer to a context handle.

### -param ThreadOrderingGuid [in]

A pointer to the unique identifier for the thread ordering group.

### -param Before [in]

The thread order. If this parameter is <b>TRUE</b>, the thread is a predecessor thread that is scheduled to run before the parent thread. If this parameter is <b>FALSE</b>, the thread is a successor thread that is scheduled to run after the parent thread.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The thread encloses the code to be executed during each period within a loop that is controlled by the <a href="/windows/desktop/api/avrt/nf-avrt-avrtwaitonthreadorderinggroup">AvRtWaitOnThreadOrderingGroup</a> function.

A thread can create more than one thread ordering group and join more than one thread ordering group. However, a thread cannot join the same thread ordering group more than one time.

The number of threads that can join a group is limited only by available system resources.

## -see-also

<a href="/windows/desktop/ProcThread/thread-ordering-service">Thread Ordering Service</a>