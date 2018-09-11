---
UID: NF:avrt.AvRtJoinThreadOrderingGroup
title: AvRtJoinThreadOrderingGroup function
author: windows-sdk-content
description: Joins client threads to a thread ordering group.
old-location: base\avrtjointhreadorderinggroup.htm
tech.root: procthread
ms.assetid: 76e70f91-750e-49c8-8ddf-e8eddd150aa4
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: AvRtJoinThreadOrderingGroup, AvRtJoinThreadOrderingGroup function, avrt/AvRtJoinThreadOrderingGroup, base.avrtjointhreadorderinggroup
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Avrt.dll
api_name:
 - AvRtJoinThreadOrderingGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The thread encloses the code to be executed during each period within a loop that is controlled by the <a href="https://msdn.microsoft.com/11318ce3-d938-4bb5-adb1-28dd15e8cd80">AvRtWaitOnThreadOrderingGroup</a> function.

A thread can create more than one thread ordering group and join more than one thread ordering group. However, a thread cannot join the same thread ordering group more than one time.

The number of threads that can join a group is limited only by available system resources.




## -see-also




<a href="https://msdn.microsoft.com/5c37873a-ced4-447e-a6e1-55cfa8ab24b4">Thread Ordering Service</a>
 

 

