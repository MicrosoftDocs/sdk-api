---
UID: NE:dispatcherqueue.DISPATCHERQUEUE_THREAD_APARTMENTTYPE
title: DISPATCHERQUEUE_THREAD_APARTMENTTYPE
author: windows-sdk-content
description: Specifies the threading apartment type for a new DispatcherQueueController.
old-location: base\dispatcherqueue_thread_apartmenttype.htm
tech.root: ProcThread
ms.assetid: 46BCD25E-22C7-4D9C-A424-AFF0B0B41AB6
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: DISPATCHERQUEUE_THREAD_APARTMENTTYPE, DISPATCHERQUEUE_THREAD_APARTMENTTYPE enumeration, DQTAT_COM_ASTA, DQTAT_COM_NONE, DQTAT_COM_STA, base.dispatcherqueue_thread_apartmenttype, dispatcherqueue/DISPATCHERQUEUE_THREAD_APARTMENTTYPE, dispatcherqueue/DQTAT_COM_ASTA, dispatcherqueue/DQTAT_COM_NONE, dispatcherqueue/DQTAT_COM_STA
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: dispatcherqueue.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - DispatcherQueue.h
api_name:
 - DISPATCHERQUEUE_THREAD_APARTMENTTYPE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DISPATCHERQUEUE_THREAD_APARTMENTTYPE enumeration


## -description


Specifies the threading apartment type for a new <a href="https://docs.microsoft.com/uwp/api/windows.system.dispatcherqueuecontroller">DispatcherQueueController</a>.


## -enum-fields




### -field DQTAT_COM_NONE

No COM threading apartment type specified.


### -field DQTAT_COM_ASTA

Specifies an application single-threaded apartment (ASTA) COM threading apartment.


### -field DQTAT_COM_STA

Specifies a single-threaded apartment (STA) COM threading apartment.


## -remarks



This value is relevant when <a href="https://msdn.microsoft.com/F9AF7DDE-13EB-43DB-BAD5-61A6ABD9307D">DispatcherQueueOptions.threadType</a> is  <b>DQTYPE_THREAD_DEDICATED</b>. Use <b>DQTAT_COM_NONE</b> when <b>DispatcherQueueOptions.threadType</b> is <b>DQTYPE_THREAD_CURRENT</b>.

Introduced in Windows 10, version 1709.




## -see-also




<a href="https://msdn.microsoft.com/750097BB-C4D1-4579-9353-582124D5CE3B">CreateDispatcherQueueController</a>



<a href="https://msdn.microsoft.com/F9AF7DDE-13EB-43DB-BAD5-61A6ABD9307D">DispatcherQueueOptions</a>
 

 

