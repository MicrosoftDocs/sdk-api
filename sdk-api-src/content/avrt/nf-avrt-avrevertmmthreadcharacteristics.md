---
UID: NF:avrt.AvRevertMmThreadCharacteristics
title: AvRevertMmThreadCharacteristics function (avrt.h)
description: Indicates that a thread is no longer performing work associated with the specified task.
helpviewer_keywords: ["AvRevertMmThreadCharacteristics","AvRevertMmThreadCharacteristics function","avrt/AvRevertMmThreadCharacteristics","base.avrevertmmthreadcharacteristics"]
old-location: base\avrevertmmthreadcharacteristics.htm
tech.root: backup
ms.assetid: 2ae0d34c-3819-46fa-9779-5de8a57e5281
ms.date: 12/05/2018
ms.keywords: AvRevertMmThreadCharacteristics, AvRevertMmThreadCharacteristics function, avrt/AvRevertMmThreadCharacteristics, base.avrevertmmthreadcharacteristics
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
 - AvRevertMmThreadCharacteristics
 - avrt/AvRevertMmThreadCharacteristics
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
 - AvRevertMmThreadCharacteristics
---

# AvRevertMmThreadCharacteristics function


## -description

Indicates that a thread is no longer performing work associated with the specified task.

## -parameters

### -param AvrtHandle [in]

A handle to the task. This handle is returned by the <a href="/windows/desktop/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa">AvSetMmThreadCharacteristics</a> or <a href="/windows/desktop/api/avrt/nf-avrt-avsetmmmaxthreadcharacteristicsa">AvSetMmMaxThreadCharacteristics</a> function.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function must be called from the same thread that called the <a href="/windows/desktop/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa">AvSetMmThreadCharacteristics</a> or <a href="/windows/desktop/api/avrt/nf-avrt-avsetmmmaxthreadcharacteristicsa">AvSetMmMaxThreadCharacteristics</a> function to create the handle. Otherwise, the function will fail.

## -see-also

<a href="/windows/desktop/ProcThread/multimedia-class-scheduler-service">Multimedia Class Scheduler Service</a>