---
UID: NE:dispatcherqueue.DISPATCHERQUEUE_THREAD_APARTMENTTYPE
title: DISPATCHERQUEUE_THREAD_APARTMENTTYPE (dispatcherqueue.h)
description: Specifies the threading apartment type for a new DispatcherQueueController.
helpviewer_keywords: ["DISPATCHERQUEUE_THREAD_APARTMENTTYPE","DISPATCHERQUEUE_THREAD_APARTMENTTYPE enumeration","DQTAT_COM_ASTA","DQTAT_COM_NONE","DQTAT_COM_STA","base.dispatcherqueue_thread_apartmenttype","dispatcherqueue/DISPATCHERQUEUE_THREAD_APARTMENTTYPE","dispatcherqueue/DQTAT_COM_ASTA","dispatcherqueue/DQTAT_COM_NONE","dispatcherqueue/DQTAT_COM_STA"]
old-location: base\dispatcherqueue_thread_apartmenttype.htm
tech.root: backup
ms.assetid: 46BCD25E-22C7-4D9C-A424-AFF0B0B41AB6
ms.date: 12/05/2018
ms.keywords: DISPATCHERQUEUE_THREAD_APARTMENTTYPE, DISPATCHERQUEUE_THREAD_APARTMENTTYPE enumeration, DQTAT_COM_ASTA, DQTAT_COM_NONE, DQTAT_COM_STA, base.dispatcherqueue_thread_apartmenttype, dispatcherqueue/DISPATCHERQUEUE_THREAD_APARTMENTTYPE, dispatcherqueue/DQTAT_COM_ASTA, dispatcherqueue/DQTAT_COM_NONE, dispatcherqueue/DQTAT_COM_STA
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DISPATCHERQUEUE_THREAD_APARTMENTTYPE
 - dispatcherqueue/DISPATCHERQUEUE_THREAD_APARTMENTTYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DispatcherQueue.h
api_name:
 - DISPATCHERQUEUE_THREAD_APARTMENTTYPE
---

# DISPATCHERQUEUE_THREAD_APARTMENTTYPE enumeration


## -description

Specifies the threading apartment type for a new <a href="/uwp/api/windows.system.dispatcherqueuecontroller">DispatcherQueueController</a>.

## -enum-fields

### -field DQTAT_COM_NONE:0

No COM threading apartment type specified.

### -field DQTAT_COM_ASTA:1

Specifies an application single-threaded apartment (ASTA) COM threading apartment.

### -field DQTAT_COM_STA:2

Specifies a single-threaded apartment (STA) COM threading apartment.

## -remarks

This value is relevant when <a href="/windows/desktop/api/dispatcherqueue/ns-dispatcherqueue-dispatcherqueueoptions">DispatcherQueueOptions.threadType</a> is  <b>DQTYPE_THREAD_DEDICATED</b>. Use <b>DQTAT_COM_NONE</b> when <b>DispatcherQueueOptions.threadType</b> is <b>DQTYPE_THREAD_CURRENT</b>.

Introduced in Windows 10, version 1709.

## -see-also

<a href="/windows/desktop/api/dispatcherqueue/nf-dispatcherqueue-createdispatcherqueuecontroller">CreateDispatcherQueueController</a>



<a href="/windows/desktop/api/dispatcherqueue/ns-dispatcherqueue-dispatcherqueueoptions">DispatcherQueueOptions</a>
