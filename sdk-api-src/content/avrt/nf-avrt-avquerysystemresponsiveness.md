---
UID: NF:avrt.AvQuerySystemResponsiveness
title: AvQuerySystemResponsiveness function (avrt.h)
description: Retrieves the system responsiveness setting used by the multimedia class scheduler service.
helpviewer_keywords: ["AvQuerySystemResponsiveness","AvQuerySystemResponsiveness function","avrt/AvQuerySystemResponsiveness","base.avquerysystemresponsiveness"]
old-location: base\avquerysystemresponsiveness.htm
tech.root: backup
ms.assetid: 87184232-9f58-4a59-87e9-fdd081a7dc5c
ms.date: 12/05/2018
ms.keywords: AvQuerySystemResponsiveness, AvQuerySystemResponsiveness function, avrt/AvQuerySystemResponsiveness, base.avquerysystemresponsiveness
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
 - AvQuerySystemResponsiveness
 - avrt/AvQuerySystemResponsiveness
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
 - AvQuerySystemResponsiveness
---

# AvQuerySystemResponsiveness function


## -description

Retrieves the system responsiveness setting used by the multimedia class scheduler service.

## -parameters

### -param AvrtHandle [in]

A handle to the task. This handle is returned by the <a href="/windows/desktop/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa">AvSetMmThreadCharacteristics</a> or <a href="/windows/desktop/api/avrt/nf-avrt-avsetmmmaxthreadcharacteristicsa">AvSetMmMaxThreadCharacteristics</a> function.

### -param SystemResponsivenessValue [out]

The system responsiveness value. This value can range from 10 to 100 percent.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/ProcThread/multimedia-class-scheduler-service">Multimedia Class Scheduler Service</a>