---
UID: NF:avrt.AvRevertMmThreadCharacteristics
title: AvRevertMmThreadCharacteristics function (avrt.h)
author: windows-sdk-content
description: Indicates that a thread is no longer performing work associated with the specified task.
old-location: base\avrevertmmthreadcharacteristics.htm
tech.root: ProcThread
ms.assetid: 2ae0d34c-3819-46fa-9779-5de8a57e5281
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AvRevertMmThreadCharacteristics, AvRevertMmThreadCharacteristics function, avrt/AvRevertMmThreadCharacteristics, base.avrevertmmthreadcharacteristics
ms.topic: function
f1_keywords: ["avrt/AvRevertMmThreadCharacteristics"]
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
 - AvRevertMmThreadCharacteristics
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AvRevertMmThreadCharacteristics function


## -description


Indicates that a thread is no longer performing work associated with the specified task.


## -parameters




### -param AvrtHandle [in]

A handle to the task. This handle is returned by the <a href="https://docs.microsoft.com/windows/desktop/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa">AvSetMmThreadCharacteristics</a> or <a href="https://docs.microsoft.com/windows/desktop/api/avrt/nf-avrt-avsetmmmaxthreadcharacteristicsa">AvSetMmMaxThreadCharacteristics</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



This function must be called from the same thread that called the <a href="https://docs.microsoft.com/windows/desktop/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa">AvSetMmThreadCharacteristics</a> or <a href="https://docs.microsoft.com/windows/desktop/api/avrt/nf-avrt-avsetmmmaxthreadcharacteristicsa">AvSetMmMaxThreadCharacteristics</a> function to create the handle. Otherwise, the function will fail.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/ProcThread/multimedia-class-scheduler-service">Multimedia Class Scheduler Service</a>
 

 

