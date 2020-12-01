---
UID: NF:avrt.AvSetMmThreadPriority
title: AvSetMmThreadPriority function (avrt.h)
description: Adjusts the thread priority of the calling thread relative to other threads performing the same task.
helpviewer_keywords: ["AVRT_PRIORITY_CRITICAL","AVRT_PRIORITY_HIGH","AVRT_PRIORITY_LOW","AVRT_PRIORITY_NORMAL","AvSetMmThreadPriority","AvSetMmThreadPriority function","avrt/AvSetMmThreadPriority","base.avsetmmthreadpriority"]
old-location: base\avsetmmthreadpriority.htm
tech.root: backup
ms.assetid: 74259dbc-a9e9-409e-96e6-66a9dc590099
ms.date: 12/05/2018
ms.keywords: AVRT_PRIORITY_CRITICAL, AVRT_PRIORITY_HIGH, AVRT_PRIORITY_LOW, AVRT_PRIORITY_NORMAL, AvSetMmThreadPriority, AvSetMmThreadPriority function, avrt/AvSetMmThreadPriority, base.avsetmmthreadpriority
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
 - AvSetMmThreadPriority
 - avrt/AvSetMmThreadPriority
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
 - AvSetMmThreadPriority
---

# AvSetMmThreadPriority function


## -description

Adjusts the thread priority of the calling thread relative to other threads performing the same task.

## -parameters

### -param AvrtHandle [in]

A handle to the task. This handle is returned by the <a href="/windows/desktop/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa">AvSetMmThreadCharacteristics</a> or <a href="/windows/desktop/api/avrt/nf-avrt-avsetmmmaxthreadcharacteristicsa">AvSetMmMaxThreadCharacteristics</a> function.

### -param Priority [in]

The relative thread priority of this thread to other threads performing a similar task. This parameter can be one of the following values.



#### AVRT_PRIORITY_CRITICAL (2)



#### AVRT_PRIORITY_HIGH (1)



#### AVRT_PRIORITY_LOW (-1)



#### AVRT_PRIORITY_NORMAL (0)

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/ProcThread/multimedia-class-scheduler-service">Multimedia Class Scheduler Service</a>